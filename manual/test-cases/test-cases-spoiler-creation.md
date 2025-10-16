# Test Cases – Spoiler Creation

**Requirement Link:** [SSQ-114 – Spoiler Creation](https://storyspoilerqa.atlassian.net/browse/SSQ-114)  

This file documents the 10 test cases for the **Spoiler Creation** feature.  
Each test case is traceable to its corresponding **Use Case** and **Requirement** in Jira.  

---

## TC-CRSP-01 – Verify Create Spoiler page
**Jira Test Case:** [SSQ-118](https://storyspoilerqa.atlassian.net/browse/SSQ-118)  
**Use Case:** [UC-CRSP-1](../use-cases/use-cases-spoiler-creation.md#uc-crsp-1--access-create-spoiler-page) (Jira: [SSQ-115](https://storyspoilerqa.atlassian.net/browse/SSQ-115))

**Prerequisites:** TD-02: Valid user account.

**Steps:**
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. Observe the Create Spoiler page.

**Expected Result:**
The Create Spoiler page displays the following elements:
- Story title field
- Describe your story spoiler field
- Add a picture for the spoiler field
- “CREATE” button

**Execution Result:** ✅ Passed

---

## TC-CRSP-02 – Verify spoiler creation with all valid fields
**Jira Test Case:** [SSQ-119](https://storyspoilerqa.atlassian.net/browse/SSQ-119)  
**Use Case:** [UC-CRSP-2](../use-cases/use-cases-spoiler-creation.md#uc-crsp-2--create-new-spoiler) (Jira: [SSQ-116](https://storyspoilerqa.atlassian.net/browse/SSQ-116))

**Prerequisites:** TD-02: Valid user account.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. In the Story title field, enter TD-40 (valid story title).
6. In the Describe your story spoiler field, enter TD-41 (valid story description).
7. In the Add a picture for the spoiler field, enter TD-33 (valid picture URL).
8. Click “CREATE” button.

**Expected Result:**  
Spoiler is created successfully. User is redirected to the Home Page where the newly created spoiler appears with its attributes (title, description, picture, username, date) and buttons (“SHARE”, “EDIT”, and “DELETE”).

**Execution Result:** ✅ Passed

**Note:**  
Button presence is verified in a separate query.

**Related Query:** 
- [QRY-CRSP-01](../queries/queries.md#XXXXX) (Jira: [SSQ-67](https://storyspoilerqa.atlassian.net/browse/SSQ-67))

---

## TC-CRSP-03 – Verify spoiler creation with only required fields
**Jira Test Case:** [SSQ-120](https://storyspoilerqa.atlassian.net/browse/SSQ-120)  
**Use Case:** [UC-CRSP-2](../use-cases/use-cases-spoiler-creation.md#uc-crsp-2--create-new-spoiler) (Jira: [SSQ-116](https://storyspoilerqa.atlassian.net/browse/SSQ-116))

**Prerequisites:** TD-02: Valid user account.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. In the Story title field, enter TD-40 (valid story title).
6. In the Describe your story spoiler field, enter TD-41 (valid story description).
7. In the Add a picture for the spoiler field, enter TD-42 (empty picture URL).
8. Click “CREATE” button.

**Expected Result:**  
Spoiler is created successfully. User is redirected to the Home Page where the newly created spoiler appears with its attributes (title, description, empty spoiler picture placeholder, username, date) and buttons (“SHARE”, “EDIT”, and “DELETE”).

**Note:** Presence of the action buttons (“SHARE” / “EDIT” / “DELETE”) on the created spoiler is tracked separately in query [QRY-CRSP-01 – Missing "SHARE" button on newly created spoilers](https://storyspoilerqa.atlassian.net/browse/SSQ-67). This test verifies creation + attribute visibility; button functionality will be covered under the Spoiler Management requirement.

**Execution Result:** ✅ Passed

**Related Query:** 
- [QRY-CRSP-01](../queries/queries.md#XXXXX) (Jira: [SSQ-67](https://storyspoilerqa.atlassian.net/browse/SSQ-67))

---

## TC-CRSP-04 – Verify required fields validation when all fields are empty
**Jira Test Case:** [SSQ-121](https://storyspoilerqa.atlassian.net/browse/SSQ-121)  
**Use Case:** [UC-CRSP-3](../use-cases/use-cases-spoiler-creation.md#uc-crsp-3--validation-errors-during-spoiler-creation) (Jira: [SSQ-117](https://storyspoilerqa.atlassian.net/browse/SSQ-117))

**Prerequisites:** TD-02: Valid user account.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. Leave all fields empty.
8. Click “CREATE” button.

**Expected Result:**  
Clear and consistent validation messages are displayed for each required field (Story title and Describe your story spoiler). Optional field (Add a picture for the spoiler) does not trigger error.

**Execution Result:** ✅ Passed

**Related Query:** 
- [QRY-UX-01](../queries/queries.md#qry-ux-01--extra-bullet-point-before-error-messages-across-multiple-forms) (Jira: [SSQ-60](https://storyspoilerqa.atlassian.net/browse/SSQ-60))

---

## TC-CRSP-05 – Verify maximum length validation for spoiler title
**Jira Test Case:** [SSQ-122](https://storyspoilerqa.atlassian.net/browse/SSQ-122)  
**Use Case:** [UC-CRSP-3](../use-cases/use-cases-spoiler-creation.md#uc-crsp-3--validation-errors-during-spoiler-creation) (Jira: [SSQ-117](https://storyspoilerqa.atlassian.net/browse/SSQ-117))

**Prerequisites:** TD-02: Valid user account.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. In the Story title field, attempt to enter TD-43 (invalid story title, too long).
6. In the Describe your story spoiler field, enter TD-41 (valid story description).
7. In the Add a picture for the spoiler field, enter TD-42 (empty picture URL).
8. Click “CREATE” button.

**Expected Result:**  
User cannot complete the creation process with a value exceeding the maximum length. The field enforces the 70-character limit by preventing additional input.

**Execution Result:** ✅ Passed

---

## TC-CRSP-06 – Verify maximum length validation for spoiler description
**Jira Test Case:** [SSQ-123](https://storyspoilerqa.atlassian.net/browse/SSQ-123)  
**Use Case:** [UC-CRSP-3](../use-cases/use-cases-spoiler-creation.md#uc-crsp-3--validation-errors-during-spoiler-creation) (Jira: [SSQ-117](https://storyspoilerqa.atlassian.net/browse/SSQ-117))

**Prerequisites:** TD-02: Valid user account.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. In the Story title field, enter TD-40 (valid story title).
6. In the Describe your story spoiler field, attempt to enter TD-44 (invalid story description, too long).
7. In the Add a picture for the spoiler field, enter TD-42 (empty picture URL).
8. Click “CREATE” button.

**Expected Result:**  
User cannot complete the creation process with a value exceeding the maximum length. The field enforces the 400-character limit by preventing additional input.

**Execution Result:** ✅ Passed

---

## TC-CRSP-07 – Verify validation for spoiler picture field with invalid URL (missing protocol)
**Jira Test Case:** [SSQ-124](https://storyspoilerqa.atlassian.net/browse/SSQ-124)  
**Use Case:** [UC-CRSP-3](../use-cases/use-cases-spoiler-creation.md#uc-crsp-3--validation-errors-during-spoiler-creation) (Jira: [SSQ-117](https://storyspoilerqa.atlassian.net/browse/SSQ-117))

**Prerequisites:** TD-02: Valid user account.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. In the Story title field, enter TD-40 (valid story title).
6. In the Describe your story spoiler field, enter TD-41 (valid story description).
7. In the Add a picture for the spoiler field, enter TD-35 (invalid picture URL, missing protocol).
8. Click “CREATE” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the image URL must start with `"http://"` or `"https://"`.

**Execution Result:** ✅ Passed

**Related Queryies:** 
- [QRY-UX-01](../queries/queries.md#qry-ux-01--extra-bullet-point-before-error-messages-across-multiple-forms) (Jira: [SSQ-60](https://storyspoilerqa.atlassian.net/browse/SSQ-60))
- [QRY-CRSP-02](../queries/queries.md#XXXX) (Jira: [SSQ-94](https://storyspoilerqa.atlassian.net/browse/SSQ-94))

---

## TC-CRSP-08 – Verify validation for spoiler picture field with invalid URL (missing file extension)
**Jira Test Case:** [SSQ-125](https://storyspoilerqa.atlassian.net/browse/SSQ-125)  
**Use Case:** [UC-CRSP-3](../use-cases/use-cases-spoiler-creation.md#uc-crsp-3--validation-errors-during-spoiler-creation) (Jira: [SSQ-117](https://storyspoilerqa.atlassian.net/browse/SSQ-117))

**Prerequisites:** TD-02: Valid user account.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. In the Story title field, enter TD-40 (valid story title).
6. In the Describe your story spoiler field, enter TD-41 (valid story description).
7. In the Add a picture for the spoiler field, enter TD-36 (invalid picture URL, missing file extension).
8. Click “CREATE” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the picture URL must end with a valid image extension (e.g., `.jpg`, `.png`, `.jpeg`, `.gif`).

**Execution Result:** ✅ Passed

**Related Queryies:** 
- [QRY-UX-01](../queries/queries.md#qry-ux-01--extra-bullet-point-before-error-messages-across-multiple-forms) (Jira: [SSQ-60](https://storyspoilerqa.atlassian.net/browse/SSQ-60))
- [QRY-CRSP-02](../queries/queries.md#XXXX) (Jira: [SSQ-94](https://storyspoilerqa.atlassian.net/browse/SSQ-94))

---

## TC-CRSP-09 – Verify validation for spoiler picture field with invalid URL (wrong extension)
**Jira Test Case:** [SSQ-126](https://storyspoilerqa.atlassian.net/browse/SSQ-126)  
**Use Case:** [UC-CRSP-3](../use-cases/use-cases-spoiler-creation.md#uc-crsp-3--validation-errors-during-spoiler-creation) (Jira: [SSQ-117](https://storyspoilerqa.atlassian.net/browse/SSQ-117))

**Prerequisites:** TD-02: Valid user account.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. In the Story title field, enter TD-40 (valid story title).
6. In the Describe your story spoiler field, enter TD-41 (valid story description).
7. In the Add a picture for the spoiler field, enter TD-37 (invalid picture URL, wrong extension).
8. Click “CREATE” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the picture URL must end with a valid image extension (e.g., `.jpg`, `.png`, `.jpeg`, `.gif`).

**Execution Result:** ✅ Passed

**Related Queryies:** 
- [QRY-UX-01](../queries/queries.md#qry-ux-01--extra-bullet-point-before-error-messages-across-multiple-forms) (Jira: [SSQ-60](https://storyspoilerqa.atlassian.net/browse/SSQ-60))
- [QRY-CRSP-02](../queries/queries.md#XXXX) (Jira: [SSQ-94](https://storyspoilerqa.atlassian.net/browse/SSQ-94))

---

## TC-CRSP-10 – Verify validation for spoiler picture field with invalid URL (invalid URL structure)
**Jira Test Case:** [SSQ-127](https://storyspoilerqa.atlassian.net/browse/SSQ-127)  
**Use Case:** [UC-CRSP-3](../use-cases/use-cases-spoiler-creation.md#uc-crsp-3--validation-errors-during-spoiler-creation) (Jira: [SSQ-117](https://storyspoilerqa.atlassian.net/browse/SSQ-117))

**Prerequisites:** TD-02: Valid user account.

**Steps:**  
1. Navigate to the app URL.
2. Click “LOG IN” button in the navigation bar.
3. Enter the valid credentials (username and password) from TD-02.
4. Click the Create Spoiler link in the navigation bar.
5. In the Story title field, enter TD-40 (valid story title).
6. In the Describe your story spoiler field, enter TD-41 (valid story description).
7. In the Add a picture for the spoiler field, enter TD-34 (invalid picture URL, invalid URL structure).
8. Click “CREATE” button.

**Expected Result:**  
Clear validation error message is displayed indicating that the picture URL must start with `"http://"` or `"https://"` and end with a valid image extension (e.g., `.jpg`, `.png`, `.jpeg`, `.gif`).

**Execution Result:** ✅ Passed

**Related Queryies:** 
- [QRY-UX-01](../queries/queries.md#qry-ux-01--extra-bullet-point-before-error-messages-across-multiple-forms) (Jira: [SSQ-60](https://storyspoilerqa.atlassian.net/browse/SSQ-60))
- [QRY-CRSP-02](../queries/queries.md#XXXX) (Jira: [SSQ-94](https://storyspoilerqa.atlassian.net/browse/SSQ-94))