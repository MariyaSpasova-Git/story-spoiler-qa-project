# Use Cases – User Registration

**Requirement Link:** [REQ-2 – User Registration](https://storyspoilerqa.atlassian.net/browse/SSQ-29)

---

## UC-REG-1 – Access Sign Up Page
**Jira Use Case:** [SSQ-30](https://storyspoilerqa.atlassian.net/browse/SSQ-30)

### Description
Unregistered users should be able to access the Sign Up page from the Home Page.

### Preconditions
- User is not logged in.  
- Application is available at the designated URL.

### Main Flow
1. User clicks the **SIGN UP** button on the Home Page.
2. System loads the Sign Up page with the registration form.

### Expected Outcome
The Sign Up page is displayed with all required form fields and action buttons.

---

## UC-REG-2 – Complete Registration with Valid Data
**Jira Use Case:** [SSQ-31](https://storyspoilerqa.atlassian.net/browse/SSQ-31)

### Description
User enters valid registration details and successfully creates a new account.

### Preconditions
- User is not logged in.
- Sign Up page is open.

### Main Flow
1. User fills in all required fields with valid input.
2. User clicks **SIGN UP**.
3. System validates the input.
4. System creates the new account.

### Expected Outcome
User account is created, and user is either redirected to the Log In page or automatically logged in.

---

## UC-REG-3 – Validation Errors during Registration
**Jira Use Case:** [SSQ-32](https://storyspoilerqa.atlassian.net/browse/SSQ-32)

### Description
System must handle invalid or incomplete input and display clear error messages.  

### Preconditions
- User is not logged in.
- Sign Up page is open.

### Main Flow
1. User submits incomplete or invalid data (e.g., invalid email, short password).
2. System validates the input.
3. Validation fails.

### Expected Outcome
System prevents form submission and displays appropriate error messages for each invalid field.

---

## UC-REG-4 – Cancel or Redirect to Log In
**Jira Use Case:** [SSQ-33](https://storyspoilerqa.atlassian.net/browse/SSQ-33)

### Description
User can cancel registration and instead navigate to the Log In page.

### Preconditions
- User is not logged in.
- Sign Up page is open.

### Main Flow
1. User clicks the **LOG IN HERE** button.

### Expected Outcome
System redirects the user to the Log In page.