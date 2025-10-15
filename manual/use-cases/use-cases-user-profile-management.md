# Use Cases – User Profile Management

**Requirement Link:** [REQ-4 – User Profile Management](https://storyspoilerqa.atlassian.net/browse/SSQ-88)

---

## UC-PROF-1 – Access My Profile Page
**Jira Use Case:** [SSQ-89](https://storyspoilerqa.atlassian.net/browse/SSQ-89)

### Description
Logged-in users can access their Profile page by clicking the user icon in the navigation bar.

### Preconditions
- User is successfully logged in.
- User is on the My Profile page.

### Main Flow
1. User clicks the user profile icon in the top-right navigation bar.  
2. System navigates to the My Profile page.

### Expected Outcome
My Profile page displays Username, Profile Picture, Full Name, Email, Total Spoilers count, and About Me section.

---

## UC-PROF-2 – Redirect to Edit Profile Info Page
**Jira Use Case:** [SSQ-98](https://storyspoilerqa.atlassian.net/browse/SSQ-98)

### Description
User can access the Edit Profile Info page to edit their profile.

### Preconditions
- My Profile page is open.

### Main Flow
1. User clicks the EDIT button.

### xpected Outcome
System redirects the user to the Edit Profile Info page.

---

## UC-PROF-3 – Access Edit Profile Info Page
**Jira Use Case:** [SSQ-100](https://storyspoilerqa.atlassian.net/browse/SSQ-100)

### Description
Logged-in users can access their Edit Profile Info page by clicking the “EDIT” button on My Profile page.

### Preconditions
- User is on My Profile page.

### Main Flow
1. User clicks the “EDIT” button on My Profile page.  
2. System navigates to the Edit Profile Info page. 

### xpected Outcome
Edit Profile Info page displays fields First Name, Middle Name, Last Name, About Me, and Profile picture.

---

## UC-PROF-4 – Edit Profile Information
**Jira Use Case:** [SSQ-90](https://storyspoilerqa.atlassian.net/browse/SSQ-90)

### Description
Logged-in users can edit their profile information from My Profile page.

### Preconditions
- User is on My Profile page.

### Main Flow
1. User clicks the “EDIT” button.  
2. System opens the Edit Profile Info page.  
3. User updates one or more of the following fields:
   - Profile Picture (valid image URL)
   - First Name
   - Middle Name
   - Last Name
   - About Me  
4. The user clicks “ADD.”  

### Expected Outcome
System validates inputs, saves the changes, and updates the displayed profile information.

---

## UC-PROF-5 – Validation Errors During Profile Edit
**Jira Use Case:** [SSQ-91](https://storyspoilerqa.atlassian.net/browse/SSQ-91)

### Description
System must prevent invalid data submission during profile edits.

### Preconditions
- User is on Edit Profile Info page.

### Main Flow
1. User leaves required fields blank or enters invalid data. 
2. User clicks "ADD" button.

### Expected Outcome
System prevents user from editing their profile. Appropriate error messages are displayed for each incorrect field, indicating the specific rule that has been violated.