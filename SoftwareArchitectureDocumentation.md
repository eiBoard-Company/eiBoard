# eiBoard - Software Architecture Documentation

## Table of contents
- [Table of contents](#table-of-contents)
- [Introduction](#1-introduction)
    - [Purpose](#11-purpose)
    - [Scope](#12-scope)
    - [Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
    - [References](#14-references)
    - [Overview](#15-overview)
- [Architectural Representation](#2-architectural-representation)
- [Architectural Goals and Constraints](#3-architectural-goals-and-constraints)
- [Use-Case View](#4-use-case-view)
    - [Use-Case Realization](#41-use-case-realization)
- [Logical View](#5-logical-view)
    - [Overview](#51-overview)
    - [Architecturally Significant Design Packages](#52-architecturally-significant-design-packages)
- [Process View](#6-process-view)
- [Deployment View](#7-deployment-view)
- [Implementation View](#8-implementation-view)
    - [Overview](#81-overview)
    - [Implementation View](#82-layers)
- [Size and Performance](#9-size-and-performance)
- [Quality](#11-quality)

 

## 1. Introduction
### 1.1 Purpose
This Software Architecture Document (SAD) provides an overview of the entire Software Architecture Document. It provides a comprehensive architectural overview of the system, using a number of different architectural views to depict different aspects of the system. It is intended to capture and convey the significant architectural decisions which have been made on the system.

### 1.2 Scope
[A brief description of what the Software Architecture Document applies to; what is affected or influenced by this document.]


### 1.3 Definitions, Acronyms and Abbreviations
| Abbrevation | Explanation                            |
| ----------- | -------------------------------------- |
| API         | Application Programming Interface      |
| FAQ         | Frequently asked Questions             |
| n/a         | not applicable                         |
| SRS         | Software Requirements Specification    |
| UC          | Use Case                               |
| UCD         | Overall Use Case Diagram               |
| RaPla       | Raum Planer                            |

### 1.4 References

| Title                                                              | Date       | Publishing organization   |
| -------------------------------------------------------------------|:----------:| ------------------------- |
| [eiCompany Blog](https://eicompany.wordpress.com/)                 | 20.10.2022 | eiCompany                 |


### 1.5 Overview
[This subsection describes what the rest of the Software Architecture Document contains and explains how the Software Architecture Document is organized.]
    
## 2. Architectural Representation
[This section describes what software architecture is for the current system, and how it is represented. Of the Use-Case, Logical, Process, Deployment, and Implementation Views, it enumerates the views that are necessary, and for each view, explains what types of model elements it contains.]

## 3. Architectural Goals and Constraints
The application “eiBoard” is a mobile app designed to create and manage todos. The frontend is going to be realized with Flutter. The backend will be implemented with the Spring Boot Framework and Java. Most important are the three subsystems in the application:
 Start dashboard: The essential part of the UI, which shows the DHBW rapla schedule, tasks, and exams.
Account system: Users of eiBoard can create their own accounts to get their personal space. The account will also be connected with the rapla calendar to show each user’s schedule.
Database system: All the data which is shown by the start dashboard of each user should be stored in a database. For the database we decided to use H2 database which is an in-memory database but can also used on a persistent level.
For the design of eiBoard there is a style guide, which includes all fonts and style.
The whole application progress is stored on GitHub and documented by a WordPress blog.


## 4. Supporting Information
For any further information you can contact the eiBoard team or check out our [eiCompany Blog](https://eicompany.wordpress.com/). 
The Team Members are:
- Eileen Fahrner
- Niklas Geppert
- Marius Schad
- Matteo Staar
- Julian Stadler
