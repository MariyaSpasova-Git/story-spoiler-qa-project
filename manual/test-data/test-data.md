# Test Data

This file contains **anonymized test data** for manual test cases.
Each test case references the corresponding **Test Data ID (TD-XX)**.

> ⚠️ All credentials below are dummy values for testing only.

---

## Home Page Test Data

### TD-01 – Guest Session
* No active user session
* Browser cache and cookies cleared

### TD-02 – Valid User 1
* Username: `test_user_1`
* Password: `123456`
* Existing spoilers available
* Existing user profile

### TD-03 – Valid User 2 (New Account)
* Username: `new_test_user`
* Password: `123456`
* No spoilers yet
* No user profile yet

### TD-04 – Invalid User
* Username: `invalid_user`
* Password: `123456`

---

## User Registration Test Data

### TD-05 – Invalid Username (1 character)
**Value:** `a`
**Note:** Below minimum length (2 characters)

### TD-06 – Invalid Username (31 characters)

**Value:** `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`
**Note:** Above maximum length (30 characters)

### TD-07 – Valid Username
**Value:** `qa_user_01`

### TD-08 – Empty Username
**Value:** ``

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
**Note:** Below minimum length (2 characters)

### TD-16 – Invalid First Name (61 characters)
**Value:** `AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA` *(61 characters)*
**Note:** Above maximum length (60 characters)

---

### TD-17 – Valid Last Name
**Value:** `Smith`

### TD-18 – Invalid Last Name (1 character)
**Value:** `B`
**Note:** Below minimum length (2 characters)

### TD-19 – Invalid Last Name (61 characters)
**Value:** `LLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLL` *(61 chars)*
**Note:** Above maximum length (60 characters)

---

### TD-20 – Valid Password
**Value:** `1234567`
**Constraints:** 6–30 characters

### TD-21 – Valid Repeat Password (matches TD-19)
**Value:** `1234567`

### TD-22 – Invalid Password (5 characters)
**Value:** `12345`
**Note:** Below minimum length (6 characters)

### TD-23 – Invalid Password (31 characters)
**Value:** `ppppppppppppppppppppppppppppppp`
**Note:** Above maximum length (30 characters)

### TD-24 – Invalid Repeat Password (mismatch)
**Value:** `DifferentPass`

---

### TD-25 – Invalid Middle Name (1 character)
**Value:** `M`
**Note:** Below minimum length (2 characters)

### TD-26 – Invalid Middle Name (61 characters)
**Value:** `MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM`
**Note:** Above maximum length (60 characters)

### TD-27 – Valid Middle Name
**Value:** `Doe`

### TD-28 – Empty Middle Name (valid, optional)
**Value:** ``

### TD-29 – Valid Email (registered account)
**Value:** `test_user_1@example.com`

### TD-30 – Invalid Email (missing '@' and '.')
**Value:** `exampleemail`

### TD-31 – Invalid User (valid username with incorrect password)
* Username: `test_user_1`
* Password: `wrongpass123`

### TD-32 – Empty Credentials
* Username: ``
* Password: ``

### TD-33 – Valid Picture URL
* **Value:** `http://example.com/test-image.jpg`

### TD-34 Invalid Picture URL (invalid URL structure)
**Value:** `pictureimage`

### TD-35 Invalid Picture URL (missing protocol)
**Value:** `example.com/image.png`

### TD-36 Invalid Picture URL (missing file extension)
**Value:** `http://example.com/image`

### TD-37 Invalid Picture URL (wrong extension)
**Value:** `http://example.com/image.txt`

### TD-38 Valid About Me Description
**Value:** `Dedicated QA tester with a passion for software quality assurance.`

### TD-39 – Invalid About Me description (257 characters)
**Value:** `DDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDD`
**Note:** Above maximum length (256 characters)

---

### TD-40 Valid Story Title
**Value:** `Unexpected Ending`

### TD-41 Valid Story Description
**Value:** `The hero discovers that the villain is his father`

### TD-42 – Empty Picture URL
**Value:** ``

### TD-43 – Invalid Story Title (71 characters)
**Value:** `SSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSS`
**Note:** Above maximum length (60 characters)

### TD-44 – Invalid Story Description (401 characters)
**Value:** `DDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDDD`
**Note:** Above maximum length (400 characters)

## Usage Notes

* Test cases reference TD-IDs directly (e.g., **Enter TD-09** for valid email).
* Long-string test data (61 / 31 chars) use placeholder values, length is what matters.
* This file is kept synchronized with all test case documents.


## 🔗 Linking
This test data is referenced in:  

- [Test Cases – Home Page](./test-cases-home-page.md)