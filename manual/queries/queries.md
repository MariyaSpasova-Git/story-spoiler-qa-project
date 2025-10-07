# Queries – Home Page

This document lists all open queries identified during requirements and test case analysis.
Each query has a unique ID (QRY-HP-XX), is linked to Jira, and references the related test case(s).
These issues are not strictly functional bugs but require clarification and alignment with stakeholders.
Screenshots are stored in the `docs/screenshots/` folder.

---

## QRY-HP-01 – Requirements for Home Page for logged in users lack visuals and detailed content specification

**Jira query:** [SSQ-27](https://storyspoilerqa.atlassian.net/browse/SSQ-27)  
**Related Test Case:** [TC-HP-08](../../tests/test-cases-home-page.md#tc-hp-08) (Jira: [SSQ-13](https://storyspoilerqa.atlassian.net/browse/SSQ-13))

**Description:**
The original requirement document for the **Home Page (Logged-in User)** is incomplete. It lacks visuals and detailed text specification. Without them, developers and testers cannot reliably build or validate the feature.

**Steps to Identify:**

1. Open the oiginal requirement document.
2. Navigate to the section "Home Page (Logged-in User)".

**Expected:**
The requirement should contain a clear visual alongside a detailed description of:

* Page title and welcome message
* Content and layout of the body
* Labels/icons for navigation (Home, Profile, etc.)

**Actual:**

* No visuals provided
* Text description is incomplete and ambiguous

**Status:** ⏳ Open

---

## QRY-HP-02 – Home Page for logged-in users navigation link label

**Jira Query:** [SSQ-28](https://storyspoilerqa.atlassian.net/browse/SSQ-28)  
**Related Test Case:** [TC-HP-11](../tests/test-cases-home-page.md#tc-hp-11) (Jira: [SSQ-16](https://storyspoilerqa.atlassian.net/browse/SSQ-16))

**Description:**
Original requirement document states the navigation bar should display “**StorySpoil**” (mixed case), but both the mockup and current implementation show “**STORYSPOIL**” (all caps).

**Steps to Identify:**

1. Open the original requirement document.
2. Compare with the attached mockup.
3. Verify the implemented navigation bar in the app.

**Expected:**
Text formatting should be consistent between requirement, design mockup, and implementation.

**Actual:**
Requirement text differs from both design and implementation.

**Status:** ⏳ Open

---

## QRY-REG-01 – Consistency of capitalization in field names

* **Jira Query ID:** [SSQ-59](https://storyspoilerqa.atlassian.net/browse/SSQ-59) 
* **Related Test Cases:** 
- TC-REG-20 (../tests/test-cases-home-page.md#tc-reg-20) (Jira: [SSQ-53](https://storyspoilerqa.atlassian.net/browse/SSQ-53))
- TC-REG-04 (../tests/test-cases-home-page.md#tc-reg-04) (Jira: [SSQ-40](https://storyspoilerqa.atlassian.net/browse/SSQ-40))

**Description:**
Error messages use inconsistent capitalization for field names (e.g., `"UserName already taken!"` vs. `"User name is required!"`).

**Steps to Identify:**

1. Open the app URL.
2. Navigate to Sign Up page.
3. In the Username field, enter duplicate (TD-02) or invalid (empty) usernames to trigger different validation messages.

**Expected Result:**
Error messages should follow a consistent capitalization style (e.g., “Username”).

**Actual Result:**
Field names are inconsistently capitalized across error messages.

**Screenshots:**
![QRY-REG-01-01](../../docs/screenshots/qry-reg-01-01.png)
![QRY-REG-01-02](../../docs/screenshots/qry-reg-01-02.png)

**Status:** ⏳ Open

---

## QRY-REG-02 – Extra bullet point before error messages

* **Jira Query ID:** [SSQ-60](https://storyspoilerqa.atlassian.net/browse/SSQ-60) 
* **Related Test Cases:** 
- TC-REG-20 (../tests/test-cases-home-page.md#tc-reg-20) (Jira: [SSQ-53](https://storyspoilerqa.atlassian.net/browse/SSQ-53))
- TC-REG-21 (../tests/test-cases-home-page.md#tc-reg-21) (Jira: [SSQ-40](https://storyspoilerqa.atlassian.net/browse/SSQ-54))

**Description:**
An unnecessary bullet point (“•”) is displayed before validation error messages when trying to sign up with an existing username or email.

- `"UserName already taken!"`
- `"User name is required!"`.

**Steps to Identify:**

1. Open the app URL.
2. Navigate to Sign Up page.
3. Enter existing username (TD-02) or existing email address (TD-29) to trigger validation messages.

**Expected Result:**
Error messages should display cleanly without bullet points.

**Actual Result:**
Error messages are preceded by an unnecessary bullet point.

**Status:** Open

---

## QUERY-REG-03 – Clarity of system-generated email validation error

* **Jira Query ID:** SSQ-63
* **Related Test Case ID:** TC-REG-04 (../tests/test-cases-home-page.md#tc-reg-04) (Jira: [SSQ-40](https://storyspoilerqa.atlassian.net/browse/SSQ-40))

**Description:**
System-generated email validation error reads:
`"Please include an '@' in the email address. The 'XXXX' is missing an 'a'."`

**Steps to Identify:**

1. Open the app URL.
2. Enter an invalid email format such as `testemail`.
3. Attempt to sign up.

**Expected Result:**
Error message should clearly and simply explain the invalid format (e.g., “Invalid email format. Please include an ‘@’ and a ‘.’”).

**Actual Result:**
Message may confuse users with wording like “missing an ‘a’.”

**Status:** Open

---

## QUERY-REG-04 – Consistency of required field messages

* **Jira Query ID:** SSQ-Q05
* **Related Test Case ID:** TC-REG-17
* **Jira Link:** [SSQ-Q05](https://your-jira-instance.atlassian.net/browse/SSQ-Q05)

**Description:**
Required field messages are inconsistent:

* `"User name is required!"`
* `"The e-mail is required!"`
* `"First name is required!"`
* `"The password is required!"`

**Steps to Identify:**
Trigger required field validation across different fields.

**Expected Result:**
Required messages should follow a consistent format (e.g., `"<Field> is required!"`).

**Actual Result:**
Some messages start with “The”, others don’t.

**Status:** Open

---

## QUERY-REG-05 – Tone and punctuation inonsistency

* **Jira Query ID:** SSQ-Q06
* **Related Test Case ID:** TC-REG-13, TC-REG-19, TC-REG-20
* **Jira Link:** [SSQ-Q06](https://your-jira-instance.atlassian.net/browse/SSQ-Q06)

**Description:**
Inconsistent punctuation:

* `"Password has to be at least 6 symbols!"` (exclamation mark).
* `"Passwords don't match."` (period).

**Steps to Identify:**
Trigger validation errors in password and confirm password fields.

**Expected Result:**
All error messages should use consistent punctuation.

**Actual Result:**
Error messages mix exclamation marks and periods.

**Status:** 

---

## QUERY-REG-06 – Label discrepancy for “Repeat Password” vs. “Confirm Password”

* **Jira Query:** [SSQ-59](https://storyspoilerqa.atlassian.net/browse/SSQ-59) 
* **Related Test Case ID:** TC-REG-01 (../tests/test-cases-user-registration.md#tc-reg-04) (Jira: [SSQ-34](https://storyspoilerqa.atlassian.net/browse/SSQ-34))

**Description:**
In the original requirements document, the field label is described as “Repeat password”, but the image shows “Confirm password”. The application also uses “Confirm password”.

**Steps to Identify:**

1. Open the original requirements document.
2. Navigate to the section Sign Up Page.
3. Compare the field label in the text vs. the image and application.

**Expected Result:**
There should be no inconsistency between requirement description, UI design, and app implementation.

**Actual Result:**
Requirements specify “Repeat password”, but design and app show “Confirm password”.

**Status:** ⏳ Open

---

## QUERY-REG-08 – Required field indicators not defined in requirements

* **Jira Query ID:** SSQ-Q08
* **Related Test Case ID:** TC-REG-17
* **Jira Link:** [SSQ-Q08](https://your-jira-instance.atlassian.net/browse/SSQ-Q08)

**Description:**
It is not mentioned in the SRS whether required fields should be visually marked. The app currently does not display required field indicators (e.g., red asterisk).

**Steps to Identify:**

1. Open the requirements document.
2. Navigate to **Sign Up Page**.
3. Compare field specifications with actual UI.

**Expected Result:**
Requirements should specify if required fields must be visually indicated.

**Actual Result:**
No indicators are defined or displayed.

**Status:** Open

---

## QUERY-REG-09 – Missing user flows for sign-up process in requirements

* **Jira Query ID:** SSQ-Q09
* **Related Test Case ID:** TC-REG-06 – TC-REG-25
* **Jira Link:** [SSQ-Q09](https://your-jira-instance.atlassian.net/browse/SSQ-Q09)

**Description:**
The requirements lack defined user flows for the sign-up process.

**Steps to Identify:**

1. Open the requirements document.
2. Navigate to **Sign Up Page**.

**Expected Result:**
The requirements should specify expected behavior for different flows (e.g., successful sign-up, failed sign-up, duplicate username, invalid email).

**Actual Result:**
User flows are not defined; expected behavior is unknown.

**Status:** Open

---

# Additional Queries – User Registration

These queries identify missing or unclear requirements discovered during the **User Registration** testing phase.
They are intended for clarification and alignment with stakeholders.

---

## QUERY-REG-10 – Missing character type constraints for all input fields

* **Jira Query ID:** SSQ-Q10
* **Related Test Case ID:** TC-REG-06 – TC-REG-25
* **Jira Link:** [SSQ-Q10](https://your-jira-instance.atlassian.net/browse/SSQ-Q10)

**Description:**
The SRS defines only the **minimum and maximum character lengths** for each registration field but does not specify **permitted or prohibited character types** (e.g., special characters, digits, spaces, symbols).

**Steps to Identify:**

1. Review the SRS sections “User Registration” and “Sign Up Page”.
2. Observe that no field-level constraints are mentioned for character types.
3. Compare with actual app behavior (fields accept a wide range of symbols and special characters).

**Expected Result:**
The requirements should specify which character types are allowed or disallowed for each field (e.g., only letters for names, alphanumeric for usernames, etc.).

**Actual Result:**
Only field length constraints are defined; no character-type restrictions are mentioned.

**Status:** Open

---

## QUERY-REG-11 – Missing user agreement or terms acceptance step

* **Jira Query ID:** SSQ-Q11
* **Related Test Case ID:** TC-REG-06 – TC-REG-25
* **Jira Link:** [SSQ-Q11](https://your-jira-instance.atlassian.net/browse/SSQ-Q11)

**Description:**
The **Sign Up form** does not include an option for users to agree to **Terms and Conditions** or **Privacy Policy**, nor is this requirement defined in the SRS.

**Steps to Identify:**

1. Open the app URL.
2. Navigate to **Sign Up Page**.
3. Observe that the registration form contains no checkbox or link for legal agreements.
4. Review the SRS “Sign Up Page” section for confirmation.

**Expected Result:**
Requirements and UI should include a step for users to explicitly agree to Terms of Service and Privacy Policy before account creation.

**Actual Result:**
No such checkbox or acceptance step exists in the current implementation or in the documented requirements.

**Status:** Open

---
