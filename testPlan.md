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
            - [5.1.2 User Interface Testing](#512-user-interface-testing)
            - [5.1.3 Integration Testing (API Testing)](#513-integration-testing-api-testing)
            - [5.1.4 Data and Database Integrity Testing](#514-data-and-database-integrity-testing)
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
[This subsection outlines what the rest of the Test Plan contains and gives an introduction to how the rest of the document is organized. This section may be eliminated if a Table of Contents is used.]

## 2. Evaluation Mission and Test Motivation
 [Provide an overview of the mission and motivation for the testing that will be conducted in this iteration.]

### 2.1 Background

[Provide a brief description of the background surrounding why the test effort defined by this Test Plan will be undertaken. Include information such as the key problem being solved, the major benefits of the solution, the planned architecture of the solution, and a brief history of the project. Where this information is defined in other documents, you can include references to those other more detailed documents if appropriate. This section should only be about three to five paragraphs in length.]

### 2.2 Evaluation Mission
[Provide a brief statement that defines the mission for the evaluation effort in the current iteration. This statement might incorporate one or more concerns including:
•	find as many bugs as possible
•	find important problems, assess perceived quality risks
•	advise about perceived project risks
•	certify to a standard
•	verify a specification (requirements, design or claims)
•	advise about product quality, satisfy stakeholders
•	advise about testing
•	fulfill process mandates 
•	and so forth
Each mission provides a different context to the test effort and alters the way in which testing should be approached.]


### 2.3 Test Motivators

[Provide an outline of the key elements that will motivate the testing effort in this iteration. Testing will be motivated by many thingsquality risks, technical risks, project risks, use cases, functional requirements, non-functional requirements, design elements, suspected failures or faults, change requests, and so forth.]

## 3. Target Test Items

The listing below identifies those test items: software, hardware, and supporting product elements that have been identified as targets for testing. This list represents what items will be tested. 

- FLutter Frontend
- Server Backend (and APIs)

## 4. Outline of Planned Tests

### 4.1 Outline of Test Inclusions

*Frontend: FLutter application: Web Client*:

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
- Usability tests
- any further tests

## 5. Test Approach
[The Test Approach presents the recommended strategy for designing and implementing the required tests. Sections 3, Target Test Items, and 4, Outline of Planned Tests, identified what items will be tested and what types of tests would be performed. This section describes how the tests will be realized. 
One aspect to consider for the test approach is the techniques to be used. This should include an outline of how each technique can be implemented, both from a manual and/or an automated perspective, and the criterion for knowing that the technique is useful and successful. For each technique, provide a description of the technique and define why it is an important part of the test approach by briefly outlining how it helps achieve the Evaluation Mission or addresses the Test Motivators.
Another aspect to discuss in this section is the Fault or Failure models that are applicable and ways to approach evaluating them.
As you define each aspect of the approach, you should update Section 10, Responsibilities, Staffing, and Training Needs, to document the test environment configuration and other resources that will be needed to implement each aspect.]


### 5.1 Testing Techniques and Types

#### 5.1.1 Unit Testing

TODO: jeweils Tabelle einfügen

#### 5.1.2 UI Testing
TODO: jeweils Tabelle einfügen

#### 5.1.3 Integration Testing (API Testing)
TODO: jeweils Tabelle einfügen

#### 5.1.4 Data and Database Integrity Testing
TODO: jeweils Tabelle einfügen

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
