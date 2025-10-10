# Test Cases – Log In Page

**Requirement Link:** [SSQ-71 – Log In Page](https://storyspoilerqa.atlassian.net/browse/SSQ-71)  

This file documents the 7 test cases for the **Log In Page** feature.  
Each test case is traceable to its corresponding **Use Case** and **Requirement** in Jira.  

---

## TC-LOG-01 – Verify Log In page
**Jira Test Case:** [SSQ-77](https://storyspoilerqa.atlassian.net/browse/SSQ-77)  
**Use Case:** [UC-LOG-1](../use-cases/use-cases-log-in-page.md#uc-log-1--access-log-in-page) (Jira: [SSQ-72](https://storyspoilerqa.atlassian.net/browse/SSQ-72))

**Prerequisites:** TD-01: Guest Session.

**Steps:**
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar. 
3. Observe the Log In page.

**Expected Result:**
The Log In page displays the following elements:
- Username input field
- Password input field
- LOG IN button
- Forgot Password? option
- Don't have an account? option with a CREATE NEW button

**Execution Result:** ✅ Passed

---

## TC-LOG-02 – Verify successful log-in with valid credentials
**Jira Test Case:** [SSQ-78](https://storyspoilerqa.atlassian.net/browse/SSQ-78)  
**Use Case:** [UC-LOG-2](../use-cases/use-cases-log-in-page.md#uc-log-2--log-in-with-valid-credentials) (Jira: [SSQ-73](https://storyspoilerqa.atlassian.net/browse/SSQ-73))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Open the app URL.
2. Click “LOG IN” button in the navigation bar.
3. In the Username field, enter the valid username from TD-02.
4. In the Password field, enter the valid password from TD-02.
5. Click “LOG IN” button.

**Expected Result:**  
The user successfully logs in and is redirected to the Home Page for logged-in users.

**Execution Result:** ✅ Passed

---

## TC-LOG-03 – Verify validation for required fields
**Jira Test Case:** [SSQ-79](https://storyspoilerqa.atlassian.net/browse/SSQ-79)  
**Use Case:** [UC-LOG-3](../use-cases/use-cases-log-in-page.md#uc-log-3--validation-errors-for-invalid-credentials) (Jira: [SSQ-74](https://storyspoilerqa.atlassian.net/browse/SSQ-74))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Leave the Username and Password fields empty (TD-31).
4. Click “LOG IN” button.

**Expected Result:**  
User is not logged in. Validation errors are displayed for both Username and Password fields. Each field shows a clear, user-friendly message indicating that it is required.

**Execution Result:** ✅ Passed

**Related Queries:** 
- [QRY-LOG-01](../queries/queries.md#qry-log-01--extra-bullet-point-before-unable-to-sign-in-error-message-1) (Jira: [SSQ-84](https://storyspoilerqa.atlassian.net/browse/SSQ-84))
- [QRY-LOG-02](../queries/queries.md#qry-log-02--consistency-of-required-field-messages) (Jira: [SSQ-85](https://storyspoilerqa.atlassian.net/browse/SSQ-85))

---

## TC-LOG-04 – Verify validation for invalid username
**Jira Test Case:** [SSQ-80](https://storyspoilerqa.atlassian.net/browse/SSQ-80)  
**Use Case:** [UC-LOG-3](../use-cases/use-cases-log-in-page.md#uc-log-3--validation-errors-for-invalid-credentials) (Jira: [SSQ-74](https://storyspoilerqa.atlassian.net/browse/SSQ-74))

**Prerequisites:** TD-04: Invalid user (invalid username, valid password)

**Steps:**  
1. Open the app URL.
2. Click “LOG IN” button in the navigation bar.
3. In the Username field, enter the invalid username from TD-04.
4. In the Password field, enter the valid password from TD-04.
5. Click “LOG IN” button.

**Expected Result:**  
User remains on the Log In page. A clear error message should be displayed indicating that the username/password is incorrect.

**Execution Result:** ✅ Passed

**Related Queries:** 
- [QRY-LOG-01](../queries/queries.md#qry-log-01--extra-bullet-point-before-unable-to-sign-in-error-message-1) (Jira: [SSQ-84](https://storyspoilerqa.atlassian.net/browse/SSQ-84))
- [QRY-LOG-03](../queries/queries.md#qry-log-03--generic-error-message-for-invalid-login-credentials) (Jira: [SSQ-86](https://storyspoilerqa.atlassian.net/browse/SSQ-86))

---

## TC-LOG-05 – Verify validation for invalid password
**Jira Test Case:** [SSQ-81](https://storyspoilerqa.atlassian.net/browse/SSQ-81)  
**Use Case:** [UC-LOG-3](../use-cases/use-cases-log-in-page.md#uc-log-3--validation-errors-for-invalid-credentials) (Jira: [SSQ-74](https://storyspoilerqa.atlassian.net/browse/SSQ-74))

**Prerequisites:** TD-30: Invalid user (valid username, invalid password)

**Steps:**  
1. Open the app URL.
2. Click “LOG IN” button in the navigation bar.
3. In the Username field, enter the valid username from TD-30.
4. In the Password field, enter the invalid password from TD-30.
5. Click “LOG IN” button.

**Expected Result:**  
User remains on the Log In page. A clear error message should be displayed indicating that the username/password is incorrect.

**Execution Result:** ✅ Passed

**Related Queries:** 
- [QRY-LOG-01](../queries/queries.md#qry-log-01--extra-bullet-point-before-unable-to-sign-in-error-message-1) (Jira: [SSQ-84](https://storyspoilerqa.atlassian.net/browse/SSQ-84))
- [QRY-LOG-03](../queries/queries.md#qry-log-03--generic-error-message-for-invalid-login-credentials) (Jira: [SSQ-86](https://storyspoilerqa.atlassian.net/browse/SSQ-86))

---

## TC-LOG-06 – Verify "Forgot password?" link redirects to Restore Password page
**Jira Test Case:** [SSQ-82](https://storyspoilerqa.atlassian.net/browse/SSQ-82)  
**Use Case:** [UC-LOG-4](../use-cases/use-cases-log-in-page.md#uc-log-4--redirect-to-forgot-password-page) (Jira: [SSQ-75](https://storyspoilerqa.atlassian.net/browse/SSQ-75))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Click "Forgot Password?" link.

**Expected Result:**  
User is redirected to the Restore Password page.

**Execution Result:** ❌ Failed

**Related Bug:** [BUG-LOG-01](../bugs/bug-report.md#bug-log-01--forgot-password-link-redirects-to-home-page-instead-of-restore-password-page) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

---

## TC-LOG-06 – Verify "CREATE NEW" button redirects to Sign Up page
**Jira Test Case:** [SSQ-83](https://storyspoilerqa.atlassian.net/browse/SSQ-83)  
**Use Case:** [UC-LOG-5](../use-cases/use-cases-log-in-page.md#uc-log-5--redirect-to-sign-up-page) (Jira: [SSQ-76](https://storyspoilerqa.atlassian.net/browse/SSQ-76))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Open the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Click "CREATE NEW" button.

**Expected Result:**  
User is redirected to the Sign Up page.
