# Test plan

- [Test plan](#test-plan)
    - [1. Introduction](#1-introduction)
        - [1.1 Purpose](#11-purpose)
        - [1.2 Scope](#12-scope)
        - [1.3 Intended Audience](#13-intended-audience)
        - [1.4 Document Terminology and Acronyms](#14-document-terminology-and-acronyms)
        - [1.5  References](#15--references)
        - [1.6 Document Structure](#16-document-structure)
    - [2. Evaluation Mission and Test Motivation](#2-evaluation-mission-and-test-motivation)
        - [2.1 Background](#21-background)
        - [2.2 Evaluation Mission](#22-evaluation-mission)
        - [2.3 Test Motivators](#23-test-motivators)
    - [3. Target Test Items](#3-target-test-items)
    - [4. Outline of Planned Tests](#4-outline-of-planned-tests)
        - [4.1 Outline of Test Inclusions](#41-outline-of-test-inclusions)
        - [4.2 Outline of Other Candidates for Potential Inclusion](#42-outline-of-other-candidates-for-potential-inclusion)
        - [4.3 Outline of Test Exclusions](#43-outline-of-test-exclusions)
    - [5. Test Approach](#5-test-approach)
        - [5.1 Testing Techniques and Types](#51-testing-techniques-and-types)
            - [5.1.1 Unit Testing](#511-unit-testing)
            - [5.1.2 UI Testing](#512-ui-testing)
            - [5.1.3 Integration Testing (API Testing)](#513-integration-testing-api-testing)
    - [6. Entry and Exit Criteria](#6-entry-and-exit-criteria)
        - [6.1 Test Plan](#61-test-plan)
            - [6.1.1 Test Plan Entry Criteria](#611-test-plan-entry-criteria)
            - [6.1.2 Test Plan Exit Criteria](#612-test-plan-exit-criteria)
    - [7. Deliverables](#7-deliverables)
        - [7.1 Test Evaluation Summaries](#71-test-evaluation-summaries)
        - [7.2 Reporting on Test Coverage](#72-reporting-on-test-coverage)
        - [7.3 Perceived Quality Reports](#73-perceived-quality-reports)
        - [7.4 Incident Logs and Change Requests](#74-incident-logs-and-change-requests)
        - [7.5 Smoke Test Suite and Supporting Test Scripts](#75-smoke-test-suite-and-supporting-test-scripts)
    - [8. Testing Workflow](#8-testing-workflow)
    - [9. Environmental Needs](#9-environmental-needs)
        - [9.1 Base System Hardware](#91-base-system-hardware)
        - [9.2 Base Software Elements in the Test Environment](#92-base-software-elements-in-the-test-environment)
        - [9.3 Productivity and Support Tools](#93-productivity-and-support-tools)
    - [10. Responsibilities, Staffing, and Training Needs](#10-responsibilities-staffing-and-training-needs)
        - [10.1 People and Roles](#101-people-and-roles)
        - [10.2 Staffing and Training Needs](#102-staffing-and-training-needs)
    - [11. Iteration Milestones](#11-iteration-milestones)
    - [12. Risks, Dependencies, Assumptions, and Constraints](#12-risks-dependencies-assumptions-and-constraints)
    - [13. Management Process and Procedures](#13-management-process-and-procedures)

## 1. Introduction

### 1.1 Purpose

The purpose of the Iteration Test Plan is to gather all of the information necessary to plan and control the test effort for a given iteration. It describes the approach to testing the software.
This Test Plan for eiBoard supports the following objectives:

- Identifies the items that should be targeted by the tests.
- Identifies the motivation for and ideas behind the test areas to be covered.
- Outlines the testing approach that will be used.
- Identifies the required resources and provides an estimate of the test efforts.

### 1.2 Scope

This test plan will cover tests assuring the functionality of the application's frontend, backend and the communication between the two.
This document shows the following types of testing:

- Unit Testing
- Integration Testing
- UI Testing (End-to-End Tests)

 Not covered are any tests related to performance and scale or usability.

### 1.3 Intended Audience

This test plan is written primarily for internal documentation reasons. It is meant to provide orientation to the developers to work from and as a documentation to measure the fullfillment of quality requirements against.

### 1.4 Document Terminology and Acronyms

| Abbr | Abbreviation                        |
|------|-------------------------------------|
| API  | Application Programmable Interface  |
| CI   | Continuous Integration              |
| CD   | Continuous Delivery/Deployment      |
| n/a  | not applicable                      |
| SRS  | Software Requirements Specification |
| UI   | User Interface                      |

### 1.5  References

| Title                                                                   | Date       | Publishing organization   |
| ------------------------------------------------------------------------|:----------:| ------------------------- |
| [Blog](https://eicompany.wordpress.com/)                          | Oct. 2022  | eiCompany                 |
| [UC1 Rapla Calendar/Schedule](https://github.com/eiBoard-Company/eiBoard/blob/main/UC1_SCHEDULE.md)               | Oct. 2022  | eiCompany                 |
| [UC2 Task/To do List](https://github.com/eiBoard-Company/eiBoard/blob/main/UC2_TASKS.md)               | Oct. 2022  | eiCompany                 |
| [UC3 Creating events](https://github.com/eiBoard-Company/eiBoard/blob/main/UC3_EVENTS.md)               | Oct. 2022  | eiCompany                 |
| [UC4  Creating an account](https://github.com/eiBoard-Company/eiBoard/blob/main/UC4_CREATE_ACCOUNT.md)               | Oct. 2022  | eiCompany                 |
| [UC5 Logging in](https://github.com/eiBoard-Company/eiBoard/blob/main/UC5_LOGIN.md)               | Oct. 2022  | eiCompany                 |
| [UC6 Logging out](https://github.com/eiBoard-Company/eiBoard/blob/main/UC6_LOGGING_OUT.md)               | Oct. 2022  | eiCompany                 |
| [UC7 Classes](https://github.com/eiBoard-Company/eiBoard/blob/main/UC7_CLASSES.md)               | Oct. 2022  | eiCompany                 |
| [UC8 Settings](https://github.com/eiBoard-Company/eiBoard/blob/main/UC8_SETTINGS.md)              | Oct. 2022  | eiCompany                 |
| [SRS](https://github.com/eiBoard-Company/eiBoard/blob/main/SoftwareRequirementsSpecification.md)                          | Oct. 2023  | eiCompany                 |
| [SAD](https://github.com/eiBoard-Company/eiBoard/blob/main/SoftwareArchitectureDocumentation.md)                               | Jan. 2023  | eiCompany                 |

### 1.6 Document Structure
n/a

## 2. Evaluation Mission and Test Motivation

### 2.1 Background
eiBoard aims to provide users with an easy-to-use and feature-rich calendar application that can help them manage their schedules and tasks more efficiently. The project has been in development for several months and has gone through several iterations of design and development. The application is designed to work on both Android and iOS platforms, and utilizes a clean software architecture with separate model view and controller, thanks to the implementation of the MVC pattern in both the frontend and backend subsystems. You can read more on our architecture [here](https://github.com/eiBoard-Company/eiBoard/blob/documentation/SoftwareArchitectureDocumentation.md).

Testing serves to ensure that the written code does what it is intended to do, so users will be able to enjoy the best app version possible. Testing is an integral part of ensuring that eiBoard is of high quality, meets user requirements, and functions as intended, making it an essential component of the development process.

Testing can help identify defects, errors, and bugs early in the development process, making it easier and less expensive to fix these issues. It can also help ensure that the application is reliable and efficient, leading to a better user experience and increased user satisfaction.

In our case testing is very important as the application serves as an important tool for users to manage their schedules and tasks. Any errors or bugs in the application could result in incorrect or missing information, leading to confusion and potential negative consequences. Additionally, the application relies on multiple subsystems and APIs, making thorough testing even more critical to ensure that all parts of the application are working together seamlessly.

### 2.2 Evaluation Mission
As mentioned above testing can help identify defects, errors, and bugs early in the development process, making it easier and less expensive to fix these issues. With this testing is a crucial part of the development process.

The focus of the testing effort will be on identifying critical defects that could negatively impact the user experience, as well as identifying any potential quality risks that could impact the reliability of the application.

### 2.3 Test Motivators

The following elements will motivate the testing effort for eiBoard in this iteration:

1. **Quality risks and Use cases**: Testing will ensure that the application meets the desired level of quality and functionality, and will identify any areas where improvements can be made. Testing will focus on ensuring that the application meets the needs and requirements of its users.

2. **Technical risks**: The application relies on multiple subsystems and APIs, so testing will be crucial to ensure that all parts of the application are working together seamlessly.

3. **Functional requirements**: Testing will ensure that the application meets its intended functional requirements, and will identify any areas where improvements can be made to enhance its functionality.

## 3. Target Test Items

The listing below identifies those test items: software, hardware, and supporting product elements that have been identified as targets for testing. This list represents what items will be tested. 

- Flutter Frontend
- Server Backend (and APIs)

## 4. Outline of Planned Tests

### 4.1 Outline of Test Inclusions

*Frontend: Flutter application: Web Client*:

- UI testing
- Unit testing

*Backend: Spring Boot Application*:

- Unit testing
- Integration testing

The tests themself will not be tested and will not account into code coverage.

### 4.2 Outline of Other Candidates for Potential Inclusion

n/a

### 4.3 Outline of Test Exclusions

Because of time and resource constraints we will not do:

- Stress tests
- Load/Performance tests
- Database tests
- Usability tests
- any further tests

## 5. Test Approach

### 5.1 Testing Techniques and Types

#### 5.1.1 Unit Testing

Unit testing ensures, that the tested sourcecode works as expected. Therefore small parts of the sourcecode will be tested independently.

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    | Ensure that each unit of code (functions, methods, classes) works as intended                  |
|Technique              | Implement test methods using JUnit Framework, Mockito library (Backend) and flutter_test library (Frontend) |
|Oracles                | Test results are logged in CI/CD tool (Jenkins), and compared against expected output to determine if the tests passed or failed|
|Required Tools         | JUnit 5 and Mockito Dependencies in Backend, and flutter_test library in Frontend. CI/CD Pipeline with test stages                    |
|Success Criteria       | All tests pass. Coverage is above 10% (Frontend) / 20% (Backend)    |
|Special Considerations | -                                                                   |


#### 5.1.2 UI Testing

UI testing evaluates the application's performance from a user's point of view, with the aim of verifying that the user interface operates as intended.

|                       | Description                                                          |
|-----------------------|----------------------------------------------------------------------|
|Technique Objective    | Test application automated from the perspective of the user through UI Test |
|Technique              | Writing test cases using Cypress to simulate user interactions with the application's UI (mainly use cases).  |
|Oracles                | Expect that the UI elements are displayed and behave as expected during test execution. Test results are logged in CI/CD tool (Jenkins), and compared against expected output to determine if the tests passed or failed. |
|Required Tools         | Cypress |
|Success Criteria       | All UI tests pass.
|Special Considerations | - |

#### 5.1.3 Integration Testing (API Testing)

API Testing is part of integration testing. Integration tests test multiple modules of an application together. The main goal of API testing is to ensure, that the provided APIs of the Backend behave as expected.

|                       | Description                                                          |
|-----------------------|----------------------------------------------------------------------|
|Technique Objective    | Ensure that the implemented API functions correctly and returns expected results                                 |
|Technique              | Implement test methods using JUnit Framework and REST-assured library to perform HTTP requests and verify responses  |            |
|Oracles                | Test results are logged in CI/CD tool (Jenkins), and compared against expected output to determine if the tests passed or failed |
|Required Tools         | JUnit 5 and REST-assured library dependencies in Backend                                    |
|Success Criteria       | All tests pass. Coverage is above 40%                                |
|Special Considerations | APIs must be in a testable state, e.g., mock objects are used for dependencies that may not be available during tests |

## 6. Entry and Exit Criteria

### 6.1 Test Plan

#### 6.1.1 Test Plan Entry Criteria
n/a


#### 6.1.2 Test Plan Exit Criteria
n/a

## 7. Deliverables

## 7.1 Test Evaluation Summaries
The project owns a certain amount of tests in the Frontend and Backend. Each pushed commit should trigger the projects CI/CD Pipeline, which builds the application and executes the tests with a code analysis with Codacy. (In our final demo this sadly does not work yet)


## 7.2 Reporting on Test Coverage
This happens manually every time a developer writes a new test with the test coverage tools EclEmma and IntelliJ IDEA Code Coverage and with the tool Codacy.

## 7.3 Perceived Quality Reports
If a build of our CI/CD Pipeline fails the administrators will be messaged. This includes a fail due to a failed test. Furthermore, the code quality tool is codacy.

## 7.4 Incident Logs and Change Requests
Codacy should be added to the CI/CD pipeline. Every time someone pushes to the main repository, the pipeline with a build will be triggered. If a build fails this is directly visible in Jenkins.


## 7.5 Smoke Test Suite and Supporting Test Scripts
The automated test execution in our CI/CD Pipeline enables regression testing. With this approach it is clearly visible when changes break existing functions and affect the correct behaviour of the application.

## 8. Testing Workflow
1. Local testing in the IDE
2. A Commit or Push to the main repository triggers the build and test exection in the CI/CD Pipeline
3. This triggers the pipeline (build and test)
4. Before the automated deployment the build and test stages are executed

## 9. Environmental Needs

### 9.1 Base System Hardware
The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource              | Quantity | Name and Type                |
|-----------------------|:--------:|------------------------------|
| CI/CD server          |    1     | Jenkins              |
| local test machine    |    1     | notebook (Eileen, Niklas, Matteo, Julian, Marius)       |
| web application (eiboard.de)   |    1     | web application |


### 9.2 Base Software Elements in the Test Environment
The following base software elements are required in the test environment for this Test Plan.

| Software Element Name |  Type and Other Notes                        |
|-----------------------|----------------------------------------------|
| Eclipse, IntelliJ, Visual Studio Code        | Test Runner / IDE                            |
| JUnit 5, Mockito, flutter_test           | Unit testing library                         |
| Cypress              | UI testing library                           |


### 9.3 Productivity and Support Tools
The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type | Tool Brand Name                              |
|-----------------------|----------------------------------------------|
| Repository            | [github.com](http://github.com/)             |
| Test Coverage Monitor | [codacy](https://app.codacy.com/)            |
| CI/CD Service         | [Jenkins](https://www.jenkins.io/)           |


## 10. Responsibilities, Staffing, and Training Needs

### 10.1 People and Roles
| Role          | Person Assigned |  Specific Responsibilities or Comments |
|---------------|:--------------:|----------------------------------------|
| Test Manager | Marius | Provides management oversight. |
| Test Designer | Julian, Eileen, Niklas | Defines the technical approach to the implementation of the test effort. |
| Test System Administrator | Julian, Matteo | Ensures test environment and assets are managed and maintained. |


### 10.2 Staffing and Training Needs
n/a

## 11. Iteration Milestones
We want to keep over 20% code coverage.

## 12. Risks, Dependencies, Assumptions, and Constraints
| Risk | Mitigation Strategy | Contingency (Risk is realized) |
|------|---------------------|--------------------------------|
| Code has lots of side effects | Refactor code (Clean Code principles) | publish new refactored tests |
| Test Runner is not able to execute tests | Use standard libraries which include working Test Runner | fix test execution configuration |
| UI tests fail | Refactor test | publish refactored test and restart |


## 13. Management Process and Procedures

n/a
