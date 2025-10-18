# Story Spoiler Project – Jira Hierarchy Overview

This document illustrates the traceability structure used for the Story Spoiler QA project.

## 🔗 QA Item Relationships

The following hierarchy defines how project artifacts are related in Jira:

```
📘 Requirement (Epic)
│
├── 📗 Use Case (custom issue type)
│ │
│ ├── 📄 Test Case (Sub-task)
│ │ │
│ │ ├── 🐞 Bug (linked to failing test case)
│ │ └── ❓ Query (linked to test case for missing or unclear requirements)
│ │
│ └── ❓ Query (linked directly to use case when functionality is unclear)
│
└── 🔗 (All items linked in Jira through issue relationships)
```

## 📘 Example Workflow

1. **Requirement (Epic)**  
   Defines a key system feature, e.g., *Spoiler Management*.

2. **Use Case**  
   Describes how a user interacts with a specific functionality within the requirement.

3. **Test Case (Sub-task)**  
   Validates the behavior described in the use case. Each test case corresponds to one scenario.

4. **Bug**  
   Created when a test case fails. Linked back to the failed test case.

5. **Query**  
   Created when a requirement or use case lacks information or clarity.  
   Queries can be linked directly to the related Use Case or Test Case.

## 🧭 Traceability Example (Simplified)

Requirement → Use Case → Test Case → Bug / Query

## ✅ Key Notes

- This structure ensures traceability between requirements, use cases, tests, and defects.  
- Queries represent missing or ambiguous information, not test failures.  
- Each level provides clear visibility of test coverage.  
- The structure is simplified for educational and portfolio purposes.
