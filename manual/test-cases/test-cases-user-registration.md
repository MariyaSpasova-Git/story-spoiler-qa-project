# Test Cases – User Registration

**Requirement Link:** [SSQ-29 – User Registration](https://storyspoilerqa.atlassian.net/browse/SSQ-29)  

This file documents the 19 test cases for the **Use Registration** feature.  
Each test case is traceable to its corresponding **Use Case** and **Requirement** in Jira.  

---

## TC-REG-01 – Verify Sign Up page
**Jira Test Case:** [SSQ-34](https://storyspoilerqa.atlassian.net/browse/SSQ-34)
**Use Case:** UC-REG-1 (Jira: [SSQ-30](https://storyspoilerqa.atlassian.net/browse/SSQ-30))

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

---

## TC-REG-02 – Verify registration with valid data without optional middle name
**Jira Test Case:** [SSQ-35](https://storyspoilerqa.atlassian.net/browse/SSQ-35)
**Use Case:** UC-REG-2 (Jira: [SSQ-31](https://storyspoilerqa.atlassian.net/browse/SSQ-31))

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

---

## TC-REG-03 – Verify registration with valid data with optional middle name
**Jira Test Case:** [SSQ-39](https://storyspoilerqa.atlassian.net/browse/SSQ-39)
**Use Case:** UC-REG-2 (Jira: [SSQ-31](https://storyspoilerqa.atlassian.net/browse/SSQ-31))

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

---

## TC-REG-04 – Verify validation for all required fields
**Jira Test Case:** [SSQ-40](https://storyspoilerqa.atlassian.net/browse/SSQ-40)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-05 – Verify validation for invalid username (too short)
**Jira Test Case:** [SSQ-38](https://storyspoilerqa.atlassian.net/browse/SSQ-38)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Username must be between 2–30 characters.

---

## TC-REG-06 – Verify validation for invalid username (too long)
**Jira Test Case:** [SSQ-36](https://storyspoilerqa.atlassian.net/browse/SSQ-36)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-07 – Verify validation for invalid email (missing '@')
**Jira Test Case:** [SSQ-37](https://storyspoilerqa.atlassian.net/browse/SSQ-37)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Email must contain ‘@' and '.’.

---

## TC-REG-08 – Verify validation for invalid email (missing '.')
**Jira Test Case:** [SSQ-41](https://storyspoilerqa.atlassian.net/browse/SSQ-41)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-09 – Verify validation for invalid email (too short)
**Jira Test Case:** [SSQ-42](https://storyspoilerqa.atlassian.net/browse/SSQ-42)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the email must be between 6–254 characters.

---

## TC-REG-10 – Verify validation for invalid email (too long)
**Jira Test Case:** [SSQ-43](https://storyspoilerqa.atlassian.net/browse/SSQ-43)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-11 – Verify validation for invalid first name (too short)
**Jira Test Case:** [SSQ-44](https://storyspoilerqa.atlassian.net/browse/SSQ-44)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the First Name must be between 2–60 characters.

---

## TC-REG-12 – Verify validation for invalid first name (too long)
**Jira Test Case:** [SSQ-45](https://storyspoilerqa.atlassian.net/browse/SSQ-45)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-13 – Verify validation for invalid middle name (too short)
**Jira Test Case:** [SSQ-46](https://storyspoilerqa.atlassian.net/browse/SSQ-46)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Middle Name must be between 2–60 characters.

---

## TC-REG-14 – Verify validation for invalid middle name (too long)
**Jira Test Case:** [SSQ-47](https://storyspoilerqa.atlassian.net/browse/SSQ-47)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-15 – Verify validation for invalid last name (too short)
**Jira Test Case:** [SSQ-48](https://storyspoilerqa.atlassian.net/browse/SSQ-48)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Last Name must be between 2–60 characters.

---

## TC-REG-16 – Verify validation for invalid last name (too long)
**Jira Test Case:** [SSQ-49](https://storyspoilerqa.atlassian.net/browse/SSQ-49)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-17 – Verify validation for invalid password (too short)
**Jira Test Case:** [SSQ-50](https://storyspoilerqa.atlassian.net/browse/SSQ-50)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Password must be between 6–30 characters.

---

## TC-REG-18 – Verify validation for invalid password (too long)
**Jira Test Case:** [SSQ-51](https://storyspoilerqa.atlassian.net/browse/SSQ-51)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-19 – Verify validation for invalid repeat password (mismatched)
**Jira Test Case:** [SSQ-52](https://storyspoilerqa.atlassian.net/browse/SSQ-52)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-20 – Verify validation for existing username reuse
**Jira Test Case:** [SSQ-53](https://storyspoilerqa.atlassian.net/browse/SSQ-53)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

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

---

## TC-REG-21 – Verify validation for existing email reuse
**Jira Test Case:** [SSQ-54](https://storyspoilerqa.atlassian.net/browse/SSQ-54)
**Use Case:** UC-REG-3 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. In the Username field, enter TD-07 (valid username).
4. In the Email field, enter TD-02 (invalid email, already existing).
5. In the First Name field, enter TD-14 (valid first name).
6. In the Middle Name field, enter TD-28 (empty middle name).
7. In the Last Name field, enter TD-17 (valid last name).
8. In the Password field, enter TD-20 (valid password).
9. In the Confirm Password field, repeat the password with TD-21.
10. Click “SIGN UP” button.

**Expected Result:**  
The user is prevented from completing the sign-up process. A clear validation message should be displayed indicating that the Email is already in use.

---

## TC-REG-22 – Verify "LOG IN HERE" button redirects to Log In page
**Jira Test Case:** [SSQ-55](https://storyspoilerqa.atlassian.net/browse/SSQ-55)
**Use Case:** UC-REG-4 (Jira: [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-33))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “SIGN UP” button in the navigation bar.
3. Click "LOG IN HERE" button at the bottom.

**Expected Result:**  
User is redirected to the Log In page.