# 🐞 Bug Report

## Overview

This file documents all identified bugs identified during the Manual Testing Phase of the Story Spoiler web application related to requirements, use case and test case analysis.
It works in parallel with [queries/queries.md](../queries/queries.md).
Each bug has a unique ID (BUG-XX-XX), is linked to its corresponding Jira issue, GitHub test case(s), and screenshot evidence.
Screenshots are stored in the `docs/screenshots/` folder. All usernames, emails, and other data displayed in screenshots are dummy test data used solely for QA and educational purposes

> ⚠️ Note: Screenshots or excerpts from the original requirements document are omitted due to copyright restrictions. Related issues are described textually without reproducing protected material.

---

## 🧪 Detailed Bug List

### 🏠 Home Page

#### BUG-HP-01 – Missing picture in "Upload a Picture" section
**Jira Bug:** [SSQ-25](https://storyspoilerqa.atlassian.net/browse/SSQ-25)  
**Related Test Case:** [TC-HP-01](../test-cases/test-cases-home-page.md#tc-hp-01--verify-home-page-for-non-logged-in-users) (Jira [SSQ-6](https://storyspoilerqa.atlassian.net/browse/SSQ-6))
- **Severity:** Medium  
- **Priority:** Medium  
- **Status:** Open  
- **Affected Area:** Home Page (non-logged-in users)

**Steps to Reproduce:**
1. Open the app URL.  
2. Scroll to the "Upload a Picture" section.  

**Expected Result:** 
The section should display:
- Motivational phrase
- Short description
- Corresponding picture

**Actual Result:** 
The picture is not displayed. Instead, the alt text `"uploading spoiler story picture"` appears.

**Screenshot:**  
![Missing Picture](../../docs/screenshots/home-page/bug-hp-01-missing-picture.png)

---

#### BUG-HP-02 – Copyright link in footer does not redirect
**Jira Bug:** [SSQ-26](https://storyspoilerqa.atlassian.net/browse/SSQ-26)  
**Related Test Cases:** [TC-HP-07](../test-cases/test-cases-home-page.md#tc-hp-07--verify-copyright-link-in-footer-for-non-logged-in-users) (Jira [SSQ-12](https://storyspoilerqa.atlassian.net/browse/SSQ-12)), [TC-HP-15](../test-cases/test-cases-home-page.md#tc-hp-15--verify-copyright-link-in-footer-for-logged-in-users) (Jira [SSQ-15](https://storyspoilerqa.atlassian.net/browse/SSQ-20))

- **Severity:** Medium  
- **Priority:** High  
- **Status:** Open  
- **Affected Areas:** All pages

**Steps to Reproduce:**
1. Open the app URL.
2. Scroll to the footer.
3. Click the "StorySpoil" copyright link.

**Expected Result:** 
The user is redirected to the dedicated Copyright page.

**Actual Result:** 
The page does not redirect. Instead, the screen scrolls to top of the page.

**Note:** This issue occurs on all pages (both logged-in and non-logged-in views). However, it was verified and documented through two representative test cases to avoid redundancy.

**Screenshots:**  
![Footer Link Before Click](../../docs/screenshots/screenshots-home-page/bug-hp-02-01-footer-link-before-click.png)  
![No Redirect After Click](../../docs/screenshots/screenshots-home-page/bug-hp-02-02-no-redirect-after-click.png)

---

### 🧍‍♀️ User Registration

#### BUG-REG-01 – Validation error message does not specify the correct email address format
**Jira Bug:** [SSQ-56](https://storyspoilerqa.atlassian.net/browse/SSQ-56)  
**Related Test Case:** [TC-REG-08](../test-cases/test-cases-user-registration.md#tc-reg-08--verify-validation-for-invalid-email-missing-) (Jira [SSQ-41](https://storyspoilerqa.atlassian.net/browse/SSQ-41))
- **Severity:** Medium  
- **Priority:** High  
- **Status:** Open  
- **Affected Area:** Registration form – Email field

**Steps to Reproduce:**
1. Open the app URL.
2. Click the “SIGN UP” button in the navigation bar.
3. In the Email field, enter TD-30 (invalid email, missing '@' and '.').
4. Fill in all other required fields with valid test data (see TD-07, TD-14, TD-28, TD-17, TD-20, TD-21).
5. Click the “SIGN UP” button.

**Expected Result:** 
A clear validation error message is displayed that specifies the correct email format, including the presence of an `"@"` and a `"."`.

**Actual Result:** 
The validation error message only mentions the `"@"` requirement but does not specify the missing `"."`.

**Screenshot:**  
![Incorrect Email Validation Error](../../docs/screenshots/user-registration/bug-reg-01-incorrect-email-validation-error.png)

---

#### BUG-REG-02 – User is able to sign up with an invalid email address missing a "."
**Jira Bug:** [SSQ-57](https://storyspoilerqa.atlassian.net/browse/SSQ-57)  
**Related Test Case:** [TC-REG-08](../test-cases/test-cases-user-registration.md#tc-reg-08--verify-validation-for-invalid-email-missing-) (Jira [SSQ-41](https://storyspoilerqa.atlassian.net/browse/SSQ-41))
- **Severity:** High  
- **Priority:** Critical 
- **Status:** Open  
- **Affected Area:** Registration form – Email validation

**Steps to Reproduce:**
1. Open the app URL.
2. Click the “SIGN UP” button in the navigation bar.
3. In the Email field, enter TD-11 (invalid email, missing `"."`).
4. Fill in all other required fields with valid test data (see TD-07, TD-14, TD-28, TD-17, TD-20, TD-21).
5. Click the “SIGN UP” button.

**Expected Result:** 
The user should not be able to complete the sign-up process. A clear validation error message should be displayed indicating that the email format is invalid.

**Actual Result:** 
The user is successfully registered with an invalid email address. No error message is displayed.

**Screenshots:**  
![Form Before Submit](../../docs/screenshots/user-registration/bug-reg-02-form-before-submit.png)  
![Successful Login After Registration](../../docs/screenshots/user-registration/bug-reg-02-successful-login-after-registration.png)

---

#### BUG-REG-03 – User can sign up with a middle name below the minimum boundary
**Jira Bug:** [SSQ-58](https://storyspoilerqa.atlassian.net/browse/SSQ-58)   
**Related Test Case:** [TC-REG-13](../test-cases/test-cases-user-registration.md#tc-reg-13--verify-validation-for-invalid-middle-name-too-short) (Jira [SSQ-46](https://storyspoilerqa.atlassian.net/browse/SSQ-46))
- **Severity:** Low
- **Priority:** Medium
- **Status:** Open  
- **Affected Areas:** Registration form – Middle Name field

**Steps to Reproduce:**
1. Open the app URL.
2. Click the "SIGN UP" button in the navigation bar.
3. In the Middle Name field, enter TD-25 (invalid middle name, too short).
4. Fill in all other required fields with valid test data (see TD-07, TD-09, TD-14, TD-17, TD-21).
5. Click the "SIGN UP" button.

**Expected Result:** 
The user should not be able to create an account with a middle name shorter than 2 characters. A clear validation error message should be displayed indicating that the middle name must be at least 2 characters.

**Actual Result:** 
The user is able to create an account with a 1-character middle name. No error message is displayed.

**Screenshots:**  
![Form Before Submit](../../docs/screenshots/user-registration/bug-reg-03-form-before-submit.png)  
![Successful Login After Registration](../../docs/screenshots/user-registration/bug-reg-03-successful-login-after-registration.png)

---

#### BUG-REG-04 – Incorrect field reference in Last Name validation
**Jira Bug:** [SSQ-70](https://storyspoilerqa.atlassian.net/browse/SSQ-70)  
**Related Test Case:** [TC-REG-15](../test-cases/test-cases-user-registration.md#tc-reg-15--verify-validation-for-invalid-last-name-too-short) (Jira[SSQ-48](https://storyspoilerqa.atlassian.net/browse/SSQ-48))
- **Severity:** Medium
- **Priority:** High
- **Status:** Open  
- **Affected Areas:** Registration form – Last Name field validation

**Steps to Reproduce:**
1. Open the app URL.
2. Click the “SIGN UP” button in the navigation bar.
3. In the Last Name field, enter TD-18 (invalid last name, too short). 
4. Fill in all other required fields with valid test data (see TD-07, TD-09, TD-14, TD-20, TD-21).
5. Click the “SIGN UP” button.

**Expected Result:** 
A clear validation error message should be displayed indicating that the last name must be at least 2 characters.

**Actual Result:** 
An error message appears under the Last Name field: `"First name has to be at least 2 symbols!"`.

**Screenshot:**  
![Invalid Last Name Error](../../docs/screenshots/screenshots-user-registration/bug-reg-04-invalid-last-name-error.png)

---

### 🔑 Log In

#### BUG-LOG-01 – “Forgot Password?” link redirects to Home Page instead of Restore Password
**Jira Bug:** [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87)  
**Related Test Case:** [TC-LOG-06](../test-cases/test-cases-user-registration.md#tc-log-06--verify-create-new-button-redirects-to-sign-up-paget) (Jira[SSQ-82](https://storyspoilerqa.atlassian.net/browse/SSQ-82))
- **Severity:** High  
- **Priority:** High  
- **Status:** Open  
- **Affected Area:** Log In page  

**Steps to Reproduce**
1. Open the app URL.  
2. Click the "LOG IN" button in the navigation bar.  
3. Click "Forgot Password?" link.

**Expected Result:**
The user is redirected to the Restore Password page.

**Actual Result:** 
The user is redirected to the Home page.

**Screenshots:**  
![Forgot Password Link Before Click](../../docs/screenshots/screenshots-log-in-page/bug-log-01-01-forgot-password-link-before-click.png)  
![Wrong Redirect After Click](../../docs/screenshots/screenshots-log-in-page/bug-log-01-02-wrong-redirect-after-click.png)

---

### 👤 Profile Management

#### BUG-PROF-01 – “EDIT” button does not open Edit Profile Info page
**Jira Bug:** [SSQ-99](https://storyspoilerqa.atlassian.net/browse/SSQ-99)  
**Related Test Cases:** [TC-PROF-03](../test-cases/test-cases-user-profile-management.md#tc-prof-03--verify-edit-button-redirects-to-edit-profile-info-page) (Jira [SSQ-95](https://storyspoilerqa.atlassian.net/browse/SSQ-95)), [TC-PROF-04](../test-cases/test-cases-user-profile-management.md#tc-prof-04--verify-edit-profile-info-page) (Jira [SSQ-101](https://storyspoilerqa.atlassian.net/browse/SSQ-101)), [TC-PROF-05](../test-cases/test-cases-user-profile-management.md#tc-prof-05--verify-profile-edit-with-valid-data) (Jira [SSQ-96](https://storyspoilerqa.atlassian.net/browse/SSQ-96)), [TC-PROF-06](../test-cases/test-cases-user-profile-management.md#tc-prof-06--verify-required-fields-validation-when-all-fields-are-empty) (Jira [SSQ-97](https://storyspoilerqa.atlassian.net/browse/SSQ-97)), [TC-PROF-07](../test-cases/test-cases-user-profile-management.md#tc-prof-07--verify-minimum-length-validation-when-editing) (Jira [SSQ-102](https://storyspoilerqa.atlassian.net/browse/SSQ-102)), [TC-PROF-08](../test-cases/test-cases-user-profile-management.md#tc-prof-08--verify-maximum-length-validation-when-editing-the-first-name-field) (Jira [SSQ-103](https://storyspoilerqa.atlassian.net/browse/SSQ-103)), [TC-PROF-09](../test-cases/test-cases-user-profile-management.md#tc-prof-09--verify-minimum-length-validation-when-editing-the-middle-name-field) (Jira [SSQ-104](https://storyspoilerqa.atlassian.net/browse/SSQ-104)), [TC-PROF-10](../test-cases/test-cases-user-profile-management.md#tc-prof-10--verify-maximum-length-validation-when-editing-the-middle-name-field) (Jira [SSQ-105](https://storyspoilerqa.atlassian.net/browse/SSQ-105)), [TC-PROF-11](../test-cases/test-cases-user-profile-management.md#tc-prof-11--verify-minimum-length-validation-when-editing-the-last-name-field) (Jira [SSQ-106](https://storyspoilerqa.atlassian.net/browse/SSQ-106)), [TC-PROF-12](../test-cases/test-cases-user-profile-management.md#tc-prof-12--verify-maximum-length-validation-when-editing-the-last-name-field) (Jira [SSQ-107](https://storyspoilerqa.atlassian.net/browse/SSQ-107)), [TC-PROF-13](../test-cases/test-cases-user-profile-management.md#tc-prof-13--verify-maximum-length-validation-when-editing-the-about-me-field) (Jira [SSQ-108](https://storyspoilerqa.atlassian.net/browse/SSQ-108)), [TC-PROF-14](../test-cases/test-cases-user-profile-management.md#tc-prof-14--verify-validation-for-profile-picture-field-with-invalid-url-missing-protocol) (Jira [SSQ-109](https://storyspoilerqa.atlassian.net/browse/SSQ-109)), [TC-PROF-15](../test-cases/test-cases-user-profile-management.md#tc-prof-15--verify-validation-for-profile-picture-field-with-invalid-url-missing-file-extension) (Jira [SSQ-110](https://storyspoilerqa.atlassian.net/browse/SSQ-110)), [TC-PROF-16](../test-cases/test-cases-user-profile-management.md#tc-prof-16--verify-validation-for-profile-picture-field-with-invalid-url-wrong-extension) (Jira [SSQ-111](https://storyspoilerqa.atlassian.net/browse/SSQ-111)), [TC-PROF-17](../test-cases/test-cases-user-profile-management.md#tc-prof-17--verify-validation-for-profile-picture-field-with-invalid-url-invalid-url-structure) (Jira [SSQ-112](https://storyspoilerqa.atlassian.net/browse/SSQ-112))
- **Severity:** Blocking  
- **Priority:** High  
- **Affected Areas:** My Profile and Edit Profile Info pages

**Steps to Reproduce**
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click “EDIT” button.

**Expected Result:** 
The user is redirected to the Edit Profile Info page.

**Actual Result:**
The “EDIT” button does not perform any action. The user remains on the My Profile page; the Edit Profile Info page is not accessible.

**Screenshot:**  
![Edit Button Not Working](../../docs/screenshots/screenshots-user-profile-management/bug-prof-01-edit-button-not-working.png)

---

### 💬 Spoiler Management

#### BUG-SM-01 – Missing “SHARE” button for created spoilers on Home Page
**Jira Bug:** [SSQ-158](https://storyspoilerqa.atlassian.net/browse/SSQ-158)  
**Related Test Cases:** [TC-SM-01](../test-cases/test-cases-spoiler-management.md#tc-sm-01--verify-spoiler-list-and-functional-buttons-on-home-page) (Jira [SSQ-138](https://storyspoilerqa.atlassian.net/browse/SSQ-138)), [TC-SM-04](../test-cases/test-cases-spoiler-management.md#tc-sm-04--verify-share-spoiler-page) (Jira [SSQ-141](https://storyspoilerqa.atlassian.net/browse/SSQ-141)), [TC-SM-05](../test-cases/test-cases-spoiler-management.md#tc-sm-05--verify-spoiler-sharing-with-valid-data) (Jira [SSQ-142](https://storyspoilerqa.atlassian.net/browse/SSQ-142)), [TC-SM-06](../test-cases/test-cases-spoiler-management.md#tc-sm-06--verify-maximum-length-validation-for-message) (Jira [SSQ-168](https://storyspoilerqa.atlassian.net/browse/SSQ-168)), [TC-SM-07](../test-cases/test-cases-spoiler-management.md#tc-sm-07--verify-maximum-length-validation-for-name) (Jira [SSQ-169](https://storyspoilerqa.atlassian.net/browse/SSQ-169)), [TC-SM-08](../test-cases/test-cases-spoiler-management.md#tc-sm-08--verify-validation-for-invalid-email-missing-e) (Jira [SSQ-143](https://storyspoilerqa.atlassian.net/browse/SSQ-143)), [TC-SM-09](../test-cases/test-cases-spoiler-management.md#tc-sm-09--verify-validation-for-invalid-email-missing-) (Jira [SSQ-144](https://storyspoilerqa.atlassian.net/browse/SSQ-144)), [TC-SM-10](../test-cases/test-cases-spoiler-management.md#tc-sm-10--verify-validation-for-invalid-email-missing--and-) (Jira [SSQ-145](https://storyspoilerqa.atlassian.net/browse/SSQ-145)), [TC-SM-11](../test-cases/test-cases-spoiler-management.md#tc-sm-11--verify-validation-for-invalid-email-extra-spaces) (Jira [SSQ-146](https://storyspoilerqa.atlassian.net/browse/SSQ-146)), [TC-SM-12](../test-cases/test-cases-spoiler-management.md#tc-sm-12--verify-validation-for-empty-email-field) (Jira [SSQ-147](https://storyspoilerqa.atlassian.net/browse/SSQ-147)), [TC-SM-13](../test-cases/test-cases-spoiler-management.md#tc-sm-13--verify-validation-for-invalid-email-missing-username) (Jira [SSQ-148](https://storyspoilerqa.atlassian.net/browse/SSQ-148)), [TC-SM-14](../test-cases/test-cases-spoiler-management.md#tc-sm-14--verify-validation-for-invalid-email-missing-domain-name) (Jira [SSQ-149](https://storyspoilerqa.atlassian.net/browse/SSQ-149)), [TC-SM-15](../test-cases/test-cases-spoiler-management.md#tc-sm-15--verify-validation-for-invalid-email-missing-host) (Jira [SSQ-150](https://storyspoilerqa.atlassian.net/browse/SSQ-150)), [TC-SM-16](../test-cases/test-cases-spoiler-management.md#tc-sm-16--verify-validation-for-invalid-email-multiple--symbols) (Jira [SSQ-151](https://storyspoilerqa.atlassian.net/browse/SSQ-151))
- **Severity:** High  
- **Priority:** High  
- **Status:** Open  
- **Affected Areas:** Home Page (Logged-in Users) and Spoiler Management (Edit functionality)

**Steps to Reproduce**
1. Open the app URL.
2. Click the "LOG IN" button in the navigation bar.  
3. Enter valid credentials (username and password) from TD-02.
4. Observe the list of spoilers displayed on the Home Page.

**Expected Result:** 
Each spoiler should have “SHARE”, “EDIT”, and “DELETE” buttons.  

**Actual Result:** 
The “SHARE” button is missing.

**Screenshot:**  
![Missing SHARE Button](../../docs/screenshots/screenshots-spoiler-management/bug-sm-01-missing-share-button.png)

---

#### BUG-SM-02 – Search functionality not working (no action on input or button click)
**Jira Bug:** [SSQ-170](https://storyspoilerqa.atlassian.net/browse/SSQ-170)  
**Related Test Cases:** [TC-SM-29](../test-cases/test-cases-spoiler-management.md#tc-sm-29--verify-that-write-spoiler-button-redirects-to-the-create-spoiler-page) (Jira [SSQ-155](https://storyspoilerqa.atlassian.net/browse/SSQ-155)), [TC-SM-30](../test-cases/test-cases-spoiler-management.md#tc-sm-30--verify-search-functionality-displays-matching-spoilers) (Jira [SSQ-156](https://storyspoilerqa.atlassian.net/browse/SSQ-156)), [TC-SM-31](../test-cases/test-cases-spoiler-management.md#tc-sm-31--verify-search-returns-no-results-for-non-existing-titles) (Jira [SSQ-157](https://storyspoilerqa.atlassian.net/browse/SSQ-157))
- **Severity:** High  
- **Priority:** High  
- **Status:** Open
- **Affected Areas:** Home Page (Logged-in Users) page and Spoiler Management (search functionality)

**Steps to Reproduce:**
1. Open the app URL.  
2. Click the "LOG IN" button in the navigation bar.  
3. Enter valid credentials (username and password) from TD-02.  
4. Locate the Search field on the Home Page.  
5. Enter any search term — either a matching or non-matching keyword.  
6. Press Enter or click the Search button.

**Expected Result:**
The system should:
- Display a list of spoilers that match the search term (for matching input).  
- Show a "There are no spoilers :(" message (for non-matching input).  
- Indicate that the search action has been processed (e.g., spinner or filtered list). 

**Actual Result:** 
- No action occurs after pressing Enter or clicking the Search button.  
- The list of spoilers remains unchanged.  
- No feedback or error message is displayed.

**Screenshots:**  
![Before - Matching Input Entered](../../docs/screenshots/spoiler-management/bug-sm-02-01-matching-input-entered.png)  
![After - No Result Matching Input](../../docs/screenshots/spoiler-management/bug-sm-02-02-no-result-matching-input.png)  
![Before - Non-Matching Input Entered](../../docs/screenshots/spoiler-management/bug-sm-02-03-non-matching-input-entered.png)  
![After - No Result Non-Matching Input](../../docs/screenshots/spoiler-management/bug-sm-02-04-no-result-non-matching-input.png)

---

## 🧾 Summary

✅ **9 total bugs logged** across **5 functional areas**.  
💡 The **Registration module** has the highest defect count (4), primarily validation-related.  
🔥 **Search and Edit Profile** bugs are considered **high priority**, as they impact key user actions.  

---

> 🧠 *All issues are tracked in Jira, linked to corresponding Test Cases for traceability. This file provides a static reference within the GitHub repository for portfolio purposes.*