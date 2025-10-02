# Queries – Home Page

This document lists all open queries identified during requirements and test case analysis.
Each query has a unique ID (QRY-HP-XX), is linked to Jira, and references the related test case(s).

---

## QRY-HP-01 – Requirements for Home Page for logged in users lack visuals and detailed content specification

**Jira query:** [SSQ-27](https://storyspoilerqa.atlassian.net/browse/SSQ-27)

**Related Test Case:** [TC-HP-08](../tests/test-cases-home-page.md#tc-hp-08) (Jira link: [SSQ-13](https://storyspoilerqa.atlassian.net/browse/SSQ-13)) – Verify Home Page for logged-in users  

**Description:**
The original requirement document for the **Home Page (Logged-in User)** is incomplete. It lacks visuals and detailed text specification. Without them, developers and testers cannot reliably build or validate the feature.

**Steps to Identify:**

1. Open the oiginal requirements document.
2. Navigate to the section "Home Page (Logged-in User)".

**Expected:**
The requirement should contain a clear visual alongside a detailed description of:

* Page title and welcome message
* Content and layout of the body
* Labels/icons for navigation (Home, Profile, etc.)

**Actual:**

* No visuals provided
* Text description is incomplete and ambiguous

**Status:** ⏳ Open

---

## QRY-HP-02 – Home Page for logged-in users navigation link label

**Jira Query:** [SSQ-28](https://storyspoilerqa.atlassian.net/browse/SSQ-28)

**Related Test Case:** [TC-HP-11](../tests/test-cases-home-page.md#tc-hp-11) (Jira link: [SSQ-16](https://storyspoilerqa.atlassian.net/browse/SSQ-16)) – Verify "STORYSPOIL" home link for logged-in users

**Description:**
Original requirement document states the navigation bar should display “**StorySpoil**” (mixed case), but both the mockup and current implementation show “**STORYSPOIL**” (all caps).

**Steps to Identify:**

1. Open the original requirement document.
2. Compare with the attached mockup.
3. Verify the implemented navigation bar in the app.

**Expected:**
Text formatting should be consistent between requirement, design mockup, and implementation.

**Actual:**
Requirement text differs from both design and implementation.

**Status:** ⏳ Open

---
