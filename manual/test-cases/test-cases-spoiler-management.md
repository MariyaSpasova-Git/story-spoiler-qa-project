# Test Cases – Spoiler Management

**Requirement Link:** [SSQ-128 – Spoiler Management](https://storyspoilerqa.atlassian.net/browse/SSQ-128)  

This file documents the 31 test cases for the **Spoiler Management** feature.  
Each test case is traceable to its corresponding **Use Case** and **Requirement** in Jira.  

**Note:**
> The original requirements document does not specify detailed field requirements for the Edit Spoiler and Share Spoiler pages.
> Test cases related to these pages are created based on the assumption that their field rules and validation constraints are consistent with those defined for the Create Spoiler page, unless clarified otherwise in future requirement updates.

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

**Note:** Assumed Message and Name fields rules (requirements not specified).

---

## TC-SM-06 – Verify maximum length validation for message
**Jira Test Case:** [SSQ-168](https://storyspoilerqa.atlassian.net/browse/SSQ-168)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, attempt to enter TD-55 (invalid message, too long).
6. In the Email field, enter TD-46 (valid email).
7. In the Name field, enter TD-47 (valid name).
8. Click “SHARE” button.

**Expected Result:**  
System prevents the user from sharing the spoiler when the message exceeds 100 characters. The field enforces the character limit by restricting additional input.

**Note:** Assumed Message field rules (requirements not specified).

---

## TC-SM-07 – Verify maximum length validation for name
**Jira Test Case:** [SSQ-169](https://storyspoilerqa.atlassian.net/browse/SSQ-169)  
**Use Case:** [UC-SM-4](../use-cases/use-cases-spoiler-management.md#uc-sm-4--validation-errors-during-spoiler-share) (Jira: [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132))

**Prerequisites:** 
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “SHARE” button for a spoiler on the Home Page.
5. In the Message field, enter TD-45 (valid message).
6. In the Email field, enter TD-46 (valid email).
7. In the Name field, enter TD-56 (invalid name, too long).
8. Click “SHARE” button.

**Expected Result:**  
System prevents the user from sharing the spoiler when the name exceeds 70 characters. The field enforces the character limit by restricting additional input.

**Note:** Assumed Name field rules (requirements not specified).

---

## TC-SM-08 – Verify validation for invalid email (missing '@')
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

## TC-SM-09 – Verify validation for invalid email (missing '.')
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

## TC-SM-10 – Verify validation for invalid email (missing '@' and '.')
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

## TC-SM-11 – Verify validation for invalid email (extra spaces)
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

## TC-SM-12 – Verify validation for empty email field
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

## TC-SM-13 – Verify validation for invalid email (missing username)
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

## TC-SM-14 – Verify validation for invalid email (missing domain name)
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

## TC-SM-15 – Verify validation for invalid email (missing host)
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

## TC-SM-16 – Verify validation for invalid email (multiple '@' symbols)
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

## TC-SM-17 – Verify Edit Spoiler page
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

## TC-SM-18 – Verify spoiler edit with all valid fields
**Jira Test Case:** [SSQ-159](https://storyspoilerqa.atlassian.net/browse/SSQ-159)  
**Use Case:** [UC-SM-6](../use-cases/use-cases-spoiler-management.md#uc-sm-6--edit-an-existing-spoiler) (Jira: [SSQ-134](https://storyspoilerqa.atlassian.net/browse/SSQ-134))

**Prerequisites:** 
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.
5. In the first (title) field, enter TD-40 (valid story title).
6. In the second (description) field, enter TD-41 (valid story description).
7. In the third (picture URL) field, enter TD-33 (valid picture URL).
8. Click “CREATE” button.

**Expected Result:**  
Spoiler is updated successfully. User is redirected to the Home Page where the updated spoiler appears.

**Note:** Assumed same field rules as Create Spoiler page (requirements not specified).

---

## TC-SM-19 – Verify spoiler edit with only required fields
**Jira Test Case:** [SSQ-160](https://storyspoilerqa.atlassian.net/browse/SSQ-160)  
**Use Case:** [UC-SM-6](../use-cases/use-cases-spoiler-management.md#uc-sm-6--edit-an-existing-spoiler) (Jira: [SSQ-134](https://storyspoilerqa.atlassian.net/browse/SSQ-134))

**Prerequisites:** 
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.
5. In the first (title) field, enter TD-40 (valid story title).
6. In the second (description) field, enter TD-41 (valid story description).
7. In the third (picture URL) field, enter TD-42 (empty picture URL).
8. Click “CREATE” button.

**Expected Result:**  
Spoiler is updated successfully. User is redirected to the Home Page where the updated spoiler appears.

**Note:** Assumed same field rules as Create Spoiler page (requirements not specified).

---

## TC-SM-20 – Verify required fields validation when all fields are empty
**Jira Test Case:** [SSQ-161](https://storyspoilerqa.atlassian.net/browse/SSQ-161)  
**Use Case:** [UC-SM-7](../use-cases/use-cases-spoiler-management.md#uc-sm-7--validation-errors-during-spoiler-edit) (Jira: [SSQ-135](https://storyspoilerqa.atlassian.net/browse/SSQ-135))

**Prerequisites:** 
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.
5. Leave all fields empty.
8. Click “CREATE” button.

**Expected Result:**  
Clear and consistent validation messages are displayed for each required field: the first one (story title) and the second one (story description). The optional third field (picture URL) does not trigger error.

**Note:** Assumed same field rules as Create Spoiler page (requirements not specified).

---

## TC-SM-21 – Verify maximum length validation for spoiler title
**Jira Test Case:** [SSQ-162](https://storyspoilerqa.atlassian.net/browse/SSQ-162)  
**Use Case:** [UC-SM-7](../use-cases/use-cases-spoiler-management.md#uc-sm-7--validation-errors-during-spoiler-edit) (Jira: [SSQ-135](https://storyspoilerqa.atlassian.net/browse/SSQ-135))

**Prerequisites:** 
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.
5. In the first (title) field, attempt to enter TD-43 (invalid story title, too long).
6. In the second (description) field, enter TD-41 (valid story description).
7. In the third (picture URL) field, enter TD-33 (valid picture URL).
8. Click “CREATE” button.

**Expected Result:**  
System prevents the user from saving the spoiler when the title exceeds 70 characters. The field enforces the character limit by restricting additional input.

**Note:** Assumed same field rules as Create Spoiler page (requirements not specified).

---

## TC-SM-22 – Verify maximum length validation for spoiler description
**Jira Test Case:** [SSQ-163](https://storyspoilerqa.atlassian.net/browse/SSQ-163)  
**Use Case:** [UC-SM-7](../use-cases/use-cases-spoiler-management.md#uc-sm-7--validation-errors-during-spoiler-edit) (Jira: [SSQ-135](https://storyspoilerqa.atlassian.net/browse/SSQ-135))

**Prerequisites:**
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.
5. In the first (title) field, enter TD-40 (valid story title).
6. In the second (description) field, attempt to enter TD-44 (invalid story description, too long).
7. In the third (picture URL) field, enter TD-33 (valid picture URL).
8. Click “CREATE” button.

**Expected Result:**  
User cannot save the changes with a value exceeding the maximum length. The field enforces the 400-character limit by preventing additional input.

**Note:** Assumed same field rules as Create Spoiler page (requirements not specified).

---

## TC-SM-23 – Verify validation for spoiler picture field with invalid URL (missing protocol)
**Jira Test Case:** [SSQ-164](https://storyspoilerqa.atlassian.net/browse/SSQ-164)  
**Use Case:** [UC-SM-7](../use-cases/use-cases-spoiler-management.md#uc-sm-7--validation-errors-during-spoiler-edit) (Jira: [SSQ-135](https://storyspoilerqa.atlassian.net/browse/SSQ-135))

**Prerequisites:**
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.
5. In the first (title) field, enter TD-40 (valid story title).
6. In the second (description) field, enter TD-41 (valid story description).
7. In the third (picture URL) field, enter TD-35 (invalid picture URL, missing protocol).
8. Click “CREATE” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the image URL must start with `"http://"` or `"https://"`.

**Note:** Assumed same field rules as Create Spoiler page (requirements not specified).

---

## TC-SM-24 – Verify validation for spoiler picture field with invalid URL (missing file extension)
**Jira Test Case:** [SSQ-165](https://storyspoilerqa.atlassian.net/browse/SSQ-165)  
**Use Case:** [UC-SM-7](../use-cases/use-cases-spoiler-management.md#uc-sm-7--validation-errors-during-spoiler-edit) (Jira: [SSQ-135](https://storyspoilerqa.atlassian.net/browse/SSQ-135))

**Prerequisites:**
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.
5. In the first (title) field, enter TD-40 (valid story title).
6. In the second (description) field, enter TD-41 (valid story description).
7. In the third (picture URL) field, enter TD-36 (invalid picture URL, missing file extension).
8. Click “CREATE” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the picture URL must end with a valid image extension (e.g., `.jpg`, `.png`, `.jpeg`, `.gif`).

**Note:** Assumed same field rules as Create Spoiler page (requirements not specified).

---

## TC-SM-25 – Verify validation for spoiler picture field with invalid URL (wrong extension)
**Jira Test Case:** [SSQ-166](https://storyspoilerqa.atlassian.net/browse/SSQ-166)  
**Use Case:** [UC-SM-7](../use-cases/use-cases-spoiler-management.md#uc-sm-7--validation-errors-during-spoiler-edit) (Jira: [SSQ-135](https://storyspoilerqa.atlassian.net/browse/SSQ-135))

**Prerequisites:**
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.
5. In the first (title) field, enter TD-40 (valid story title).
6. In the second (description) field, enter TD-41 (valid story description).
7. In the third (picture URL) field, enter TD-37 (invalid picture URL, wrong extension).
8. Click “CREATE” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the picture URL must end with a valid image extension (e.g., `.jpg`, `.png`, `.jpeg`, `.gif`).

**Note:** Assumed same field rules as Create Spoiler page (requirements not specified).

---

## TC-SM-26 – Verify validation for spoiler picture field with invalid URL (invalid URL structure)
**Jira Test Case:** [SSQ-167](https://storyspoilerqa.atlassian.net/browse/SSQ-167)  
**Use Case:** [UC-SM-7](../use-cases/use-cases-spoiler-management.md#uc-sm-7--validation-errors-during-spoiler-edit) (Jira: [SSQ-135](https://storyspoilerqa.atlassian.net/browse/SSQ-135))

**Prerequisites:**
- TD-02: Valid user account.
- At least one spoiler has been created.

**Steps:**
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click “EDIT” button for a spoiler on the Home Page.
5. In the first (title) field, enter TD-40 (valid story title).
6. In the second (description) field, enter TD-41 (valid story description).
7. In the third (picture URL) field, enter TD-34 (invalid picture URL, invalid URL structure).
8. Click “CREATE” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the picture URL must start with `"http://"` or `"https://"` and end with a valid image extension (e.g., `.jpg`, `.png`, `.jpeg`, `.gif`).

**Note:** Assumed same field rules as Create Spoiler page (requirements not specified).

---

## TC-SM-27 – Verify Spoiler Deletion
**Jira Test Case:** [SSQ-153](https://storyspoilerqa.atlassian.net/browse/SSQ-153)  
**Use Case:** [UC-SM-8](../use-cases/use-cases-spoiler-management.md#uc-sm-6--edit-an-existing-spoiler) (Jira: [SSQ-136](https://storyspoilerqa.atlassian.net/browse/SSQ-134))

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

## TC-SM-28 – Verify that the search field and button are displayed on Home Page
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

## TC-SM-29 – Verify that "WRITE SPOILER" button redirects to the Create Spoiler page
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

## TC-SM-30 – Verify search functionality displays matching spoilers
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

## TC-SM-31 – Verify search returns no results for non-existing titles
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