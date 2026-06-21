# Test Cases: Phone Number Validation Feature

**Feature Under Test:** Add a phone number to request a taxi code.
**Requirement Specification:** The phone number field must accept exactly 10 digits, starting with a country code (e.g., +1 for US/Canada or your local region). It should not accept letters, special characters, or lengths other than specified.

### 🧠 Test Design Applied
* **Equivalence Partitioning (EP):** 
  * Valid Partition: Exactly 10 digits with '+' sign.
  * Invalid Partitions: Empty field, letters, special characters, less than 10 digits, more than 10 digits.
* **Boundary Value Analysis (BVA):** Testing 9 digits (boundary - 1), 10 digits (boundary), and 11 digits (boundary + 1).

### 📋 Test Cases Matrix

| Test Case ID | Description | Input Data | Expected Result | Status |
| :--- | :--- | :--- | :--- | :--- |
| **TC-UR-001** | Verify successful phone registration with valid 10-digit number (Positive) | `+12345678901` | Code confirmation modal is displayed; "Next" button is enabled. | PASSED |
| **TC-UR-002** | Verify error message when field is left empty (Negative) | *Leave Blank* | "Next" button remains disabled or error warning appears. | PASSED |
| **TC-UR-003** | Verify input rejection when inserting text/letters (Negative) | `+12345678AB` | Field rejects alphabet input or displays validation error. | PASSED |
| **TC-UR-004** | Boundary Test: Verify system response with 9 digits (Negative) | `+123456789` | "Next" button is disabled; validation fails. | PASSED |
| **TC-UR-005** | Boundary Test: Verify system response with 11 digits (Negative) | `+123456789012` | Field truncates input or triggers an invalid format error. | PASSED |
