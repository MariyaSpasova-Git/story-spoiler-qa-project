# Bugs Report – Home Page

This file documents all identified bugs related to the Home Page requirements and use cases.  
Each bug is linked to its corresponding Jira issue, GitHub test case(s), and screenshot evidence.  

---

## BUG-HP-01 – Missing picture in "Upload a Picture" section

**Jira Issue:** [SSQ-25](https://storyspoilerqa.atlassian.net/browse/SSQ-25)
**Related Test Case:**  
- [TC-HP-01](../tests/test-cases-home-page.md#tc-hp-01) ([Jira link:](https://storyspoilerqa.atlassian.net/browse/SSQ-6)) – Verify Home Page for non-logged-in users  

### Title
Picture missing in "Upload a Picture" section

### Steps to Reproduce
1. Open the app URL.
2. Scroll to the "Upload a Picture" section on the Home Page.

### Expected Result
The section should display:
- Motivational phrase
- Short description
- Corresponding picture

### Actual Result
The picture is not displayed. Instead, the alt text `"uploading spoiler story picture"` appears.

### Severity
Medium – Content is incomplete, impacting user experience.

### Priority
Medium – Fix needed but not blocking core functionality.

### Status
Open

### Affected Areas
- Home Page (non-logged-in users)

### Screenshot
![BUG-HP-01](../docs/screenshots/bug-hp-01.png)

---

## BUG-HP-02 – Copyright link in footer does not redirect

**Jira Issue:** [SSQ-26](https://storyspoilerqa.atlassian.net/browse/SSQ-26)
**Related Test Cases:**  
- [TC-HP-07](../tests/test-cases-home-page.md#tc-hp-07) ([Jira link:](https://storyspoilerqa.atlassian.net/browse/SSQ-12)) – Verify Copyright link in footer for non-logged-in users
- [TC-HP-15](../tests/test-cases-home-page.md#tc-hp-15) – ([Jira link:](https://storyspoilerqa.atlassian.net/browse/SSQ-20)) - Verify Copyright link in footer for logged-in users

### Title
Copyright link in footer does not redirect to Copyright page

### Steps to Reproduce
1. Open the app URL.
2. Scroll to the footer.
3. Click the "StorySpoil" copyright link.

### Expected Result
User is redirected to the dedicated Copyright page.

### Actual Result
The page does not redirect. Instead, the screen scrolls to the top.

### Severity
Medium – Functionality issue that impacts compliance/UX but does not block core flows.  

### Priority
High – Affects all users across all pages where the footer appears.  

### Status
Open  

### Affected Areas
- Home Page (non-logged-in users)  
- Home Page (logged-in users)  
- Any page containing the footer component  

---

