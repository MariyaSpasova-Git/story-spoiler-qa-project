# Test Cases – Spoiler Management

**Requirement Link:** [SSQ-128 – Spoiler Management](https://storyspoilerqa.atlassian.net/browse/SSQ-128)  

This file documents the 7 test cases for the **Spoiler Management** feature.  
Each test case is traceable to its corresponding **Use Case** and **Requirement** in Jira.  

---

## TC-SM-01 – Verify spoiler list and functional buttons on Home Page
**Jira Test Case:** [SSQ-138](https://storyspoilerqa.atlassian.net/browse/SSQ-138)  
**Use Case:** [UC-SM-1](../use-cases/use-cases-spoiler-management.md#uc-sm-1--view-and-manage-created-spoilers) (Jira: [SSQ-129](https://storyspoilerqa.atlassian.net/browse/SSQ-129))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Observe the spoiler/s on the Home Page.

**Expected Result:**
All created spoilers appear with their attributes and buttons “SHARE”, “EDIT”, and “DELETE”.

---

## TC-SM-02 – Verify Home Page default values for new users
**Jira Test Case:** [SSQ-139](https://storyspoilerqa.atlassian.net/browse/SSQ-139)  
**Use Case:** [UC-SM-1](../use-cases/use-cases-spoiler-management.md#uc-sm-1--view-and-manage-created-spoilers) (Jira: [SSQ-129](https://storyspoilerqa.atlassian.net/browse/SSQ-129))

**Prerequisites:** 
- TD-03: Valid new user.
- No spoilers have been created yet.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-03.
4. Observe the content on the Home Page.

**Expected Result:**  
Home Page displays the following elements:
- “No Spoilers Yet!” message
- “WRITE SPOILER” button

---

## TC-SM-03 – Verify “WRITE SPOILER” button redirects to Create Spoiler page
**Jira Test Case:** [SSQ-140](https://storyspoilerqa.atlassian.net/browse/SSQ-140)  
**Use Case:** [UC-SM-1](../use-cases/use-cases-spoiler-management.md#uc-sm-1--view-and-manage-created-spoilers) (Jira: [SSQ-129](https://storyspoilerqa.atlassian.net/browse/SSQ-129))

**Prerequisites:**
- TD-03: Valid new user.
- No spoilers have been created yet.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-03.
4. Click “WRITE SPOILER” button on the Home Page.

**Expected Result:**  
User is redirected to the Create Spoiler page.

---

## TC-SM-04 – Verify Share Spoiler page
**Jira Test Case:** [SSQ-141](https://storyspoilerqa.atlassian.net/browse/SSQ-141)  
**Use Case:** [UC-SM-2](../use-cases/use-cases-spoiler-management.md#uc-sm-2--create-new-spoiler) (Jira: [SSQ-130](https://storyspoilerqa.atlassian.net/browse/SSQ-130))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.

**Expected Result:**  
The Share Spoiler page opens successfully and displays the following elements:
- Message field with placeholder text “Add a short message”
- Email field with placeholder text “Add an email”
- Name field with placeholder text “Add The name of your friend”
- “SHARE” button

---

## TC-SM-05 – Verify spoiler sharing with valid data
**Jira Test Case:** [SSQ-142](https://storyspoilerqa.atlassian.net/browse/SSQ-142)  
**Use Case:** [UC-SM-3](../use-cases/use-cases-spoiler-management.md#uc-sm-3--share-a-spoiler) (Jira: [SSQ-131](https://storyspoilerqa.atlassian.net/browse/SSQ-131))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-46 (valid email).
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
System sends the email successfully.

---

## TC-SM-06 – Verify validation for invalid email (missing '@')
**Jira Test Case:** [SSQ-143](https://storyspoilerqa.atlassian.net/browse/SSQ-143)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-10 (invalid email missing '@').
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
The user is prevented from completing the sharing process. A clear validation message should be displayed indicating that the Email must contain '@'.

---

## TC-SM-07 – Verify validation for invalid email (missing '.')
**Jira Test Case:** [SSQ-144](https://storyspoilerqa.atlassian.net/browse/SSQ-144)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-11 (invalid email missing '.').
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
The user is prevented from completing the sharing process. A clear validation message should be displayed indicating that the Email must contain '.'.

---

## TC-SM-08 – Verify validation for invalid email (missing '@' and '.')
**Jira Test Case:** [SSQ-145](https://storyspoilerqa.atlassian.net/browse/SSQ-145)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-30 (invalid email missing '@” and  '.').
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
The user is prevented from completing the sharing process. A clear validation message should be displayed indicating that the Email must contain '@' and '.'.

---

## TC-SM-09 – Verify validation for invalid email (extra spaces)
**Jira Test Case:** [SSQ-146](https://storyspoilerqa.atlassian.net/browse/SSQ-146)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-48 (leading/trailing spaces).
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
The user is prevented from completing the sharing process. A clear validation message should be displayed indicating that the Email must not contain white spaces.

---

## TC-SM-10 – Verify validation for empty email field
**Jira Test Case:** [SSQ-147](https://storyspoilerqa.atlassian.net/browse/SSQ-147)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. Leave Email field empty.
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
The user is prevented from completing the sharing process. A clear validation message should be displayed indicating that the Email field is mandatory.

---

## TC-SM-11 – Verify validation for invalid email (missing username)
**Jira Test Case:** [SSQ-148](https://storyspoilerqa.atlassian.net/browse/SSQ-148)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-49 (invalid email, missing username).
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
The user is prevented from completing the sharing process. A clear validation message should be displayed indicating that the Email must include a username.

---

## TC-SM-12 – Verify validation for invalid email (missing domain name)
**Jira Test Case:** [SSQ-149](https://storyspoilerqa.atlassian.net/browse/SSQ-149)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-50 (invalid email, missing domain name).
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
The user is prevented from completing the sharing process. A clear validation message should be displayed indicating that the Email must include a domain name between '@' and '.'.

---

## TC-SM-13 – Verify validation for invalid email (missing host)
**Jira Test Case:** [SSQ-150](https://storyspoilerqa.atlassian.net/browse/SSQ-150)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-51 (invalid email, missing host).
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
The user is prevented from completing the sharing process. A clear validation message should be displayed indicating that the Email must end with a valid host (e.g., `.com`, `.net`).

---

## TC-SM-14 – Verify validation for invalid email (multiple '@' symbols)
**Jira Test Case:** [SSQ-151](https://storyspoilerqa.atlassian.net/browse/SSQ-151)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-52 (invalid email, multiple '@' symbols).
7. In the Name field, enter TD-47 (valid name).
8. Click "SHARE" button.

**Expected Result:**  
The user is prevented from completing the sharing process. A clear validation message should be displayed indicating that the Email must include only one '@' symbol.

---

## TC-SM-15 – Verify Edit Spoiler page
**Jira Test Case:** [SSQ-152](https://storyspoilerqa.atlassian.net/browse/SSQ-152)  
**Use Case:** [UC-SM-5](../use-cases/use-cases-spoiler-management.md#uc-sm-5--access-edit-spoiler-page) (Jira: [SSQ-133](https://storyspoilerqa.atlassian.net/browse/SSQ-133))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.

**Expected Result:**  
The Edit Spoiler page opens successfully and displays 3 input fields and a “CREATE” button.

---

## TC-SM-16 – Verify Spoiler Deletion
**Jira Test Case:** [SSQ-153](https://storyspoilerqa.atlassian.net/browse/SSQ-153)  
**Use Case:** [UC-SM-6](../use-cases/use-cases-spoiler-management.md#uc-sm-6--edit-an-existing-spoiler) (Jira: [SSQ-134](https://storyspoilerqa.atlassian.net/browse/SSQ-134))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “DELETE” button for a spoiler on the Home Page.

**Expected Result:**  
The spoiler is successfully deleted and no longer displayed on the Home Page.

---

## TC-SM-17 – Verify that the search field and button are displayed on Home Page
**Jira Test Case:** [SSQ-154](https://storyspoilerqa.atlassian.net/browse/SSQ-154)  
**Use Case:** [UC-SM-9](../use-cases/use-cases-spoiler-management.md#uc-sm-9--search-for-spoilers) (Jira: [SSQ-137](https://storyspoilerqa.atlassian.net/browse/SSQ-137))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Observe the Home Page layout.

**Expected Result:**  
A Search field and Search button (represented by a magnifying glass) are visible on the Home Page.

---

## TC-SM-18 – Verify that the "WRITE SPOILER" button redirects to the Create Spoiler page
**Jira Test Case:** [SSQ-155](https://storyspoilerqa.atlassian.net/browse/SSQ-155)  
**Use Case:** [UC-SM-9](../use-cases/use-cases-spoiler-management.md#uc-sm-9--search-for-spoilers) (Jira: [SSQ-137](https://storyspoilerqa.atlassian.net/browse/SSQ-137))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. In the Search field, enter TD-54 (invalid spoiler title, not existing).
5. Click the Search button.
6. On the “There are no spoilers :(” message view, click the “WRITE SPOILER” button. 

**Expected Result:**  
User is redirected to the Create Spoiler page. 

---

## TC-SM-19 – Verify search functionality displays matching spoilers
**Jira Test Case:** [SSQ-156](https://storyspoilerqa.atlassian.net/browse/SSQ-156)  
**Use Case:** [UC-SM-9](../use-cases/use-cases-spoiler-management.md#uc-sm-9--search-for-spoilers) (Jira: [SSQ-137](https://storyspoilerqa.atlassian.net/browse/SSQ-137))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created with the title TD-53.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Enter TD-53 in the Search field.  
5. Click the Search button.

**Expected Result:**  
The spoiler titled TD-53 is displayed.

---

## TC-SM-20 – Verify search returns no results for non-existing titles
**Jira Test Case:** [SSQ-157](https://storyspoilerqa.atlassian.net/browse/SSQ-157)  
**Use Case:** [UC-SM-9](../use-cases/use-cases-spoiler-management.md#uc-sm-9--search-for-spoilers) (Jira: [SSQ-137](https://storyspoilerqa.atlassian.net/browse/SSQ-137))

**Prerequisites:** 
- TD-02: Valid user.
- At least one spoiler has been created with the title TD-53.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. In the Search field, enter TD-54 (invalid spoiler title, not existing).
5. Click the Search button.

**Expected Result:**  
Message “There are no spoilers :(” is displayed, and the “WRITE SPOILER” button is visible.