# Use Case 1 – Home Page

**Requirement Link:** [SSQ-1 – Requirement: Home Page Access](https://storyspoilerqa.atlassian.net/browse/SSQ-1)

This document describes the four use cases related to accessing and displaying the Home Page of the StorySpoil application.  
Each use case is linked to its corresponding Jira issue for traceability.  

---

## UC-HP-1 – Home Page (Non-logged-in User)
**Jira Issue:** [SSQ-2](https://storyspoilerqa.atlassian.net/browse/SSQ-2)

### Description
A non-logged-in user should be able to access the Home Page and see the default sections.

### Preconditions
- User is not logged in.  
- Application is available at the designated URL.  

### Main Flow
1. User navigates to the application URL.  
2. The system loads the Home Page.  

### Expected Outcome
The Home Page displays:
- Navigation bar  
- Title and subtitle  
- Three main sections  
- Footer  

### Linked Requirement
[SSQ-1 – Requirement: Home Page Access](https://storyspoilerqa.atlassian.net/browse/SSQ-1)

---

## UC-HP-2 – Home Page (Logged-in User)
**Jira Issue:** [SSQ-3](https://storyspoilerqa.atlassian.net/browse/SSQ-3)

### Description
A logged-in user should be able to access the Home Page and see personalized content.

### Preconditions
- User is logged in with valid credentials.  
- Application is available at the designated URL.  

### Main Flow
1. User navigates to the application URL while logged in.  
2. The system loads the Home Page.  

### Expected Outcome
The Home Page displays:
- Navigation bar with user-specific options  
- Personalized content (spoilers feed or welcome message)  
- Footer  

### Linked Requirement
[SSQ-1 – Requirement: Home Page Access](https://storyspoilerqa.atlassian.net/browse/SSQ-1)

---

## UC-HP-3 – Home Page (New User with No Spoilers)
**Jira Issue:** [SSQ-4](https://storyspoilerqa.atlassian.net/browse/SSQ-4)

### Description
A newly registered user with no spoilers should be able to access the Home Page and see an empty state message.

### Preconditions
- User is logged in with a newly created account.  
- No spoilers are available in the user’s feed.  

### Main Flow
1. User navigates to the application URL while logged in.  
2. The system loads the Home Page.  

### Expected Outcome
The Home Page displays:
- Navigation bar with user-specific options  
- Empty state message (e.g., “No Spoilers Yet!”)  
- Footer  

### Linked Requirement
[SSQ-1 – Requirement: Home Page Access](https://storyspoilerqa.atlassian.net/browse/SSQ-1)

---

## UC-HP-4 – Home Page Failure State Message Display
**Jira Issue:** [SSQ-5](https://storyspoilerqa.atlassian.net/browse/SSQ-5)

### Description
The application should show appropriate error messages if the Home Page cannot load.

### Preconditions
- User is either logged in or not logged in.  
- Application URL is unreachable, invalid, or internet is disconnected.  

### Main Flow
1. User attempts to access the application.  
2. The system fails to load the Home Page.  

### Expected Outcome
The system displays a browser error message or application-specific failure message (e.g., “This site cannot be reached”).  

### Linked Requirement
[SSQ-1 – Requirement: Home Page Access](https://storyspoilerqa.atlassian.net/browse/SSQ-1)
