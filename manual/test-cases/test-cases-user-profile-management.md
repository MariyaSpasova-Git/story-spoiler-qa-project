# Test Cases – User Profile Management

**Requirement Link:** [SSQ-88 – User Profile Management](https://storyspoilerqa.atlassian.net/browse/SSQ-88)  

This file documents the 7 test cases for the **Profile Management** feature.  
Each test case is traceable to its corresponding **Use Case** and **Requirement** in Jira.  

---

## TC-PROF-01 – Verify My Profile page
**Jira Test Case:** [SSQ-92](https://storyspoilerqa.atlassian.net/browse/SSQ-92)  
**Use Case:** [UC-PROF-1](../use-cases/use-cases-user-profile-management.md#uc-prof-1--access-my-profile-page) (Jira: [SSQ-89](https://storyspoilerqa.atlassian.net/browse/SSQ-89))

**Prerequisites:** TD-02: Valid user.

**Steps:**
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Observe the My Profile page.

**Expected Result:**
The My Profile page displays the following sections:  
- Profile section (left): Profile picture, Username, and “EDIT” button.  
- User’s attributes section (top-right): Full Name, Email, and Total spoilers counter.  
- About Me section (below attributes): Displays default or user-entered description.

**Execution Result:** ✅ Passed

---

## TC-PROF-02 – Verify My Profile page default values for a new user
**Jira Test Case:** [SSQ-93](https://storyspoilerqa.atlassian.net/browse/SSQ-93)  
**Use Case:** [UC-PROF-1](../use-cases/use-cases-user-profile-management.md#uc-prof-1--access-my-profile-page) (Jira: [SSQ-89](https://storyspoilerqa.atlassian.net/browse/SSQ-89))

**Prerequisites:** TD-03: Valid new user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Observe the My Profile page.

**Expected Result:**  
The My Profile page displays the following default values:  
- Profile section: Empty profile picture placeholder and correct Username.  
- User’s attributes section: Correct Full Name and Email, Total spoilers counter = “0”.  
- About Me section: Displays placeholder text “You haven’t written anything about yourself…”.

**Execution Result:** ✅ Passed

---

## TC-PROF-03 – Verify “EDIT” button redirects to Edit Profile Info page
**Jira Test Case:** [SSQ-95](https://storyspoilerqa.atlassian.net/browse/SSQ-95)  
**Use Case:** [UC-PROF-2](../use-cases/use-cases-user-profile-management.md#uc-prof-2--redirect-to-edit-profile-info-page) (Jira: [SSQ-98](https://storyspoilerqa.atlassian.net/browse/SSQ-98))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button.

**Expected Result:**  
User is redirected to the Edit Profile Info page.

**Execution Result:** ❌ Failed

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Related Query:** [QRY-UX-02](../queries/queries.md#XXXX) (Jira: [SSQ-61](https://storyspoilerqa.atlassian.net/browse/SSQ-61))

---

## TC-PROF-04 – Verify Edit Profile Info page
**Jira Test Case:** [SSQ-101](https://storyspoilerqa.atlassian.net/browse/SSQ-101)  
**Use Case:** [UC-PROF-3](../use-cases/use-cases-user-profile-management.md#XXX) (Jira: [SSQ-100](https://storyspoilerqa.atlassian.net/browse/SSQ-100))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. Observe the Edit Profile Info page.

**Expected Result:**  
The Edit Profile Info page displays the following elements:
- First Name input field
- Middle Name input field
- Last Name input field
- About me input field
- Profile picture input field
- “ADD” button

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-05 – Verify profile edit with valid data
**Jira Test Case:** [SSQ-96](https://storyspoilerqa.atlassian.net/browse/SSQ-96)  
**Use Case:** [UC-PROF-4](../use-cases/use-cases-user-profile-management.md#XXXXe) (Jira: [SSQ-90](https://storyspoilerqa.atlassian.net/browse/SSQ-90))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click "LOG IN" button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, enter TD-14 (valid first name).
7. In the Middle Name field, enter TD-27 (valid middle name).
8. In the Last Name field, enter TD-17 (valid last name).
9. In the About me field, enter TD-35 (valid description).
10. In the Profile picture field, enter TD-32 (valid picture URL).
11. Click "ADD" button.

**Expected Result:**  
Profile information is updated successfully. User is redirected to the My Profile page, where the updated data is displayed.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-06 – Verify required fields validation when all fields are empty
**Jira Test Case:** [SSQ-97](https://storyspoilerqa.atlassian.net/browse/SSQ-97)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. On the Edit Profile Info page, leave all fields empty.
7. Click “ADD” button. 

**Expected Result:**  
Clear and consistent validation messages are displayed for each required field (First Name and Last Name). Optional fields (Middle Name, About me, and Profile picture) do not trigger errors.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-07 – Verify minimum length validation when editing the First Name field
**Jira Test Case:** [SSQ-102](https://storyspoilerqa.atlassian.net/browse/SSQ-102)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, enter TD-15 (invalid first name, too short).
7. In the Middle Name field, enter TD-27 (valid middle name).
8. In the Last Name field, enter TD-17 (valid last name).
9. In the About me field, enter TD-35 (valid description).
10. In the Profile picture field, enter TD-32 (valid picture URL).
11. Click “ADD” button.

**Expected Result:**  
User is prevented from completing the editing process. A clear validation message should be displayed indicating that the First Name must be at least 2 characters.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-08 – Verify maximum length validation when editing the First Name field
**Jira Test Case:** [SSQ-103](https://storyspoilerqa.atlassian.net/browse/SSQ-103)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, attempt to enter TD-16 (invalid first name, too long).
7. In the Middle Name field, enter TD-27 (valid middle name).
8. In the Last Name field, enter TD-17 (valid last name).
9. In the About me field, enter TD-35 (valid description).
10. In the Profile picture field, enter TD-32 (valid picture URL).
11. Click “ADD” button.

**Expected Result:**  
User cannot complete the editing process with a value exceeding the maximum length. The field enforces the 60-character limit by preventing additional input.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-09 – Verify minimum length validation when editing the Middle Name field
**Jira Test Case:** [SSQ-104](https://storyspoilerqa.atlassian.net/browse/SSQ-104)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, enter TD-14 (valid first name).
7. In the Middle Name field, enter TD-25 (invalid middle name, too short).
8. In the Last Name field, enter TD-17 (valid last name).
9. In the About me field, enter TD-35 (valid description).
10. In the Profile picture field, enter TD-32 (valid picture URL).
11. Click “ADD” button.

**Expected Result:**  
User is prevented from completing the editing process. A clear validation message should be displayed indicating that the Middle Name must be at least 2 characters.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-10 – Verify maximum length validation when editing the Middle Name field
**Jira Test Case:** [SSQ-105](https://storyspoilerqa.atlassian.net/browse/SSQ-105)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, enter TD-14 (valid first name).
7. In the Middle Name field, attempt to enter TD-26 (invalid middle name, too long).
8. In the Last Name field, enter TD-17 (valid last name).
9. In the About me field, enter TD-35 (valid description).
10. In the Profile picture field, enter TD-32 (valid picture URL).
11. Click “ADD” button.

**Expected Result:**  
User cannot complete the editing process with a value exceeding the maximum length. The field enforces the 60-character limit by preventing additional input.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-11 – Verify minimum length validation when editing the Last Name field
**Jira Test Case:** [SSQ-106](https://storyspoilerqa.atlassian.net/browse/SSQ-106)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, enter TD-14 (valid first name).
7. In the Middle Name field, enter TD-27 (valid middle name).
8. In the Last Name field, enter TD-18 (invalid last name, too short).
9. In the About me field, enter TD-35 (valid description).
10. In the Profile picture field, enter TD-32 (valid picture URL).
11. Click “ADD” button.

**Expected Result:**  
User is prevented from completing the editing process. A clear validation message should be displayed indicating that the Last Name must be at least 2 characters.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-12 – Verify maximum length validation when editing the Last Name field
**Jira Test Case:** [SSQ-107](https://storyspoilerqa.atlassian.net/browse/SSQ-107)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, enter TD-14 (valid first name).
7. In the Middle Name field, enter TD-27 (valid middle name).
8. In the Last Name field, attempt to enter TD-19 (invalid last name, too long).
9. In the About me field, enter TD-35 (valid description).
10. In the Profile picture field, enter TD-32 (valid picture URL).
11. Click “ADD” button.

**Expected Result:**  
User cannot complete the editing process with a value exceeding the maximum length. The field enforces the 60-character limit by preventing additional input.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-13 – Verify maximum length validation when editing the About me field
**Jira Test Case:** [SSQ-108](https://storyspoilerqa.atlassian.net/browse/SSQ-108)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, enter TD-14 (valid first name).
7. In the Middle Name field, enter TD-27 (valid middle name).
8. In the Last Name field, enter TD-17 (valid last name).
9. In the About me field, attempt to enter TD-36 (invalid description, too long).
10. In the Profile picture field, enter TD-32 (valid picture URL).
11. Click “ADD” button.

**Expected Result:**  
User cannot complete the editing process with a value exceeding the maximum length. The field enforces the 256-character limit by preventing additional input.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-14 – Verify validation for Profile picture field with invalid URL (missing "http://")
**Jira Test Case:** [SSQ-109](https://storyspoilerqa.atlassian.net/browse/SSQ-109)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, enter TD-14 (valid first name).
7. In the Middle Name field, enter TD-27 (valid middle name).
8. In the Last Name field, enter TD-17 (valid last name).
9. In the About me field, enter TD-35 (valid description).
10. In the Profile picture field, enter TD-33 (invalid picture URL, missing "http://" or "https://").
11. Click “ADD” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the image URL must start with `~http://"` or `"https://"`.

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.

---

## TC-PROF-15 – Verify validation for Profile picture field with invalid URL (missing "http://")
**Jira Test Case:** [SSQ-110](https://storyspoilerqa.atlassian.net/browse/SSQ-110)  
**Use Case:** [UC-PROF-5](../use-cases/use-cases-user-profile-management.md#XXXXt) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button on My Profile page.
6. In the First Name field, enter TD-14 (valid first name).
7. In the Middle Name field, enter TD-27 (valid middle name).
8. In the Last Name field, enter TD-17 (valid last name).
9. In the About me field, enter TD-35 (valid description).
10. In the Profile picture field, enter TD-34 (invalid picture URL, missing image extension).
11. Click “ADD” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the image URL must end with a valid file extension (e.g., `.jpg`, `.png`, `.jpeg`, `.gif`).

**Execution Result:** ⚠️ Blocked

**Related Bug:** [BUG-PROF-01](../bugs/bug-report.md#XXXX) (Jira: [SSQ-87](https://storyspoilerqa.atlassian.net/browse/SSQ-87))

**Note:** This functionality should be re-tested once the Edit Profile Info page becomes available.