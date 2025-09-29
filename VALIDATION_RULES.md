# Data Validation Rules – Employee Data Form  

To ensure data accuracy, the following validation rules are applied in the **Form sheet**:  

| Field                  | Validation Formula | Rule / Error Message |
|-------------------------|--------------------|-----------------------|
| **Employee Name (C2)** | `=ISTEXT(C2)` | Must be text only (no numbers). *Error:* “Please enter a valid name.” |
| **Employee Code (C4)** | `=ISNUMBER(C4)` | Must be numeric. *Error:* “Please enter a valid Employee Code.” |
| **Email (C8)** | `=AND(ISNUMBER(SEARCH("@",C8)), ISNUMBER(SEARCH(".",C8)))` | Must follow `name@example.com`. *Error:* “Enter email in format name@example.com.” |
| **Date of Birth (C10)** | `=AND(ISNUMBER(C10), C10<TODAY())` | Must be a valid past date. *Error:* “Please enter a valid DOB.” |
| **Date of Joining (C12)** | `=ISNUMBER(C12)` | Must be a valid date. *Error:* “Please enter a valid date.” |
| **HRA (F6)** | `=ISNUMBER(F6)` | Must be numeric. *Error:* “Please enter numbers only.” |
| **Medical (F8)** | `=ISNUMBER(F8)` | Must be numeric. *Error:* “Please enter numbers only.” |
| **Conveyance (F10)** | `=ISNUMBER(F10)` | Must be numeric. *Error:* “Please enter numbers only.” |
| **Deductions (F12)** | `=ISNUMBER(F12)` | Must be numeric. *Error:* “Please enter numbers only.” |
| **Net Pay (F14)** | `=ISNUMBER(F14)` | Must be numeric. *Error:* “Please enter numbers only.” |

---

📌 These rules prevent invalid data (like text in numeric fields or invalid emails) and ensure consistent records in the **Database** sheet.  
