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
[Specify the criteria that will be used to determine whether the execution of the Test Plan can begin.]


#### 6.1.2 Test Plan Exit Criteria
 [Specify the criteria that will be used to determine whether the execution of the Test Plan is complete or that continued execution provides no further benefit.]


## 7. Deliverables
[In this section, list the various artifacts that will be created by the test effort that are useful deliverables to the various stakeholders of the test effort. Don’t list all work products; only list those that give direct, tangible benefit to a stakeholder and those by which you want the success of the test effort to be measured.]

## 7.1 Test Evaluation Summaries
[Provide a brief outline of both the form and content of the test evaluation summaries, and indicate how frequently they will be produced.]


## 7.2 Reporting on Test Coverage
[Provide a brief outline of both the form and content of the reports used to measure the extent of testing, and indicate how frequently they will be produced. Give an indication as to the method and tools used to record, measure, and report on the extent of testing.] 

## 7.3 Perceived Quality Reports
[Provide a brief outline of both the form and content of the reports used to measure the perceived quality of the product, and indicate how frequently they will be produced. Give an indication about to the method and tools used to record, measure, and report on the perceived product quality. You might include some analysis of Incidents and Change Request over Test Coverage.]

## 7.4 Incident Logs and Change Requests
[Provide a brief outline of both the method and tools used to record, track, and manage test incidents, associated change requests, and their status.]


## 7.5 Smoke Test Suite and Supporting Test Scripts

[Provide a brief outline of the test assets that will be delivered to allow ongoing regression testing of subsequent product builds to help detect regressions in the product quality.]  

## 8. Testing Workflow

[Provide an outline of the workflow to be followed by the Test team in the development and execution of this Test Plan.]
The specific testing workflow that you will use should be documented separately in the project's Development Case. It should explain how the project has customized the base RUP test workflow (typically on a phase-by-phase basis). In most cases, we recommend you place a reference in this section of the Test Plan to the relevant section of the Development Case. It might be both useful and sufficient to simply include a diagram or image depicting your test workflow.
More specific details of the individual testing tasks are defined in a number of different ways, depending on project culture; for example:
•	defined as a list of tasks in this section of the Test Plan, or in an accompanying appendix 
•	defined in a central project schedule (often in a scheduling tool such as Microsoft Project) 
•	documented in individual, "dynamic" to-do lists for each team member, which are usually too detailed to be placed in the Test Plan 
•	documented on a centrally located whiteboard and updated dynamically 
•	not formally documented at all
Based on your project culture, you should either list your specific testing tasks here or provide some descriptive text explaining the process your team uses to handle detailed task planning and provide a reference to where the details are stored, if appropriate.
For Master Test Plans, we recommend avoiding detailed task planning, which is often an unproductive effort if done as a front-loaded activity at the beginning of the project. A Master Test Plan might usefully describe the phases and the number of iterations, and give an indication of what types of testing are generally planned for each Phase or Iteration.
Note: Where process and detailed planning information is recorded centrally and separately from this Test Plan, you will have to manage the issues that will arise from having duplicate copies of the same information. To avoid team members referencing out-of-date information, we suggest that in this situation you place the minimum amount of process and planning information within the Test Plan to make ongoing maintenance easier and simply reference the "Master" source material.] 



## 9. Environmental Needs
[This section presents the non-human resources required for the Test Plan.]

### 9.1 Base System Hardware

The following table sets forth the system resources for the test effort presented in this Test Plan.
[The specific elements of the test system may not be fully understood in early iterations, so expect this section to be completed over time. We recommend that the system simulates the production environment, scaling down the concurrent access and database size, and so forth, if and where appropriate.]
[Note:  Add or delete items as appropriate.]

TODO: Tabelle einfügen


### 9.2 Base Software Elements in the Test Environment
TODO: Tabelle einfügen


### 9.3 Productivity and Support Tools
TODO: Tabelle einfügen


## 10. Responsibilities, Staffing, and Training Needs
[This section presents the required resources to address the test effort outlined in the Test Plan—the main responsibilities, and the knowledge or skill sets required of those resources.]

### 10.1 People and Roles
TODO: Tabelle einfügen


### 10.2 Staffing and Training Needs

This section outlines how to approach staffing and training the test roles for the project.
[The way to approach staffing and training will vary from project to project. If this section is part of a Master Test Plan, you should indicate at what points in the project lifecycle different skills and numbers of staff are needed. If this is an Iteration Test Plan, you should focus mainly on where and what training might occur during the Iteration.
Give thought to your training needs, and plan to schedule this based on a Just-In-Time (JIT) approach—there is often a temptation to attend training too far in advance of its usage when the test team has apparent slack. Doing this introduces the risk of the training being forgotten by the time it's needed.
Look for opportunities to combine the purchase of productivity tools with training on those tools, and arrange with the vendor to delay delivery of the training until just before you need it. If you have enough headcount, consider having training delivered in a customized manner for you, possibly at your own site.
The test team often requires the support and skills of other team members not directly part of the test team. Make sure you arrange in your plan for appropriate availability of System Administrators, Database Administrators, and Developers who are required to enable the test effort.]


## 11. Iteration Milestones

TODO: Tabelle einfügen


## 12. Risks, Dependencies, Assumptions, and Constraints

TODO: Tabelle einfügen


## 13. Management Process and Procedures

[Outline what processes and procedures are to be used when issues arise with the Test Plan and its enactment.]
