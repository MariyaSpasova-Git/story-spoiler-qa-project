# Manual QA Project (Story Spoiler)

## Project Overview

This repository contains all the Quality Assurance artifacts for the "Story Spoiler" web application, a platform designed for registered users to create, manage, and share short, story-based content. The project was completed as part of the QA Fundamentals and Manual Testing course at Software University and serves as a professional portfolio piece, showcasing an end-to-end QA workflow from requirements analysis and test case design through to bug logging, management, and final reporting.

## Project Goal

The primary goal of this QA initiative is to ensure the Story Spoiler application functions exactly as expected, according to the provided six core use cases. This involves:

- Developing a complete set of Test Cases for each use case.

- Executing all Test Cases to confirm or deny expected functionality.

- Detecting and documenting all identified bugs in detail.

- Maintaining traceability between requirements (Use Cases), testing (Test Cases), and defects (Bug Reports).

## Key Findings

This section will be populated upon the completion of the testing cycle. It will reference the final qa-report.md and summarize the overall quality status of the Story Spoiler application, including:

- **Total Test Cases Executed** (Passed/Failed/Blocked)

- **Total Bugs Logged** (Categorized by Severity and Priority)

- **Major functional or systemic issues identified**.

## Tools and Technologies

- **Project Management & Bug Tracking**: Jira (Used for managing Use Cases, Test Cases, and Bug Reports.)

- **Version Control**: GitHub (Used for documentation, history tracking, and integrating with Jira via Smart Commits.)

- **Documentation**: Markdown

- **Testing Approach**: Manual Functional Testing

## Test Environment

- **Application URL**: https://d3s5nxhwblsjbi.cloudfront.net/

- **Component**: Specification

- **Operating System**: Microsoft Windows 11 Pro (64-bit)

- **Browser**: Version 140.0.7339.128 (Official Build) (64-bit)

- **Jira Site**: https://storyspoilerqa.atlassian.net

- **GitHub Repo**: https://github.com/MariyaSpasova-Git/story-spoiler-qa-project

## Security Note

For security and privacy reasons, all test usernames and passwords used during the execution process have been intentionally omitted from the test cases and bug reports in this repository. All tests were executed using a set of valid credentials that are managed separately.

## Project Directory Structure

The project structure below illustrates how artifacts are organized. This is typically generated using the tree command in a Unix-like environment, or manually structured for clarity.

```
Story-Spoiler-QA-Project/
├── api/
│   ├── bugs/               # API bug reports
│   ├── specs/              # API specifications and documentation
│   ├── requests/           # Postman collection files for API testing
│   └── test-cases/         # API Test Cases
├── docs/
│   └── mind-map/           # Visual aids, like mind maps or flowcharts
└── manual/
    ├── bugs/               # Detailed manual bug reports
    ├── qa-report/          # The final QA Summary Report
    ├── requirements/       # Detailed System Requirements
    ├── test-cases/         # Manual Test Cases grouped by functionality
    └── use-cases/          # Use Case documentation
```
## Getting Started

To fully interact with the QA artifacts and project management workflow, you should follow these steps:

- **Clone the Repository**:
git clone https://github.com/MariyaSpasova-Git/story-spoiler-qa-project

- **Jira Setup**: Ensure you have the Story Spoiler QA Project set up in your Jira site. Use the issue types Requirement, Use Case, Test Case, and Bug.

- **Jira & GitHub Integration**: Verify the link between your Jira project and this GitHub repository. This allows commits containing the Jira issue key to appear directly on the Jira ticket for seamless traceability.

## Contact

For any questions or feedback, please feel free to reach out.

* **Name:** Mariya Spasova
* **GitHub:** https://github.com/MariyaSpasova-Git
* **Email:** mariyaspasova3@gmail.com
