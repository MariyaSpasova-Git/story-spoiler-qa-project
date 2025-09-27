# Story Spoiler Application System Requirements
NOTE: This document is a concise summary of the functional requirements. The original, full requirements document is a copyrighted work used solely for educational and QA practice purposes.

## 1. Introduction

### 1.1. Purpose and Scope

This document details the core front-end functionalities of the Story Spoiler web application and serves as the primary reference for all QA activities (test case design, use cases, and defect logging).

The scope covers the main user workflows: User Registration, Login, Profile Management, Spoiler Creation, and Spoiler Management. It excludes special user roles (e.g., Administrator) and backend API details.

## 2. Overall System Description

### 2.1. Environment and Actors
The application is hosted at https://d3s5nxhwblsjbi.cloudfront.net/.

Unregistered Users: Access restricted to the Home Page, Sign Up, and Log In pages.

Registered Users: Access all main features, including Profile Management and Spoiler functionality.

## 3. Functional Requirements

### 3.1. Authentication: User Registration (Sign Up Page)
The Sign Up page includes a form with the following fields, constraints, and requirements:

| Field | Requirement | Constraint | Required | 
| :--- | :--- | :--- | :--- | 
| **Username** | Accepts all character types. | 2–30 characters | Yes | 
| **Email** | Must be a valid email format. | 6–254 characters | Yes | 
| **First Name** | Accepts all character types. | 2–60 characters | Yes | 
| **Middle Name** | Accepts all character types. | 2–60 characters | No | 
| **Last Name** | Accepts all character types. | 2–60 characters | Yes | 
| **Password** | Any characters are acceptable. | 6–30 characters | Yes | 
| **Repeat Password** | Must exactly match the Password field. | N/A | Yes |

- **Navigation**: Includes a LOG IN HERE button to redirect to the Log In page.

### 3.2. Authentication: Log In and Navigation

- **Log In Page**: Requires Username and Password fields. Includes a Forgot password link and a CREATE NEW button (leading to Sign Up).

- **Home Page (Non-Logged User)**: Navbar includes StorySpoil Home Page link, SIGN UP, and LOG IN buttons. Includes promotional content and a Copyright Footer that links to a dedicated copyright page.

- **Home Page (Logged-In User)**: Navbar includes Profile and Home links on the left, and CREATE SPOILER and LOGOUT on the right.

### 3.3. Content Management and Search (Logged-In User)

- **Search Functionality**: Filters spoilers by their title. If no spoilers are found, it displays "No Spoilers Yet!" and a WRITE SPOILER button.

- **Spoiler Display**: New spoilers are displayed on the Home Page with SHARE, EDIT, and DELETE buttons.

### 3.4. Profile Management Requirements

**My Profile Page**

- **Display**: Shows an empty profile picture (default), Username, Full Name, Email, Total spoilers counter (default zero), and the About Me section.

- **Default Text**: About Me defaults to "You haven’t written anything about yourself…".

- **Navigation**: Includes an EDIT button.

**Edit Profile Info Page**

- **Access**: Accessible from the EDIT button.

- **Editable Fields and Constraints**:

    - **Profile Picture**: Must be a valid picture URL (e.g., http://......jpg).

    - **First Name, Middle Name, Last Name**: Maximum 60 characters each.

    - **About me**: Maximum 256 characters.

### 3.5. Spoiler Creation and Management Constraints

**Create Spoiler Page**
- **Access**: Via the CREATE SPOILER link on the Navbar.

- **Fields and Constraints**:

    - **Story Title**: Maximum 70 characters.

    - **Describe your story spoiler**: Maximum 400 characters.

    - **Add a picture for the spoiler**: Must be a valid picture URL.

- **Workflow**: Clicking CREATE redirects to the Logged-In Home page.

**Story Spoiler Management**
- **Actions**: Each spoiler features SHARE, EDIT, and DELETE buttons.

- **Delete**: Clicking DELETE permanently removes the spoiler.