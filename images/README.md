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





# 🗂️ Manual Testing Documentation
## 📌 Project Overview

This section covers **manual QA documentation** for a Financial Payments Platform, including:
- Detailed test case tables with priority, status, and expected results
- End-to-end functional testing of business flows
- Regression and smoke test checklists
- Bug reports with reproduction steps

  ## ✅ Test Case Structure

Each test case follows this format:

| Field | Description |
|-------|-------------|
| **Test ID** | Unique identifier (e.g., TC-001) |
| **Testing Object** | Feature/module under test |
| **Test Case Name** | Short description of what is tested |
| **Preconditions** | Required state before test execution |
| **Priority** | High / Medium / Low |
| **Type** | Functional / Regression / Smoke / Negative |
| **Status** | Passed / Failed / Blocked / Not Run |
| **Steps** | Numbered test execution steps |
| **Expected Result** | What should happen |
| **Actual Result** | What actually happened |
| **Evidence** | Screenshot or video link |

---
### Test Types Distribution

| Type | Count |
|------|-------|
| ✅ Functional | 55 |
| 🔁 Regression | 25 |
| 💨 Smoke | 12 |
| ❌ Negative | 10 |

---
## 🐛 Bug Report Example

```
ID:           BUG-042
Title:        Payment creation fails when currency is EUR and amount > 10,000
Severity:     High
Priority:     High
Status:       Open
Environment:  Staging / Chrome 122

Steps to Reproduce:
  1. Navigate to Payments → Create New Payment
  2. Set currency = EUR
  3. Enter amount = 15000
  4. Click "Submit"

Expected Result:
  Payment is created successfully with status "Pending"

Actual Result:
  Error 422 returned — "Amount exceeds limit" (no limit documented)

Attachments:
  - screenshot_bug042.png
  - network_log_bug042.har
```

---

## 💨 Smoke Test Checklist

- [ ] Platform loads without errors
- [ ] User can log in with valid credentials
- [ ] Dashboard displays account balance
- [ ] Create new payment — basic flow
- [ ] View transaction history
- [ ] Business functions list loads
- [ ] Document upload works

---

## 🔁 Regression Checklist

- [ ] All previously fixed bugs remain fixed
- [ ] Payment flow: create → submit → confirm
- [ ] Multi-currency: USD, EUR, GBP conversions
- [ ] Transaction filters: date, status, amount
- [ ] Business function: create → assign → complete
- [ ] Error handling: invalid inputs return correct error codes
- [ ] Pagination works on transactions list (25/50/100 per page)

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **Google Sheets / Excel** | Test case management |
| **Jira** | Bug tracking & project management |
| **Postman** | API response validation during manual tests |
| **Chrome DevTools** | Network log inspection |
| **Loom / Screenshots** | Test evidence capture |

---



<img width="2817" height="1382" alt="Screenshot_13" src="https://github.com/user-attachments/assets/e540cb67-c408-4711-834f-6958df0c3779" />

<img width="2868" height="1460" alt="Screenshot_4" src="https://github.com/user-attachments/assets/42b3ded9-ff95-4209-87ed-8688d02bf707" />

<img width="2246" height="1479" alt="Screenshot_5" src="https://github.com/user-attachments/assets/02587545-01fa-4000-aead-b217b05bb030" />

















