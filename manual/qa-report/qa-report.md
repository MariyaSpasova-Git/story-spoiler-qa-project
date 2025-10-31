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
| **Test Case Design** | Designed 106 test cases covering main and alternative flows across all modules. |
| **Test Execution** | All test cases executed manually against the latest deployed build. |
| **Queries Logging** | 22 queries logged requireing clarification with the Product Owner.
| **Bug Logging** | 9 unique bugs identified and logged in Jira, linked to corresponding test cases. |

---

## 📊 Test Execution Summary

| **Status** | **Count** | **Percentage** |
|-------------|-----------|----------------|
| ✅ Passed   | 70       | 66%            |
| ❌ Failed   | 6         | 6%            |
| 🚫 Blocked  | 30         |28%             |
| **Total**   | **45**    | **100%**       |

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
- Edit Profile button inactive (High)
- Footer link (Copyright) not redirecting (Medium)

📄 For full details, see [`manual/bugs/bug-report.md`](../bugs/bug-report.md).

---

## 📂 Bugs by Requirement (Feature Area)

| **Feature / Requirement** | **Bug IDs** | **Total** |
|----------------------------|--------------|-----------|
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
| Home Page | 19 | 2 | 0.11 |
| Registration | 23 | 5 | 0.22 |
| Login | 6 | 2 | 0.33 |
| Profile Management | 17 | 2 | 0.12 |
| Spoiler Creation | 10 | 1 | 0.10 |
| Spoiler Management | 31 | 3 | 0.30 |
| **Total** | **106** | **14** | **0.20 (Avg)** |

---

## 🧭 Conclusion

Overall, the Story Spoiler application demonstrates acceptable stability for a beta version.  
While core flows such as registration and login are functional, several usability and validation issues reduce the overall product quality.  

**Main improvement recommendations:**
1. Strengthen form validation across all input fields.
2. Fix global footer links for consistent navigation.
3. Ensure edit functionality and search are fully implemented.
4. Add automated regression coverage for high-risk flows in future iterations.

---

## ✅ Summary Snapshot

- **Requirements Reviewed:** 6  
- **Test Cases Designed:** 106  
- **Bugs Logged:** 9  
- **Test Pass Rate:** 66%  
- **Defect Density:** 0.20  
- **Modules Tested:** 6  