# 📘 Story Spoiler API Testing – Postman Collection

## Purpose
This document provides an overview of the Postman API testing setup for the Story Spoiler project. The goal is to verify the functionality, reliability, and behavior of the application’s RESTful API through manual testing in Postman. All API endpoints were validated to ensure correct responses, authentication handling, and data consistency across the system.

---

## Files Overview

| File | Description |
|------|--------------|
| **`storyspoiler-api-tests.postman_collection.json`** | Postman collection containing all API requests for Story Spoiler. |
| **`storyspoiler-env.postman_environment.json`** | Postman environment file defining the base variable `host`. |

---

## Import Instructions

1. Open Postman → Go to **File → Import**.  
2. Import both files:  
   - `storyspoiler-api-tests.postman_collection.json`  
   - `storyspoiler-env.postman_environment.json`
3. Select the environment "Story Spoiler Environment" from the dropdown at the top right.  
4. Verify that the environment variable is set correctly:
   - `host` → `https://d3s5nxhwblsjbi.cloudfront.net`

---

## Executed API Tests

| # | Request Name | Method | Endpoint | Authorization | Result |
|---|---------------|---------|-----------|----------------|----------|
| 1 | **Authenticate User** | `POST` | `/api/User/Authentication` | None | ✅ Passed |
| 2 | **Create New Spoiler** | `POST` | `/api/Story/Create` | Bearer Token | ✅ Passed |
| 3 | **List All Spoilers** | `GET` | `/api/Story/All` | Bearer Token | ✅ Passed |
| 4 | **Change Spoiler Title** | `PUT` | `/api/Story/Edit/{storyId}` | Bearer Token | ✅ Passed |
| 5 | **Delete Spoiler** | `DELETE` | `/api/Story/Delete/{storyId}` | Bearer Token | ✅ Passed |

---

## Test Data Used

| Field | Example Value |
|--------|----------------|
| **Username** | `test_user_1` |
| **Password** | `123456` |
| **New Spoiler Title** | `The Final Chapter` |
| **New Spoiler Description** | `The detective finally uncovers the truth behind the missing manuscript, changing everything we thought we knew.` |
| **New Spoiler Picture URL** | `https://example.com/xyzSpoilerCover.jpg` |
| **Updated Spoiler Title** | `The Final Chapter Edited` |

**🔐 Security Note**
All test data used in this collection is dummy and fictional. 
- No real user accounts, personal data, or sensitive information were used.  
- The image URL points to a placeholder stock image and does not represent real content.  
- Credentials and tokens are for QA testing purposes only.

---

## Summary of Findings
All five endpoints responded with the expected status codes and payload structures. Authorization headers worked as intended, and CRUD operations were validated end-to-end. No API defects were detected during testing.

---

## Notes
- The `accessToken` is automatically obtained after a successful login and must be reused in all authorized requests.  
- The API is stateless; deleting a spoiler permanently removes it from your user scope.  
- Future test cases may include negative testing, boundary validation, and invalid token scenarios.

---

*Created and verified as part of the Story Spoiler Manual QA Project.*  
*Testing completed: November 2025*  
*Author: Mariya Spasova*
