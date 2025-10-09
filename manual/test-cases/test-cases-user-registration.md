# Test Cases – User Registration

**Requirement Link:** [SSQ-29 – User Registration](https://storyspoilerqa.atlassian.net/browse/SSQ-29)  

This file documents the 22 test cases for the **Use Registration** feature.  
Each test case is traceable to its corresponding **Use Case** and **Requirement** in Jira.  

---

## TC-REG-01 – Verify Sign Up page
**Jira Test Case:** [SSQ-34](https://storyspoilerqa.atlassian.net/browse/SSQ-34)  
**Use Case:** [UC-REG-1](../use-cases/use-cases-user-registration.md#uc-reg-1--access-sign-up-page) (Jira: [SSQ-30](https://storyspoilerqa.atlassian.net/browse/SSQ-30))

**Prerequisites:** TD-01: Guest Session.

**Steps:**
1. Navigate to the app URL.
2. Click “SIGN UP” button in the navigation bar. 
3. Observe the registration form.

**Expected Result:**
The Sign Up page opens with all required fields visible:
- Username
- Email
- First Name
- Middle Name
- Last Name
- Password
- Confirm Password
- "SIGN UP" button
- "LOG IN HERE" button for registered users

**Execution Result:** ✅ Passed

**Related Query:** [QRY-REG-05](../queries/queries.md#qry-reg-05--label-discrepancy-for-repeat-password-vs-confirm-password) (Jira: [SSQ-65](https://storyspoilerqa.atlassian.net/browse/SSQ-65))

---

## TC-REG-02 – Verify registration with valid data without optional middle name
**Jira Test Case:** [SSQ-35](https://storyspoilerqa.atlassian.net/browse/SSQ-35)  
**Use Case:** [UC-REG-2](../use-cases/use-cases-user-registration.md#uc-reg-2--complete-registration-with-valid-data) (Jira: [SSQ-31](https://storyspoilerqa.atlassian.net/browse/SSQ-31))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button. 

**Expected Result:**  
Account created successfully. User is redirected to Log In page.

**Execution Result:** ✅ Passed

**Related Query:** [QRY-REG-07](../queries/queries.md#qry-reg-07--missing-character-type-constraints-for-all-input-fields) (Jira: [SSQ-68](https://storyspoilerqa.atlassian.net/browse/SSQ-68))

---

## TC-REG-03 – Verify registration with valid data with optional middle name
**Jira Test Case:** [SSQ-39](https://storyspoilerqa.atlassian.net/browse/SSQ-39)  
**Use Case:** [UC-REG-2](../use-cases/use-cases-user-registration.md#uc-reg-2--complete-registration-with-valid-data) (Jira: [SSQ-31](https://storyspoilerqa.atlassian.net/browse/SSQ-31))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-27 (valid middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button. 

**Expected Result:**  
Account created successfully. User is redirected to Log In page.

**Execution Result:** ✅ Passed

**Related Query:** [QRY-REG-07](../queries/queries.md#qry-reg-07--missing-character-type-constraints-for-all-input-fields) (Jira: [SSQ-68](https://storyspoilerqa.atlassian.net/browse/SSQ-68))

---

## TC-REG-04 – Verify validation for all required fields
**Jira Test Case:** [SSQ-40](https://storyspoilerqa.atlassian.net/browse/SSQ-40)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. Leave all fields empty.
4. Click “SIGN UP” button.

**Expected Result:**  
The user cannot complete the sign-up process.
Validation errors are displayed for all mandatory fields:
- Username
- Email
- First Name
- Last Name
- Password
- Confirm Password
Each required field displays a clear and user-friendly error message indicating that the field is mandatory.

**Execution Result:** ✅ Passed

**Related Queries:** 
- [QRY-REG-01](../queries/queries.md#qry-hp-01--requirements-for-home-page-for-logged-in-users-lack-visuals-and-detailed-content-specification) (Jira: [SSQ-59](https://storyspoilerqa.atlassian.net/browse/SSQ-59))
- [QRY-REG-03](../queries/queries.md#qry-reg-03--consistency-of-required-field-messages) (Jira: [SSQ-63](https://storyspoilerqa.atlassian.net/browse/SSQ-63))
- [QRY-REG-01](../queries/queries.md#qry-reg-06--required-field-indicators-not-defined-in-requirements) (Jira: [SSQ-66](https://storyspoilerqa.atlassian.net/browse/SSQ-66))

---

## TC-REG-05 – Verify validation for invalid username (too short)
**Jira Test Case:** [SSQ-38](https://storyspoilerqa.atlassian.net/browse/SSQ-38)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-05 (invalid username, too short).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Username must be at least 2 characters.

**Execution Result:** ✅ Passed

---

## TC-REG-06 – Verify validation for invalid username (too long)
**Jira Test Case:** [SSQ-36](https://storyspoilerqa.atlassian.net/browse/SSQ-36)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, attempt to enter TD-06 (invalid username, too long).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user cannot complete the sign-up process with a value exceeding the maximum length. The field enforces the 30-character limit by preventing additional input.

**Execution Result:** ✅ Passed

---

## TC-REG-07 – Verify validation for invalid email (missing '@')
**Jira Test Case:** [SSQ-37](https://storyspoilerqa.atlassian.net/browse/SSQ-37)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-10 (invalid email, missing '@').
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Email must contain ‘@'.

**Execution Result:** ✅ Passed

---

## TC-REG-08 – Verify validation for invalid email (missing '.')
**Jira Test Case:** [SSQ-41](https://storyspoilerqa.atlassian.net/browse/SSQ-41)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-11 (invalid email, missing '.').
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Email must contain ‘@' and '.’.

**Execution Result:** ❌ Failed

**Related Bugs:** 
- [BUG-REG-01](../bugs/bug-report.md#bug-reg-01--validation-error-message-does-not-specify-the-correct-email-address-format) (Jira: [SSQ-56](https://storyspoilerqa.atlassian.net/browse/SSQ-56))
- [BUG-REG-02](../bugs/bug-report.md#bug-reg-02--user-is-able-to-sign-up-with-an-invalid-email-address-missing-a-) (Jira: [SSQ-57](https://storyspoilerqa.atlassian.net/browse/SSQ-57))

---

## TC-REG-09 – Verify validation for invalid email (too short)
**Jira Test Case:** [SSQ-42](https://storyspoilerqa.atlassian.net/browse/SSQ-42)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-12 (invalid email, too short).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the email must be at least 6 characters.

**Execution Result:** ✅ Passed

---

## TC-REG-10 – Verify validation for invalid email (too long)
**Jira Test Case:** [SSQ-43](https://storyspoilerqa.atlassian.net/browse/SSQ-43)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-13 (invalid email, too long).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user cannot complete the sign-up process with a value exceeding the maximum length. The field enforces the 254-character limit by preventing additional input.

**Execution Result:** ✅ Passed

---

## TC-REG-11 – Verify validation for invalid first name (too short)
**Jira Test Case:** [SSQ-44](https://storyspoilerqa.atlassian.net/browse/SSQ-44)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-15 (invalid first name, too short).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the First Name must be at least 2 characters.

**Execution Result:** ✅ Passed

---

## TC-REG-12 – Verify validation for invalid first name (too long)
**Jira Test Case:** [SSQ-45](https://storyspoilerqa.atlassian.net/browse/SSQ-45)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-15 (invalid first name, too short).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user cannot complete the sign-up process with a value exceeding the maximum length. The field enforces the 60-character limit by preventing additional input.

**Execution Result:** ✅ Passed

---

## TC-REG-13 – Verify validation for invalid middle name (too short)
**Jira Test Case:** [SSQ-46](https://storyspoilerqa.atlassian.net/browse/SSQ-46)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-25 (invalid middle name, too short).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Middle Name must be at least 2 characters.

**Execution Result:** ❌ Failed

**Related Bug:** [BUG-REG-03](../bugs/bug-report.md#bug-reg-03--user-can-sign-up-with-a-middle-name-below-the-minimum-boundary) (Jira: [SSQ-58](https://storyspoilerqa.atlassian.net/browse/SSQ-58))


---

## TC-REG-14 – Verify validation for invalid middle name (too long)
**Jira Test Case:** [SSQ-47](https://storyspoilerqa.atlassian.net/browse/SSQ-47)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, attempt to enter TD-26 (invalid middle name, too long).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user cannot complete the sign-up process with a value exceeding the maximum length. The field enforces the 60-character limit by preventing additional input.

**Execution Result:** ✅ Passed

---

## TC-REG-15 – Verify validation for invalid last name (too short)
**Jira Test Case:** [SSQ-48](https://storyspoilerqa.atlassian.net/browse/SSQ-48)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-18 (invalid last name, too short).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Last Name must be at least 2 characters.

**Execution Result:** ❌ Failed

**Related Bug:** [BUG-REG-04](../bugs/bug-report.md#bug-reg-04--incorrect-field-reference-in-last-name-validation) (Jira: [SSQ-70](https://storyspoilerqa.atlassian.net/browse/SSQ-70))

---

## TC-REG-16 – Verify validation for invalid last name (too long)
**Jira Test Case:** [SSQ-49](https://storyspoilerqa.atlassian.net/browse/SSQ-49)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, attempt to enter TD-19 (invalid last name, too long).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user cannot complete the sign-up process with a value exceeding the maximum length. The field enforces the 60-character limit by preventing additional input.

**Execution Result:** ✅ Passed

---

## TC-REG-17 – Verify validation for invalid password (too short)
**Jira Test Case:** [SSQ-50](https://storyspoilerqa.atlassian.net/browse/SSQ-50)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-22 (invalid password, too short).
9. In the Confirm Password field, repeat the same password.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Password must be at least 6 characters.

**Execution Result:** ✅ Passed

**Related Query:** [QRY-REG-04](../queries/queries.md#qry-reg-04--validation-messages-tone-and-punctuation-consistency) (Jira: [SSQ-64](https://storyspoilerqa.atlassian.net/browse/SSQ-64))

---

## TC-REG-18 – Verify validation for invalid password (too long)
**Jira Test Case:** [SSQ-51](https://storyspoilerqa.atlassian.net/browse/SSQ-51)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, attempt to enter TD-23 (invalid password, too long).
9. In the Confirm Password field, repeat the same password.
10. Click “SIGN UP” button.

**Expected Result:**  
The user cannot complete the sign-up process with a value exceeding the maximum length. The field enforces the 30-character limit by preventing additional input.

**Execution Result:** ✅ Passed

---

## TC-REG-19 – Verify validation for invalid repeat password (mismatched)
**Jira Test Case:** [SSQ-52](https://storyspoilerqa.atlassian.net/browse/SSQ-52)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, enter TD-24 (invalid repeat password, mismatched).
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the passwords don’t match.

**Execution Result:** ✅ Passed

**Related Queries:** 
- [QRY-REG-03](../queries/queries.md#qry-reg-03--consistency-of-required-field-messages) (Jira: [SSQ-63](https://storyspoilerqa.atlassian.net/browse/SSQ-63))
- [QRY-REG-04](../queries/queries.md#qry-reg-04--validation-messages-tone-and-punctuation-consistency) (Jira: [SSQ-64](https://storyspoilerqa.atlassian.net/browse/SSQ-64))

---

## TC-REG-20 – Verify validation for existing username reuse
**Jira Test Case:** [SSQ-53](https://storyspoilerqa.atlassian.net/browse/SSQ-53)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-02 (invalid username, already existing).
4. In the Email field, enter TD-09 (valid email).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Username already exists.

**Execution Result:** ✅ Passed

**Related Queries:** 
- [QRY-REG-01](../queries/queries.md#qry-reg-01--consistency-of-capitalization-in-field-names) (Jira: [SSQ-59](https://storyspoilerqa.atlassian.net/browse/SSQ-59))
- [QRY-REG-02](../queries/queries.md#qry-reg-02--extra-bullet-point-before-error-messages) (Jira: [SSQ-60](https://storyspoilerqa.atlassian.net/browse/SSQ-60))

---

## TC-REG-21 – Verify validation for existing email reuse
**Jira Test Case:** [SSQ-54](https://storyspoilerqa.atlassian.net/browse/SSQ-54)  
**Use Case:** [UC-REG-3](../use-cases/use-cases-user-registration.md#uc-reg-3--validation-errors-during-registration) (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-29 (invalid email, already existing).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Email is already in use.

**Execution Result:** ✅ Passed

**Related Query:** [QRY-REG-02](../queries/queries.md#qry-reg-02--extra-bullet-point-before-error-messages) (Jira: [SSQ-60](https://storyspoilerqa.atlassian.net/browse/SSQ-60))

---

## TC-REG-22 – Verify "LOG IN HERE" button redirects to Log In page
**Jira Test Case:** [SSQ-55](https://storyspoilerqa.atlassian.net/browse/SSQ-55)  
**Use Case:** [UC-REG-4](../use-cases/use-cases-user-registration.md#uc-reg-4--cancel-or-redirect-to-log-in) (Jira: [SSQ-33](https://storyspoilerqa.atlassian.net/browse/SSQ-33))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. Click "LOG IN HERE" button at the bottom.

**Expected Result:**  
User is redirected to the Log In page.

**Execution Result:** ✅ Passed

---