# Manual QA Project (Story Spoiler)

> Comprehensive manual QA testing of the Story Spoiler demo web application — 107 test cases executed, 9 bugs, and 22 queries logged. Full documentation includes detailed test cases, bug reports, API validation, and a final QA summary.

---

## Project Overview

This repository contains all Quality Assurance artifacts for the Story Spoiler web application — a platform where registered users can create, manage, and share short, story-based content.

The project was completed as part of the QA Fundamentals and Manual Testing course at Software University and serves as a professional portfolio piece, showcasing an end-to-end QA workflow — from requirements analysis and test design through to defect reporting and API testing.

---

## Project Goal

The primary goal of this QA initiative is to verify that the Story Spoiler application functions as intended across its six core use cases. This includes:

- Designing comprehensive test cases for each use case.  
- Executing all test cases to validate expected behavior.  
- Logging and documenting bugs and queries in detail.  
- Maintaining traceability between requirements, test cases, and defects.  
- Performing API validation through Postman requests.

---

## Key Findings

The completed testing cycle is summarized in the [qa-report.md](manual/qa-report/qa-report.md):

- **Total Test Cases Executed:** 107  
- **Total Bugs Logged:** 9  
- **Total Queries Logged:** 22  
- **API Endpoints Tested:** 5
- **API Tests Passed:** 5

Overall, the Story Spoiler application demonstrates stable core functionality with a few minor API response and UI issues identified and documented.

---

### QA Results Summary

| Metric | Result |
|--------|--------|
| **Total Test Cases** | 107 |
| **Passed** | 71 (66%) |
| **Failed** | 6 (6%) |
| **Blocked** | 30 (28%) |
| **Bugs Logged** | 9 |
| **Defect Density** | 0.20 |

---

## Tools and Technologies

| Category | Tools |
|-----------|--------|
| **Project Management & Bug Tracking** | Jira |
| **Version Control** | Git, GitHub |
| **API Testing** | Postman |
| **Documentation** | Markdown, Canva |
| **Test Design & Execution** | Manual Functional and UI Testing |
| **Development Tools** | Visual Studio Code |

---

## Test Environment

- **Application URL:** https://d3s5nxhwblsjbi.cloudfront.net/  
- **Component:** Specification  
- **Operating System:** Microsoft Windows 11 Pro (64-bit)  
- **Browser:** Google Chrome 140.0.7339.128 (64-bit)  
- **Jira Site:** https://storyspoilerqa.atlassian.net  
- **GitHub Repo:** https://github.com/MariyaSpasova-Git/story-spoiler-qa-project  

---

## Security Note

For privacy and security reasons, no real user data was used during testing. All test accounts, usernames, and passwords were dummy values created solely for this project. The images and API test data (e.g., spoiler names and descriptions) are also fictional.

---

## Project Directory Structure

The project structure below illustrates how artifacts are organized. This is typically generated using the tree command in a Unix-like environment, or manually structured for clarity.

```
Story-Spoiler-QA-Project/
├── api/
│ ├── specs/
│ │ └── api-specification.md                        # Detailed endpoint documentation
│ ├── requests/
│ │ ├── storyspoiler-api.postman_collection.json    # Postman collection
│ │ ├── storyspoiler-env.postman_environment.json   # Environment variables
│ │ └── postman-collection.md                       # Overview and test summary
│ ├── test-cases/                                   # API test case documentation
│ └── bugs/                                         # API-related bug reports
├── docs/
│ ├── screenshots/                                  # Screenshots for bugs and queries
│ └── mind-map/                                     # Mind map
└── manual/
├── requirements/                                   # Functional requirements
├── use-cases/                                      # Use case documentation
├── test-cases/                                     # Manual test cases by feature
├── test-data/                                      # Test data documentation
├── queries/                                        # Queries and clarifications
├── bugs/                                           # Manual bug reports
└── qa-report/                                      # Final QA Summary Report
```
---

## Getting Started

To fully interact with the QA documentation and API test artifacts:

1. **Clone the Repository**
   ```bash
   git clone https://github.com/MariyaSpasova-Git/story-spoiler-qa-project

2. Open in Visual Studio Code
Browse documentation or preview Markdown files directly.

3. API Testing (Optional)
- Import the Postman collection from `/api/requests/`.
- Import the environment file (`storyspoiler-env.postman_environment.json`).
- Run the collection to validate the endpoints.

4. Jira Integration (Optional)
- Ensure you have the Story Spoiler QA Project set up in your Jira site.
- Use the issue types Requirement, Use Case, Test Case, Bug, and Query.
- Verify the link between your Jira project and this GitHub repository. This allows commits containing the Jira issue key to appear directly on the Jira ticket for seamless traceability.

## Contact

For any questions or feedback, please feel free to reach out.

* **Name:** Mariya Spasova
* **GitHub:** https://github.com/MariyaSpasova-Git
* **Email:** mariyaspasova3@gmail.com
