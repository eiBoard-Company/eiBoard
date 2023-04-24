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
This Test Plan for CommonPlayground supports the following objectives:

- Identifies the items that should be targeted by the tests.
- Identifies the motivation for and ideas behind the test areas to be covered.
- Outlines the testing approach that will be used.
- Identifies the required resources and provides an estimate of the test efforts.

### 1.2 Scope

This test plan will cover tests assuring the functionality of the application's front end, back end and the communication between the two.
This document shows the following types of testing:

- Unit Testing
- Integration Testing
- User Interface Testing
- API Testing

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

//TODO: add Use Cases

| Title                                                                   | Date       | Publishing organization   |
| ------------------------------------------------------------------------|:----------:| ------------------------- |
| [Blog](https://eicompany.wordpress.com/)                          | Oct. 2022  | eiCompany                 |
| [UC1 Rapla Calendar/Schedule](https://github.com/eiBoard-Company/eiBoard/blob/main/UC1_SCHEDULE.md)               | Oct. 2022  | eiCompany                 |
| [UC2 Task/To do List](https://github.com/eiBoard-Company/eiBoard/blob/main/UC2_TASKS.md)               | Oct. 2022  | eiCompany                 |
| [UC3 Creating events](https://github.com/eiBoard-Company/eiBoard/blob/main/UC3_EVENTS.md)               | Oct. 2022  | eiCompany                 |
| [UC4  Creating an account](https://github.com/eiBoard-Company/eiBoard/blob/main/UC4_CREATE_ACCOUNT.md)               | Oct. 2022  | eiCompany                 |
| [UC5 Logging in](https://github.com/eiBoard-Company/eiBoard/blob/main/UC5_LOGIN.md)               | Oct. 2022  | eiCompany                 |
| [UC6 Logging out](https://github.com/eiBoard-Company/eiBoard/blob/main/UC6_LOGGING_OUT.md)               | Oct. 2022  | eiCompany                 |
| [UC7 Classes]https://github.com/eiBoard-Company/eiBoard/blob/main/UC7_CLASSES.md)               | Oct. 2022  | eiCompany                 |
| [UC8 Settings](https://github.com/eiBoard-Company/eiBoard/blob/main/UC8_SETTINGS.md)              | Oct. 2022  | eiCompany                 |
| [SRS](https://github.com/eiBoard-Company/eiBoard/blob/main/SoftwareRequirementsSpecification.md)                          | Oct. 2023  | eiCompany                 |
| [SAD](https://github.com/eiBoard-Company/eiBoard/blob/main/SoftwareArchitectureDocumentation.md)                               | Jan. 2023  | eiCompany                 |

### 1.6 Document Structure


## 2. Evaluation Mission and Test Motivation

### 2.1 Background



### 2.2 Evaluation Mission



### 2.3 Test Motivators



## 3. Target Test Items

- Android frontend
- Server backend (and APIs)

## 4. Outline of Planned Tests

### 4.1 Outline of Test Inclusions



### 4.2 Outline of Other Candidates for Potential Inclusion



### 4.3 Outline of Test Exclusions



## 5. Test Approach

### 5.1 Testing Techniques and Types

#### 5.1.1 Unit Testing

#### 5.1.2 User Interface Testing


#### 5.1.3 Integration Testing (API Testing)



## 6. Entry and Exit Criteria

### 6.1 Test Plan

#### 6.1.1 Test Plan Entry Criteria


#### 6.1.2 Test Plan Exit Criteria


## 7. Deliverables

## 7.1 Test Evaluation Summaries


## 7.2 Reporting on Test Coverage


## 7.3 Perceived Quality Reports


## 7.4 Incident Logs and Change Requests


## 7.5 Smoke Test Suite and Supporting Test Scripts


## 8. Testing Workflow


## 9. Environmental Needs

### 9.1 Base System Hardware


### 9.2 Base Software Elements in the Test Environment


### 9.3 Productivity and Support Tools


## 10. Responsibilities, Staffing, and Training Needs

### 10.1 People and Roles


### 10.2 Staffing and Training Needs


## 11. Iteration Milestones


## 12. Risks, Dependencies, Assumptions, and Constraints


## 13. Management Process and Procedures
