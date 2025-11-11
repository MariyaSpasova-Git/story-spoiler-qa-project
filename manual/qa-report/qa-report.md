# 🧾 QA Summary Report – Story Spoiler

**Project:** Story Spoiler  
**Tester:** Mariya Spasova  
**Course:** QA Fundamentals and Manual Testing @ SoftUni  
**Testing Type:** Manual Functional Testing  
**Test Cycle:** Completed  
**Date:** October 2025  

---

## 🧠 Overview

This QA report summarizes the testing activities performed on the Story Spoiler web application. Testing covered six primary functional modules and included requirements review, test case design, execution, and defect logging.  

The focus of this report is to provide insights into application quality, defect distribution, and the main problem areas discovered during testing.

---

## 🧩 Scope of Testing

| **Phase** | **Description** |
|------------|----------------|
| **Requirements Review** | Analyzed 6 requirements for completeness, clarity, and testability. |
| **Test Case Design** | Designed 107 test cases covering main and alternative flows across all modules. |
| **Test Execution** | All test cases executed manually against the latest deployed build. |
| **Queries Logging** | 22 queries logged requiring clarification with the Product Owner. |
| **Bug Logging** | 9 unique bugs identified and logged in Jira, linked to corresponding test cases. |

---

## 📊 Test Execution Summary

| **Status** | **Count** | **Percentage** |
|-------------|-----------|----------------|
| ✅ Passed   | 71        | 66%            |
| ❌ Failed   | 6         | 6%             |
| 🚫 Blocked  | 30        | 28%            |
| **Total**   | **107**   | **100%**       |

---

### ⚠️ Blocked Test Cases Summary

A total of 30 test cases were blocked during execution, primarily due to two major unimplemented or broken features:

| **Root Cause** | **Description** | **Blocked Cases** |
|----------------|------------------|-------------------|
| 🟥 Missing “Share Spoiler” Button | The feature for sharing spoilers is not present in the tested build. This blocks testing related to social media sharing and validation of shared content. | 13 |
| 🟧 Non-functional “Edit Profile” Button | The Edit Profile button does not trigger any action, preventing validation of profile editing, field validation, and save/cancel behaviors. | 14 |
| ⚪ Other minor blockers | Miscellaneous UI issues and dependencies between features. | 3 |

**Total Blocked:** 30 test cases  

These two major issues account for 90% of all blocked tests, significantly affecting the ability to validate user interaction and profile management functionalities.

---

## 🐞 Bug Summary

A total of 9 bugs were identified during the testing phase.

| **Severity** | **Count** | **%** | **Priority** | **Count** | **%** |
|---------------|-----------|-------|---------------|-----------|-------|
| Critical      | 1         | 11%   | Critical      | 1         | 11%   |
| High          | 4         | 44%   | High          | 4         | 44%   |
| Medium        | 3         | 33%   | Medium        | 3         | 33%   |
| Low           | 1         | 11%   | Low           | 1         | 11%   |

The Registration module had the highest defect density (4 bugs), mostly related to validation logic.  
Major functional issues include:
- Search functionality not working (Critical)  
- Edit Profile button inactive (High – 14 blocked cases)  
- Missing “Share Spoiler” button (High – 13 blocked cases)  
- Footer link (Copyright) not redirecting (Medium)

📄 For full details, see [`manual/bugs/bug-report.md`](../bugs/bug-report.md).

---

## 📂 Bugs by Requirement (Feature Area)

| **Feature / Requirement** | **Bug IDs** | **Total** |
|----------------------------|-------------|-----------|
| Home Page (non-logged-in)  | BUG-HP-01, BUG-HP-02 | 2 |
| Registration               | BUG-REG-01, BUG-REG-02, BUG-REG-03, BUG-REG-04, BUG-HP-02 | 5 |
| Log In                     | BUG-LOG-01, BUG-HP-02 | 2 |
| Profile Management         | BUG-PROF-01, BUG-HP-02 | 2 |
| Spoiler Creation           | BUG-HP-02 | 1 |
| Spoiler Management         | BUG-SM-01, BUG-SM-02, BUG-HP-02 | 3 |

> **Note:** BUG-HP-02 affects all pages but is referenced once per affected module for visibility.

---

## 🧮 Defect Density

| **Module** | **# of Test Cases** | **# of Bugs** | **Defect Density** |
|-------------|--------------------|---------------|--------------------|
| Home Page | 20 | 2 | 0.10 |
| Registration | 23 | 5 | 0.22 |
| Login | 6 | 2 | 0.33 |
| Profile Management | 17 | 2 | 0.12 |
| Spoiler Creation | 10 | 1 | 0.10 |
| Spoiler Management | 31 | 3 | 0.30 |
| **Total** | **107** | **15 (includes cross-module)** | **0.20 (Avg)** |

---

## 🧭 Conclusion

Overall, the Story Spoiler application demonstrates acceptable stability for a beta version.  
While core flows such as registration, login, and logout are functional, several usability and feature gaps reduce the overall product completeness.  

**Main improvement recommendations:**
1. Implement the missing “Share Spoiler” functionality to unblock related tests.  
2. Fix the “Edit Profile” button to enable profile data updates and field validation testing.  
3. Strengthen form validation across all input fields.  
4. Fix global footer links for consistent navigation.  
5. Ensure search and edit functions are fully implemented.  
6. Add automated regression coverage for high-risk flows in future iterations.  

---

## ✅ Summary Snapshot

- **Requirements Reviewed:** 6  
- **Test Cases Designed:** 107  
- **Bugs Logged:** 9  
- **Test Pass Rate:** 66%  
- **Defect Density:** 0.20  
- **Modules Tested:** 6  
- **Blocked Tests:** 30 
