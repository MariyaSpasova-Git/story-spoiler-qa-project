# Use Cases – User Registration

**Requirement Link:** [REQ-3 – Log In Page](https://storyspoilerqa.atlassian.net/browse/SSQ-71)

---

## UC-LOG-1 – Access Log In Page
**Jira Use Case:** [SSQ-72](https://storyspoilerqa.atlassian.net/browse/SSQ-72)

### Description
Users should be able to access the Log In page from the Home Page.

### Preconditions
- The user is on the Home Page.

### Main Flow
1. User clicks the **LOG IN** button in the navigation bar.
2. System loads the Log In page.

### Expected Outcome
The Log In page is displayed with all required fields and options.

---

## UC-LOG-2 – Log In with Valid Credentials
**Jira Use Case:** [SSQ-73](https://storyspoilerqa.atlassian.net/browse/SSQ-73)

### Description
Users authenticate successfully with valid credentials.

### Preconditions
- The user has a valid, active account.

### Main Flow
1. User opens the Log In page.  
2. User enters valid **Username** and ***Password**.  
3. User clicks **LOG IN**.  
4. System verifies the credentials and grants access.  

### Expected Outcome
User is redirected to the logged-in Home Page.

---

## UC-LOG-3 – Validation Errors for Invalid Credentials
**Jira Use Case:** [SSQ-74](https://storyspoilerqa.atlassian.net/browse/SSQ-74)

### Description
System must ensure incorrect credentials and produce a clear error message.  

### Preconditions
- Log In page is open.

### Main Flow
1. User enters an invalid **Username** or **Password**.  
2. System validates the input.  
3. Authentication fails.

### Expected Outcome
System prevents user login and displays appropriate error message. User remains on the Log In page and can retry.

---

## UC-LOG-4 – Redirect to Forgot Password Page
**Jira Use Case:** [SSQ-75](https://storyspoilerqa.atlassian.net/browse/SSQ-75)

### Description
User can access the Restore Password page to recover credentials.

### Preconditions
- Log In page is open.

### Main Flow
1. User clicks the **Forgot Password?** link.

### Expected Outcome
System redirects the user to the Restore Password page.

---

## UC-LOG-5 – Redirect to Sign Up Page
**Jira Use Case:** [SSQ-76](https://storyspoilerqa.atlassian.net/browse/SSQ-76)

### Description
User can access the Sign Up page to create a new account.

### Preconditions
- Log In page is open.

### Main Flow
1. User clicks the **CREATE NEW** button.

### Expected Outcome
System redirects the user to the Sign Up page.