# Test Cases – Home Page

**Requirement Link:** [SSQ-1 – Home Page Access](https://storyspoilerqa.atlassian.net/browse/SSQ-1)  

This file documents the 19 test cases for the **Home Page** feature.  
Each test case is traceable to its corresponding **Use Case** and **Requirement** in Jira.  

---

## TC-HP-01 – Verify Home Page for Non-logged-in Users
**Jira Test Case:** [SSQ-6](https://storyspoilerqa.atlassian.net/browse/SSQ-6)  
**Use Case:** UC-HP-1 (Jira: [SSQ-2](https://storyspoilerqa.atlassian.net/browse/SSQ-2))

**Prerequisites:** TD-01: Guest Session.  

**Steps:**  
1. Navigate to the app URL.
2. Observe the Home Page layout.

**Expected Result:**  
The Home Page is scrollable and displays:  
Navigation bar on top
- Title "STORY SPOILER"
- Subtitle "Share your spoilers responsibly and kindle the love for storytelling."
- "Summarize the Story" section
- "Upload a Picture" section
- "Ready to Spoil a Story?" section
- Footer 

**Execution Result:** ❌ Failed

**Related Bug:** [BUG-HP-01](../bugs/bugs-report.md#bug-hp-01) (Jira: [SSQ-25](https://storyspoilerqa.atlassian.net/browse/SSQ-25))
**Screenshot:** ![BUG-HP-01](../screenshots/bug-hp-01.png)  


---

## TC-HP-02 – Verify Navigation Bar for Non-logged-in Users
**Jira Test Case:** [SSQ-7](https://storyspoilerqa.atlassian.net/browse/SSQ-7)  
**Use Case:** UC-HP-1 (Jira: [SSQ-2](https://storyspoilerqa.atlassian.net/browse/SSQ-2))

**Prerequisites:** TD-01: Guest Session.  

**Steps:**  
1. Navigate to the app URL.  
2. Observe the navigation bar.  

**Expected Result:**  
Navigation bar is fixed at the top and displays:  
- “StorySpoil” link (left)  
- “SIGN UP” and “LOG IN” buttons (right)

**Execution Result:** ✅ Passed

---

## TC-HP-03 – Verify “STORYSPOIL” Home Link for non-logged-in users
**Jira Test Case:** [SSQ-8](https://storyspoilerqa.atlassian.net/browse/SSQ-8)  
**Use Case:** UC-HP-1 (Jira: [SSQ-2](https://storyspoilerqa.atlassian.net/browse/SSQ-2))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Navgate to the app URL.  
2. Click “STORYSPOIL” link in the navigation bar.  

**Expected Result:**  
Home Page reloads correctly.  

**Execution Result:** ✅ Passed

---

## TC-HP-04 – Verify “SIGN UP” button in navigation bar
**Jira Test Case:** [SSQ-9](https://storyspoilerqa.atlassian.net/browse/SSQ-9)  
**Use Case:** UC-HP-1 (Jira: [SSQ-2](https://storyspoilerqa.atlassian.net/browse/SSQ-2))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Navigate to the app URL.  
2. Click “SIGN UP” button in the navigation bar.  

**Expected Result:**  
User is redirected to the Sign Up page. 

**Execution Result:** ✅ Passed

---

## TC-HP-05 – Verify “LOG IN” button in navigaton bar
**Jira Test Case:** [SSQ-10](https://storyspoilerqa.atlassian.net/browse/SSQ-10)  
**Use Case:** UC-HP-1 (Jira: [SSQ-2](https://storyspoilerqa.atlassian.net/browse/SSQ-2))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Navigate to the app URL.  
2. Click “LOG IN” button in the navigation bar.  

**Expected Result:**  
User is redirected to the Log In page.  

**Execution Result:** ✅ Passed

---

## TC-HP-06 – Verify footer for non-logged-in users
**Jira Test Case:** [SSQ-11](https://storyspoilerqa.atlassian.net/browse/SSQ-11)  
**Use Case:** UC-HP-1 (Jira: [SSQ-2](https://storyspoilerqa.atlassian.net/browse/SSQ-2))

**Prerequisites:** TD-01: Guest Session.

**Steps:**  
1. Navigate to the app URL.  
2. Observe the footer.  

**Expected Result:**  
Footer displays “Copyright © StorySpoil 2023”.  

**Execution Result:** ✅ Passed

---

## TC-HP-07 – Verify Copyright link in footer for non-logged-in users
**Jira Test Case:** [SSQ-12](https://storyspoilerqa.atlassian.net/browse/SSQ-12)  
**Use Case:** UC-HP-1 (Jira: [SSQ-2](https://storyspoilerqa.atlassian.net/browse/SSQ-2))

**Prerequisites:** TD-01: Guest Session.

**Steps:** 
1. Navigate to the app URL.  
2. Click “StorySpoil” link in the footer.  

**Expected Result:**  
User is redirected to the Copyright page.  

**Execution Result:** ❌ Failed

**Related Bug:** [BUG-HP-02](../bugs/bugs-report.md#bug-hp-02) (Jira: [SSQ-26](https://storyspoilerqa.atlassian.net/browse/SSQ-26))

---

## TC-HP-08 – Verify Home Page for logged-in users
**Jira Test Case:** [SSQ-13](https://storyspoilerqa.atlassian.net/browse/SSQ-13)  
**Use Case:** UC-HP-2 (Jira: [SSQ-3](https://storyspoilerqa.atlassian.net/browse/SSQ-3))

**Prerequisites:** TD-02: Valid User with existing Spoilers

**Steps:** 
1. Navigate to the app URL.  
2. Log in with TD-02.
3. Observe the Home Page layout. 

**Expected Result:**  
Home Page displays:
- Navigation bar on top
- Welcome message with username
- Search field with a search button
- Scrollable list of Spoilers
- Footer  

**Execution Result:** 🚫 Blocked

**Related Query:** [QRY-HP-01](../queries/queries.md#qry-hp-01) (Jira: [SSQ-27](https://storyspoilerqa.atlassian.net/browse/SSQ-27))

---

## TC-HP-09 – Verify navigation bar for logged-in users
**Jira Test Case:** [SSQ-14](https://storyspoilerqa.atlassian.net/browse/SSQ-14)  
**Use Case:** UC-HP-2 (Jira: [SSQ-3](https://storyspoilerqa.atlassian.net/browse/SSQ-3))

**Prerequisites:** TD-02: Valid user account exists.

**Steps:** 
1. Navigate to the app URL.  
2. Log in with TD-02.
3. Observe the navigation bar. 

**Expected Result:**  
Navigation bar is fixed and displays:  
- Profile + Home link (left)  
- “CREATE SPOILER” and “LOGOUT” buttons (right)  

**Execution Result:** ✅ Passed

---

## TC-HP-10 – Verify profile link in navigation bar
**Jira Test Case:** [SSQ-15](https://storyspoilerqa.atlassian.net/browse/SSQ-15)  
**Use Case:** UC-HP-2 (Jira: [SSQ-3](https://storyspoilerqa.atlassian.net/browse/SSQ-3))

**Prerequisites:** TD-02: Valid user account exists.

**Steps:** 
1. Navigate to the app URL.  
2. Log in with TD-02.
3. Click the Profile link in the navigation bar. 

**Expected Result:**  
User is redirected to My Profile page.  

**Execution Result:** ✅ Passed

---

## TC-HP-11 – Verify “STORYSPOIL” home link for logged-in users
**Jira Test Case:** [SSQ-16](https://storyspoilerqa.atlassian.net/browse/SSQ-16)  
**Use Case:** UC-HP-2 (Jira: [SSQ-3](https://storyspoilerqa.atlassian.net/browse/SSQ-3))

**Prerequisites:** TD-02: Valid user account exists.

**Steps:** 
1. Navigate to the app URL.  
2. Log in with TD-02.
3. Click the "STORYSPOIL" link in the navigation bar. 

**Expected Result:**  
Home Page reloads correctly. 

**Execution Result:** 🚫 Blocked

**Related Query:** [QRY-HP-02](../queries/queries.md#qry-hp-02) (Jira: [SSQ-28](https://storyspoilerqa.atlassian.net/browse/SSQ-28))

---

## TC-HP-12 – Verify “CREATE SPOILER” link in navigation bar
**Jira Test Case:** [SSQ-17](https://storyspoilerqa.atlassian.net/browse/SSQ-17)  
**Use Case:** UC-HP-2 (Jira: [SSQ-3](https://storyspoilerqa.atlassian.net/browse/SSQ-3))

**Prerequisites:** TD-02: Valid user account exists.

**Steps:** 
1. Navigate to the app URL.  
2. Log in with TD-02.
3. Click "CREATE SPOILER" link in the navigation bar. 

**Expected Result:**  
User is redirected to Create Spoiler page.  

**Execution Result:** ✅ Passed

---

## TC-HP-13 – Verify “LOGOUT” link in navigation bar
**Jira Test Case:** [SSQ-18](https://storyspoilerqa.atlassian.net/browse/SSQ-18)  
**Use Case:** UC-HP-2 (Jira: [SSQ-3](https://storyspoilerqa.atlassian.net/browse/SSQ-3))

**Prerequisites:** TD-02: Valid user account exists.

**Steps:** 
1. Navigate to the app URL.  
2. Log in with TD-02.
3. Click "LOGOUT" link in the navigation bar. 

**Expected Result:**  
User is logged out and redirected to Home Page for non-logged-in users.  

**Execution Result:** ✅ Passed

---

## TC-HP-14 – Verify Footer for logged-in users
**Jira Test Case:** [SSQ-19](https://storyspoilerqa.atlassian.net/browse/SSQ-19)  
**Use Case:** UC-HP-2 (Jira: [SSQ-3](https://storyspoilerqa.atlassian.net/browse/SSQ-3))

**Prerequisites:** TD-02: Valid user account exists.

**Steps:**  
1. Navigate to the app URL.
2. Log in with TD-02.
3. Observe the footer.  

**Expected Result:**  
Footer displays “Copyright © StorySpoil 2023”.  

**Execution Result:** ✅ Passed

---

## TC-HP-15 – Verify Copyright link in footer for logged-in users
**Jira Test Case:** [SSQ-20](https://storyspoilerqa.atlassian.net/browse/SSQ-20)  
**Use Case:** UC-HP-2 (Jira: [SSQ-3](https://storyspoilerqa.atlassian.net/browse/SSQ-3))

**Prerequisites:** TD-02: Valid user account exists.

**Steps:**  
1. Navigate to the app URL.
2. Log in with TD-02.
3. Observe the footer.  

**Expected Result:**  
User is redirected to Copyright page. 

**Execution Result:** ❌ Failed

**Related Bug:** [BUG-HP-02](../bugs/bugs-report.md#bug-hp-02) (Jira: [SSQ-26](https://storyspoilerqa.atlassian.net/browse/SSQ-26))

---

## TC-HP-16 – Verify Home Page with no spoilers
**Jira Test Case:** [SSQ-21](https://storyspoilerqa.atlassian.net/browse/SSQ-21)  
**Use Case:** UC-HP-3 (Jira: [SSQ-4](https://storyspoilerqa.atlassian.net/browse/SSQ-4))

**Prerequisites:** TD-03: New users account exists with no spoilers.

**Steps:**  
1. Navigate to the app URL.
2. Log in with TD-03.
3. Observe the Home Page. 

**Expected Result:**  
Home Page displays:
- Navigation bar on top
- Welcome message with username
- Search field with a search button
- Message: "No Spoilers Yet!"
- "WRITE SPOILER" button
- Footer 

**Execution Result:** ✅ Passed

---

## TC-HP-17 – Verify “WRITE SPOILER” button
**Jira Test Case:** [SSQ-22](https://storyspoilerqa.atlassian.net/browse/SSQ-22)  
**Use Case:** UC-HP-3 (Jira: [SSQ-4](https://storyspoilerqa.atlassian.net/browse/SSQ-4))

**Prerequisites:** TD-03: New users account exists with no spoilers.

**Steps:**  
1. Navigate to the app URL.
2. Log in with TD-03.
3. Click "WRITE SPOILER" on the Home page. 

**Expected Result:**  
User is redirected to Create Spoiler page.  

**Execution Result:** ✅ Passed

---

## TC-HP-18 – Verify Home Page access with no Internet connection
**Jira Test Case:** [SSQ-23](https://your-jira-instance.atlassian.net/browse/SSQ-TC-18)  
**Use Case:** UC-HP-4 (Jira: [SSQ-5](https://storyspoilerqa.atlassian.net/browse/SSQ-5))

**Prerequisites:** Internet is disabled.

**Steps:**  
1. Navigate to the app URL. 

**Expected Result:**  
App does not load, browser shows an error message like “No Internet” or “You are offline”.

**Execution Result:** ✅ Passed

---

## TC-HP-19 – Verify Home Page access with invalid/mistyped URL
**Jira Test Case:** [SSQ-24](https://storyspoilerqa.atlassian.net/browse/SSQ-24)  
**Use Case:** UC-HP-4 (Jira: [SSQ-5](https://storyspoilerqa.atlassian.net/browse/SSQ-5))

**Prerequisites:** User has Internet connection.

**Steps:**  
1. Open https://d3s5nxhwblsjbi.cloudfron.net (note typo).

**Expected Result:**  
App doesn't load, browser shows an error like “Site can’t be reached” / “DNS_PROBE_FINISHED_NXDOMAIN”.

**Execution Result:** ✅ Passed