# Test Strategy

## Objective

The objective of this testing strategy is to validate the most critical business areas of OrangeHRM using a risk-based testing approach. Testing efforts will focus on modules that directly impact system access, employee management, security, and core business operations.

The strategy aims to reduce business risk through a combination of UI, API, and data validation activities while prioritizing the areas identified as highest priority during the risk assessment phase.

## Testing Approach

| Module                 | Testing Approach                                                              |
| ---------------------- | ----------------------------------------------------------------------------- |
| Login & Authentication | UI Testing, Negative Testing, Session Management Validation, Input Validation |
| Employee Management    | UI Testing, API Validation, Data Integrity Validation, End-to-End Testing     |
| Roles & Permissions    | Authorization Testing, Security Validation, Negative Testing                  |
| Recruitment            | Workflow Validation, UI Testing, End-to-End Testing                           |
| Leave Management       | Workflow Validation, Approval Process Validation, Business Rules Validation   |
| My Info                | Data Validation, Profile Update Validation, Data Persistence Validation       |

## Test Levels

### UI Testing

UI testing will be used to validate user interactions, navigation flows, form behavior, error messages, and overall user experience.

### API Testing

API testing will be used to validate request and response behavior, business rules, data exchange, and service reliability.

### Data Validation

Data validation activities will verify that information remains accurate, consistent, and properly persisted after business operations are performed.

## Automation Strategy

Automation efforts will focus on repetitive, high-risk, and business-critical workflows that provide the highest return on investment.

The initial automation scope includes:

* Login & Authentication
* Employee Management
* Recruitment
* Leave Management
* My Info

These modules were selected because they represent critical business processes and are expected to be executed frequently throughout the testing lifecycle.

## Risk-Based Prioritization

Testing activities will follow the priorities established during the risk assessment process.

### Priority 1 (P1)

* Login & Authentication
* Employee Management
* Roles & Permissions
* Recruitment

These modules will receive the highest testing coverage and will be prioritized for smoke testing, regression testing, and automation activities.

### Priority 2 (P2)

* Leave Management
* Reporting

These modules will receive regression coverage and targeted validation based on business risk.

## Entry Criteria

Testing activities may begin when:

* The test environment is available.
* Required user accounts are accessible.
* Test data is available.
* Scope and testing strategy have been approved.

## Exit Criteria

Testing activities will be considered complete when:

* All Priority 1 scenarios have been executed.
* No critical defects remain open.
* Planned automation scenarios execute successfully.
* Test evidence and reports have been generated.
* Test objectives defined in this strategy have been achieved.