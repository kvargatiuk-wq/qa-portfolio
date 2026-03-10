# API Testing
## 🔧 Tools
- Postman
- Newman (CLI runner)
- GitHub Actions (CI)

  ## 📊 Coverage
- Authentication endpoints: 10 tests
- Products API: 25 tests  
- Orders API: 15 tests

  ### Request Validation
- Required fields presence
- Data type correctness
- Amount/currency format
- UUID format for IDs

  ### Response Validation
- HTTP status codes (200, 201, 400, 404, 422, 500)
- Response body structure
- Field data types
- Pagination metadata

  ### Business Logic
- `stateResponse` transitions
- `businessFunctions` identifier & schema validation
- `documents` — title, type, and description integrity
- Multi-level nested object validation

  ## 🐛 Bug Report Example

| Field | Details |
|-------|---------|
| **ID** | BUG-001 |
| **Title** | Transaction API returns 200 with empty `stateResponse` array |
| **Severity** | Medium |
| **Steps** | Send GET /transactions with future date filter |
| **Expected** | 404 or empty paginated response |
| **Actual** | 200 OK with null `stateResponse` |

---
<img width="2423" height="1533" alt="Screenshot_4" src="https://github.com/user-attachments/assets/d3c78267-d34e-49f0-af9a-fdb3e2342402" />


<img width="2838" height="1530" alt="Screenshot_8" src="https://github.com/user-attachments/assets/5d3c946e-eea5-406b-9c71-f7895448ec16" />


<img width="2817" height="1382" alt="Screenshot_13" src="https://github.com/user-attachments/assets/e540cb67-c408-4711-834f-6958df0c3779" />

<img width="2868" height="1460" alt="Screenshot_4" src="https://github.com/user-attachments/assets/42b3ded9-ff95-4209-87ed-8688d02bf707" />

<img width="2246" height="1479" alt="Screenshot_5" src="https://github.com/user-attachments/assets/02587545-01fa-4000-aead-b217b05bb030" />

















