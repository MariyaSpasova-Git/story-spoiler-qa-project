# Use Cases – Spoiler Creation

**Requirement Link:** [REQ-5 – Spoiler Creation](https://storyspoilerqa.atlassian.net/browse/SSQ-114)

---

## UC-CRSP-1 – Access Create Spoiler Page
**Jira Use Case:** [SSQ-115](https://storyspoilerqa.atlassian.net/browse/SSQ-115)

### Description
Logged-in users can access the Create Spoiler page by clicking the Create Spoiler link in the navigation bar.

### Preconditions
- User is successfully logged in.

### Main Flow
1. User clicks the Create Spoiler link in the top-right navigation bar.
2. System navigates to the Create Spoiler page.

### Expected Outcome
Create Spoiler page displays Story title, Describe your story spoiler, Add a picture for the spoiler, and a “CREATE” button.

---

## UC-CRSP-2 – Create New Spoiler
**Jira Use Case:** [SSQ-116](https://storyspoilerqa.atlassian.net/browse/SSQ-116)

### Description
Users can create Spoilers by entering valid data on Create Spoiler page.

### Preconditions
- User is on Create Spoiler page.

### Main Flow
1. User enters valid data in one or more of the following fields:
   - Story title
   - Describe your story spoiler
   - Add a picture for the spoiler
2. User clicks “CREATE” button.

### xpected Outcome
Spoiler is created successfully. User is redirected to the Home Page, where the new Spoiler is visible with its title, description, and picture.

---

## UC-CRSP-3 – Validation Errors During Spoiler Creation
**Jira Use Case:** [SSQ-117](https://storyspoilerqa.atlassian.net/browse/SSQ-117)

### Description
System must ensure proper validation for all input fields on the Create Spoiler page and display clear error messages.

### Preconditions
- User is on Create Spoiler page.

### Main Flow
1. User leaves required fields blank or enters invalid data.
2. User clicks “CREATE” button.

### xpected Outcome
System prevents Spoiler creation and displays appropriate error messages for each invalid field.