# Test Data

This file contains **anonymized, reusable test data** for manual and exploratory testing.  
Each test case references the corresponding **Test Data ID (TD-XX)** for consistency and traceability.  

> ⚠️ All credentials and URLs below are dummy values for testing purposes only.

---

## Test Data Versioning Policy
Test Data IDs (TD-XX) are maintained incrementally to preserve traceability across all linked test cases and Jira issues.  
Non-sequential numbering reflects iterative updates and requirement expansions over time.  
Each TD-ID remains unique and permanently associated with its original test case, ensuring full auditability and version control integrity.

---

## Usage Guidelines
* Each **TD-XX** identifier is referenced in one or more test cases.  
* When data is updated or deprecated, keep the original ID and mark the new data with a new TD number.  
* Avoid redefining empty fields — specify “Leave the field empty” directly in test steps unless the empty state has business meaning (e.g., optional fields or boundary conditions) or is reused across multiple tests.  
* Long-string test data (e.g., 61 or 401 characters) are represented by placeholder characters for simplicity — only the **length** matters.

---

## 🏠 Home Page Test Data

### TD-01 – Guest Session
* No active user session  
* Browser cache and cookies cleared  

### TD-02 – Valid User 1
* Username: `test_user_1`  
* Password: `123456`  
* Existing spoilers and user profile  

### TD-03 – Valid User 2 (New Account)
* Username: `new_test_user`  
* Password: `123456`  
* No spoilers or user profile  

### TD-04 – Invalid User
* Username: `invalid_user`  
* Password: `123456`

---

## 👤 User Registration Test Data

### TD-05 – Invalid Username (1 character)
**Value:** `a`  
**Note:** Below minimum length (2 characters)

### TD-06 – Invalid Username (31 characters)
**Value:** `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`  
**Note:** Above maximum length (30 characters)

### TD-07 – Valid Username
**Value:** `qa_user_01`

---

### TD-09 – Valid Email
**Value:** `testuser@example.com`

### TD-10 – Invalid Email (missing '@')
**Value:** `userexample.com`

### TD-11 – Invalid Email (missing '.')  
**Value:** `user@examplecom`

### TD-12 – Invalid Email (5 characters)
**Value:** `a@b.c`  
**Note:** Below minimum length (6 characters)

### TD-13 – Invalid Email (255 characters)
**Value:** `user@example.commmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmmm`  
**Note:** Above maximum length (254 characters)

---

### TD-14 – Valid First Name
**Value:** `John`

### TD-15 – Invalid First Name (1 character)
**Value:** `A`

### TD-16 – Invalid First Name (61 characters)
**Value:** `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA`  
**Note:** Above maximum length (60 characters)

---

### TD-17 – Valid Last Name
**Value:** `Smith`

### TD-18 – Invalid Last Name (1 character)
**Value:** `B`

### TD-19 – Invalid Last Name (61 characters)
**Value:** `LLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLL`

---

### TD-20 – Valid Password
**Value:** `1234567`

### TD-21 – Valid Repeat Password (matches TD-20)
**Value:** `1234567`

### TD-22 – Invalid Password (5 characters)
**Value:** `12345`  
**Note:** Below minimum length (6 characters)

### TD-23 – Invalid Password (31 characters)
**Value:** `ppppppppppppppppppppppppppppppp`

### TD-24 – Invalid Repeat Password (mismatch)
**Value:** `DifferentPass`

---

### TD-25 – Invalid Middle Name (1 character)
**Value:** `M`

### TD-26 – Invalid Middle Name (61 characters)
**Value:** `MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM`

### TD-27 – Valid Middle Name
**Value:** `Doe`

### TD-28 – Empty Middle Name (valid, optional)  
Used in tests validating optional fields.

---

### TD-29 – Valid Email (registered account)
**Value:** `test_user_1@example.com`

### TD-30 – Invalid Email (missing '@' and '.')
**Value:** `exampleemail`

---

### TD-31 – Invalid User (valid username + wrong password)
* Username: `test_user_1`
* Password: `wrongpass123`

### TD-32 – Empty Credentials
* Username: *(empty)*
* Password: *(empty)*

---

## 🧑‍💻 Profile Management Test Data

### TD-33 – Valid Picture URL
**Value:** `http://example.com/test-image.jpg`

### TD-34 – Invalid Picture URL (malformed)
**Value:** `pictureimage`

### TD-35 – Invalid Picture URL (missing protocol)
**Value:** `example.com/image.png`

### TD-36 – Invalid Picture URL (missing file extension)
**Value:** `http://example.com/image`

### TD-37 – Invalid Picture URL (wrong extension)
**Value:** `http://example.com/image.txt`

---

### TD-38 – Valid About Me Description
**Value:** `Dedicated QA tester with a passion for software quality assurance.`

### TD-39 – Invalid About Me Description (257 characters)
**Value:** `DDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDD`

---

## 📚 Spoiler Creation and Edit Test Data

### TD-40 – Valid Story Title
**Value:** `Unexpected Ending`

### TD-41 – Valid Story Description
**Value:** `The hero discovers that the villain is his father.`

### TD-42 – Empty Picture URL
Used to verify optional Picture URL field during Spoiler creation or edit.

### TD-43 – Invalid Story Title (71 characters)
**Value:** `SSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSS`  
**Note:** Above maximum length (70 characters)

### TD-44 – Invalid Story Description (401 characters)
**Value:** `DDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDD`

---

### TD-45 – Valid Message
**Value:** `Check out this amazing spoiler!`
**Note:** Assumed maximum length of 100 characters

### TD-46 – Valid Email
**Value:** `testfriend@example.com`

### TD-47 – Valid Name
**Value:** `Alex` 
**Note:** Assumed maximum length of 70 characters

---

### TD-48 – Invalid Email (leading/trailing spaces)
**Value:** `example@email.com`

### TD-49 – Invalid Email (missing username)
**Value:** `@example.com`

### TD-50 – Invalid Email (missing domain name)
**Value:** `user@.com`

### TD-51 – Invalid Email (missing host)
**Value:** `user@example.`

### TD-52 – Invalid Email (multiple '@' symbols)
**Value:** `user@@example.com`

---

### TD-53 – Valid Spoiler Title
**Value:** `Forest Story`

### TD-54 – Invalid Spoiler Title (not existing)
**Value:** `xyz123`

---

### TD-55 – Invalid Message (101 characters)
**Value:** `MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM`  
**Note:** Above maximum length (assumed maximum length of 100 characters)

### TD-56 – Invalid Name (70 characters)
**Value:** `NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN`  
**Note:** Above maximum length (assumed maximum length of 70 characters)


## 🔗 Linking Notes

This test data is referenced in:

- [Test Cases – Home Page](./test-cases-home-page.md)  
- [Test Cases – User Registration](./test-cases-user-registration.md)  
- [Test Cases – Log In Page](./test-cases-log-in-page.md)  
- [Test Cases – User Profile Management](./test-cases-user-profile-management.md)  
- [Test Cases – Spoiler Creation](./test-cases-spoiler-creation.md)
- [Test Cases – Spoiler Management](./test-cases-spoiler-management.md)

---