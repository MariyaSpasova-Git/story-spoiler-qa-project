# Use Cases – Spoiler Management

**Requirement Link:** [REQ-6 – Spoiler Creation](https://storyspoilerqa.atlassian.net/browse/SSQ-128)

---

## UC-SM-1 – View and Manage Created Spoilers
**Jira Use Case:** [SSQ-129](https://storyspoilerqa.atlassian.net/browse/SSQ-129)

### Description
Logged-in users can view all their created spoilers listed on the Home Page. Each spoiler provides options to Share, Edit, or Delete.

### Preconditions
- User is successfully logged in.
- At least one spoiler has been created.

### Main Flow
1. User navigates to the Home Page.
2. System displays all spoilers created by the logged-in user.
3. Each spoiler includes "SHARE", "EDIT", and "DELETE" buttons.

### Expected Outcome
User sees all created spoilers with management options available.

---

## UC-SM-2 – Create New Spoiler
**Jira Use Case:** [SSQ-130](https://storyspoilerqa.atlassian.net/browse/SSQ-130)

### Description
Users can access the Share Spoiler page by clicking the “SHARE” button for a specific spoiler.

### Preconditions
- User is successfully logged in.
- At least one spoiler is available on the Home Page.

### Main Flow
- User clicks the “SHARE” button for a spoiler.
- System navigates to the Share Spoiler page.

### Expected Outcome
The Share Spoiler interface appears, allowing users to share the spoiler via email.

---

## UC-SM-3 – Share a Spoiler
**Jira Use Case:** [SSQ-131](https://storyspoilerqa.atlassian.net/browse/SSQ-131)

### Description
Users can share a spoiler with a friend via email from the Share Spoiler page.

### Preconditions
- User is successfully logged in.
- Share Spoiler page is open.

### Main Flow
1. User enters a message, recipient’s email, and name in the respective fields.
2. User clicks the “SHARE” button. 
3. System processes the request and attempts to send the spoiler via email.

### Expected Outcome
- The Spoiler is sent to the provided email address.  
- If implemented, a confirmation or success message may be displayed upon successful sharing.

---

## UC-SM-4 – Validation Errors During Spoiler Share
**Jira Use Case:** [SSQ-132](https://storyspoilerqa.atlassian.net/browse/SSQ-132)

### Description
System displays appropriate error messages when invalid or incomplete data is provided during spoiler sharing.

### Preconditions
- User is successfully logged in.
- Share Spoiler page is open.

### Main Flow
1. User attempts to share a spoiler with invalid or missing share details.
2. System validates the input.
3. System displays a corresponding error message.

### Expected Outcome
Validation messages appear for invalid or incomplete inputs, preventing the share action until corrected.

---

## UC-SM-5 – Access Edit Spoiler Page
**Jira Use Case:** [SSQ-133](https://storyspoilerqa.atlassian.net/browse/SSQ-133)

### Description
Logged-in users can open the Edit Spoiler page by clicking the “EDIT” button for an existing spoiler.

### Preconditions
- User is successfully logged in.
- At least one spoiler is available on the Home Page.

### Main Flow
1. User clicks the “EDIT” button below a spoiler.
2. System navigates to the Edit Spoiler page.
3. Existing spoiler data (Title, Description, Picture URL) is pre-filled.

### Expected Outcome
Edit Spoiler page opens with current spoiler details ready for modification.

---

## UC-SM-6 – Edit an Existing Spoiler
**Jira Use Case:** [SSQ-134](https://storyspoilerqa.atlassian.net/browse/SSQ-134)

### Description
Logged-in users can modify spoiler details from the Edit Spoiler page.

### Preconditions
- User is successfully logged in.
- Edit Spoiler page is open with pre-filled spoiler data.

### Main Flow
1. User updates the spoiler’s title, description, or picture URL.
2. User clicks “EDIT”.
3. System validates the input and saves the changes.
4. User is redirected to the Home Page.

### Expected Outcome
Spoiler is updated successfully and displayed with the new details on the Home Page.

---

## UC-SM-7 – Validation Errors During Spoiler Edit

**Jira Use Case:** [SSQ-135](https://storyspoilerqa.atlassian.net/browse/SSQ-135)

### Description
System displays validation messages when invalid or incomplete data is entered while editing a spoiler.

### Preconditions
- User is successfully logged in.
- Edit Spoiler page is open.

### Main Flow
1. User enters invalid data in one or more fields.
2. User clicks “EDIT”.
3. System validates the input and identifies invalid fields.
4. System displays corresponding error messages.

### Expected Outcome
Validation messages are displayed for incorrect or empty fields, preventing update until corrected.

---

## UC-SM-8 – Delete a Spoiler

**Jira Use Case:** [SSQ-136](https://storyspoilerqa.atlassian.net/browse/SSQ-136)

### Description
Logged-in users can delete a spoiler directly from the Home Page.

### Preconditions
- User is successfully logged in.
- At least one spoiler is available on the Home Page.

### Main Flow
1. User clicks the “DELETE” button below a spoiler.
2. Spoiler is removed.
3. Spoiler disappears from the Home Page.

### Expected Outcome
Spoiler is permanently deleted and no longer appears on the Home Page.

---

## UC-SM-9 – Search for Spoilers

**Jira Use Case:** [SSQ-137](https://storyspoilerqa.atlassian.net/browse/SSQ-137)

### Description
Users can search for their spoilers by entering a keyword in the Search field on the Home Page and clicking the Search button. The system filters spoilers based on the entered title.

### Preconditions
- User is successfully logged in.
- At least one spoiler is available on the Home Page.

### Main Flow
1. User enters a keyword in the Search field.
2. User clicks the Search button or Enter.
3. System filters the spoilers list and displays all spoilers matching the keyword.

### Alternative Flow – No Results Found
1. If no spoilers match the search keyword, the system displays the message “There are no spoilers :(”.
2. The Home Page also displays a “WRITE SPOILER” button.
3. When the user clicks the “WRITE SPOILER” button, the system navigates to the Create Spoiler page.

### Expected Outcome
- Spoilers matching the entered keyword are displayed.
- If no matches exist, the message “There are no spoilers :(” and the “WRITE SPOILER” button are displayed.
- Clicking the “WRITE SPOILER” button redirects the user to the Create Spoiler page.
