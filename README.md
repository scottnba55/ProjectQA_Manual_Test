# OrangeHRM - Manual and Exploratory Testing Project

## Live Project Links
*   Live Test Repository: [Browse Test Cases on Qase.io](ПОСТАВИ_ТВОЯ_ЛИНК_ОТ_QASE_ТУК)

## Project Overview
This repository contains a comprehensive manual testing portfolio for the OrangeHRM Open-Source demo application. Due to the complete absence of project documentation and business requirements, a Chartered Exploratory Testing and Reverse Engineering approach was applied to map the system behavior, design detailed test scenarios, and detect functional anomalies.

## Tools Used
*   Qase.io: Test Case Management and Test Run Execution
*   Jira (Atlassian): Defect Tracking and Management

## Test Execution History (Test Runs)
The project deployment history in Qase.io consists of three distinct test execution cycles:

1. OrangeHRM - Regression Testing (Main Campaign): 10 test cases executed. 9 Passed, 1 Failed. (90% Pass Rate).
2. PIM functionality: Targeted smoke test suite. 9 Passed.
3. Auth and Security: Initial security suite. 2 Passed, 1 Failed.

![Qase Test Runs Dashboard](test_runs_dashboard.jpg)

### Tested Modules and Scope
1.  Admin Module: CRUD operations for system users, input boundary value testing, and form validation verification (including password case sensitivity checks).
2.  Leave/Time Module: Verification of multi-attribute filter rules, weekend time computation logic, leave entitlement updates, and workflow authorization actions (Approve/Reject/Cancel).

## Highlighted Defect Report (Sample Bug)
ID: D-3 (Qase) / Linked to Jira Issue Tracker
*   Summary: UI Inconsistency: 'Show Leave with Status' dropdown displays '-- Select --' but activates 'Pending Approval' tag after Reset.
*   Severity: Major (Blocks logical form reset state)
*   **Expected Result:** The UI state must be consistent. Either the dropdown should explicitly display "Pending Approval" to match the active tag, or the filter tag should remain completely empty until a user action triggers it.
*   **Actual Result:** The dropdown element resets to display "-- Select --", but the system automatically populates and activates the "Pending Approval" filter tag right below it. This creates a visual inconsistency for the user.
