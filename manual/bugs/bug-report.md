# Bugs Report – Home Page

This file works in parallel with [queries/queries.md](../queries/queries.md).
It documents all identified bugs related to the Home Page requirements and use cases.
Each bug is linked to its corresponding Jira issue, GitHub test case(s), and screenshot evidence.

---

## BUG-HP-01 – Missing picture in "Upload a Picture" section

**Jira Bug:** [SSQ-25](https://storyspoilerqa.atlassian.net/browse/SSQ-25)  
**Related Test Case:**  [TC-HP-01](../test-cases/test-cases-home-page.md#tc-hp-01--verify-home-page-for-non-logged-in-users) (Jira link: [SSQ-6](https://storyspoilerqa.atlassian.net/browse/SSQ-6))

### Steps to Reproduce
1. Open the app URL.
2. Scroll to the "Upload a Picture" section on the Home Page.

### Expected Result
The section should display:
- Motivational phrase
- Short description
- Corresponding picture

### Actual Result
The picture is not displayed. Instead, the alt text `"uploading spoiler story picture"` appears.

### Severity
Medium – Content is incomplete, impacting user experience.

### Priority
Medium – Fix needed but not blocking core functionality.

### Status
Open

### Affected Areas
- Home Page (non-logged-in users)

### Screenshot
![BUG-HP-01](../../docs/screenshots/home-page/bug-hp-01.png)

---

## BUG-HP-02 – Copyright link in footer does not redirect

**Jira Bug:** [SSQ-26](https://storyspoilerqa.atlassian.net/browse/SSQ-26)  
**Related Test Cases:**  
- [TC-HP-07](../test-cases/test-cases-home-page.md#tc-hp-07--verify-copyright-link-in-footer-for-non-logged-in-users) (Jira link: [SSQ-12](https://storyspoilerqa.atlassian.net/browse/SSQ-12)) – Verify Copyright link in footer for non-logged-in users
- [TC-HP-15](../test-cases/test-cases-home-page.md#tc-hp-15--verify-copyright-link-in-footer-for-logged-in-users) – (Jira link: [SSQ-15](https://storyspoilerqa.atlassian.net/browse/SSQ-20)) - Verify Copyright link in footer for logged-in users

### Steps to Reproduce
1. Open the app URL.
2. Scroll to the footer.
3. Click the "StorySpoil" copyright link.

### Expected Result
User is redirected to the dedicated Copyright page.

### Actual Result
The page does not redirect. Instead, the screen scrolls to the top.

### Severity
Medium – Functionality issue that impacts compliance/UX but does not block core flows.  

### Priority
High – Affects all users across all pages where the footer appears.  

### Status
Open  

### Affected Areas
- Home Page (non-logged-in users)  
- Home Page (logged-in users)  
- Any page containing the footer component  

---

## BUG-REG-01 – Validation error message does not specify the correct email address format

**Jira Bug:** [SSQ-56](https://storyspoilerqa.atlassian.net/browse/SSQ-56)  
**Related Test Cases:**  
- [TC-REG-08](../test-cases/test-cases-user-registration.md#tc-reg-08--verify-validation-for-invalid-email-missing-) (Jira link: [SSQ-41](https://storyspoilerqa.atlassian.net/browse/SSQ-41))
- [TC-REG-07](../test-cases/test-cases-user-registration.md#tc-reg-07--verify-validation-for-invalid-email-missing-) (Jira link: [SSQ-37](https://storyspoilerqa.atlassian.net/browse/SSQ-37))

### Steps to Reproduce
1. Open the app URL.
2. Click the “SIGN UP” button in the navigation bar.
3. Enter an invalid email address such as `testemail` in the Email field.
4. Fill in all other required fields with valid test data (see TD-07, TD-14, TD-28, TD-17, TD-20, TD-21).
5. Click the “SIGN UP” button.

### Expected Result
A clear validation error message is displayed that specifies the correct email format, including the presence of an `"@"` and a `"."`.

### Actual Result
The validation error message only mentions the `"@"` requirement but does not specify the missing `"."`.

### Severity
Medium – User is prevented from registering, but the feedback is unclear, leading to confusion.

### Priority
High – Basic requirement for user registration; incorrect messaging blocks proper user guidance.

### Status
Open

### Affected Area
Registration form – Email field

### Screenshot
![BUG-REG-01](../../docs/screenshots/user-registration/bug-reg-01.png)

---

## BUG-REG-02 – User is able to sign up with an invalid email address missing a "."

**Jira Bug:** [SSQ-57](https://storyspoilerqa.atlassian.net/browse/SSQ-57)  
**Related Test Case: ** [TC-REG-08](../test-cases/test-cases-user-registration.md#tc-reg-08--verify-validation-for-invalid-email-missing-) (Jira link: [SSQ-41](https://storyspoilerqa.atlassian.net/browse/SSQ-41))


### Steps to Reproduce
1. Open the app URL.
2. Click the “SIGN UP” button in the navigation bar.
3. Enter an invalid email address without a `"."`, e.g., `test@examplecom`.
4. Fill in all other required fields with valid test data (see TD-07, TD-14, TD-28, TD-17, TD-20, TD-21).
5. Click the “SIGN UP” button.

### Expected Result
The user should not be able to complete the sign-up process. A clear validation error message should be displayed indicating that the email format is invalid.

### Actual Result
The user is successfully registered with an invalid email address. No error message is displayed.

### Severity
High – Invalid users/accounts can be created, leading to potential system integrity and communication issues.

### Priority
Critical – Must be fixed before release since it breaks the fundamental purpose of email-based registration.

### Status
Open

### Affected Area
Registration form – Email validation

### Screenshot
![BUG-REG-01](../../docs/screenshots/user-registration/bug-reg-01.png)


---

## BUG-REG-03 – User can sign up with a middle name below the minimum boundary

**Jira Bug:** [SSQ-58](https://storyspoilerqa.atlassian.net/browse/SSQ-58)  
**Related Test Case: ** [TC-REG-13](../test-cases/test-cases-user-registration.md#tc-reg-13--verify-validation-for-invalid-middle-name-too-short) (Jira link: [SSQ-46](https://storyspoilerqa.atlassian.net/browse/SSQ-46))


### Steps to Reproduce
1. Open the app URL.
2. Click the “SIGN UP” button in the navigation bar.
3. Enter a middle name of 1 character, such as `A`, in the Middle Name field.
4. Fill in all other required fields with valid test data (see TD-07, TD-09, TD-14, TD-17, TD-21).
5. Click the “SIGN UP” button.

### Expected Result
The user should not be able to create an account with a middle name shorter than 2 characters. A clear validation error message should be displayed indicating that the middle name must be between 2–60 characters.

### Actual Result
The user is able to create an account with a 1-character middle name. No error message is displayed.

### Severity
Low - Does not break registration flow, but violates requirement constraints and data integrity.

### Priority
Medium – Should be fixed, but less urgent than the email validation issue.

### Status
Open

### Affected Area
Registration form – Middle Name field


