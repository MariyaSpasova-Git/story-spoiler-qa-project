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

---

## TC-PROF-03 – Verify “EDIT” button redirects to Edit Profile Info page
**Jira Test Case:** [SSQ-95](https://storyspoilerqa.atlassian.net/browse/SSQ-95)  
**Use Case:** [UC-PROF-2](../use-cases/use-cases-user-profile-management.md#uc-prof-1--access-my-profile-page) (Jira: [SSQ-98](https://storyspoilerqa.atlassian.net/browse/SSQ-98))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button.

**Expected Result:**  
User is redirected to the Edit Profile Info page.

---

## TC-PROF-04 – Verify user can edit their profile
**Jira Test Case:** [SSQ-96](https://storyspoilerqa.atlassian.net/browse/SSQ-96)  
**Use Case:** [UC-PROF-3](../use-cases/use-cases-user-profile-management.md#uc-prof-1--access-my-profile-page) (Jira: [SSQ-90](https://storyspoilerqa.atlassian.net/browse/SSQ-90))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button.

**Expected Result:**  
The user can edit Profile Picture (valid URL), First Name, Middle Name, Last Name, and About Me section.

---

## TC-PROF-05 – Verify validation errors for invalid input during profile edit
**Jira Test Case:** [SSQ-97](https://storyspoilerqa.atlassian.net/browse/SSQ-97)  
**Use Case:** [UC-PROF-4](../use-cases/use-cases-user-profile-management.md#uc-prof-1--access-my-profile-page) (Jira: [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91))

**Prerequisites:** TD-02: Valid user.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the top-left user profile icon in the navigation bar.
5. Click "EDIT" button.
6. On the Edit Profile Info page, enter invalid data in one or more fields, for example:  
   - Invalid Profile Picture URL (e.g., “testimage”)  
   - First Name exceeding 60 characters  
   - About Me text exceeding 256 characters  
7. Click “ADD” button. 

**Expected Result:**  
Validation errors are displayed next to each invalid field.  Error messages are clear, consistent, and user-friendly.