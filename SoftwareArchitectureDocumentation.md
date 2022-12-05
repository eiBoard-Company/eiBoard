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
- [Data View](#9-data-view)
- [Size and Performance](#10-size-and-performance)
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
- Start dashboard: The essential part of the UI, which shows the DHBW rapla schedule, tasks, and exams.
- Account system: Users of eiBoard can create their own accounts to get their personal space. The account will also be connected with the rapla calendar to show each user’s schedule.
- Database system: All the data which is shown by the start dashboard of each user should be stored in a database. For the database we decided to use H2 database which is an in-memory database but can also used on a persistent level.
For the design of eiBoard there is a style guide, which includes all fonts and style.
The whole application progress is stored on GitHub and documented by a WordPress blog.

## 4. Use-Case View
[This section lists use cases or scenarios from the use-case model if they represent some significant, central functionality of the final system, or if they have a large architectural coverage—they exercise many architectural elements or if they stress or illustrate a specific, delicate point of the architecture.]

### 4.1 Use-Case Realizations
[This section illustrates how the software actually works by giving a few selected use-case (or scenario) realizations, and explains how the various design model elements contribute to their functionality.]
 
## 5. Logical View
[This section describes the architecturally significant parts of the design model, such as its decomposition into subsystems and packages. And for each significant package, its decomposition into classes and class utilities. You should introduce architecturally significant classes and describe their responsibilities, as well as a few very important relationships, operations, and attributes.]

### 5.1 Overview
[This subsection describes the overall decomposition of the design model in terms of its package hierarchy and layers.]

### 5.2 Architecturally Significant Design Packages
[For each significant package, include a subsection with its name, its brief description, and a diagram with all significant classes and packages contained within the package.
For each significant class in the package, include its name, brief description, and, optionally, a description of some of its major responsibilities, operations, and attributes.]

## 6. Process View
Questions to answer when drawing component diagram

- What are the major executing components and how do they interact at runtime?
- What are the major shared data stores?
- Which parts of the system are replicated?
- How does data progress through the system?
- Which parts of the system can run in parallel?

## 7. Deployment View
[This section describes one or more physical network (hardware) configurations on which the software is deployed and run. It is a view of the Deployment Model. At a minimum for each configuration it should indicate the physical nodes (computers, CPUs) that execute the software and their interconnections (bus, LAN, point-to-point, and so on.) Also include a mapping of the processes of the Process View onto the physical nodes.]

## 8. Implementation View
[This section describes the overall structure of the implementation model, the decomposition of the software into layers and subsystems in the implementation model, and any architecturally significant components.]

### 8.1 Overview
[This subsection names and defines the various layers and their contents, the rules that govern the inclusion to a given layer, and the boundaries between layers. Include a component diagram that shows the relations between layers. ]

### 8.2 Layers
Subsystem:
- Dashboard: Calendar, Tasklist, Navigation, Impressumbar
- Account: Login, Sign Up
- Rapla: Lecture, ScheduleDay, RaplaApi
- Database: Entry, Person, Type

Click [here](https://github.com/eiBoard-Company/eiBoard/blob/documentation/UML_component_diagram.png) for the Component Diagram.

## 9. Data View
[A description of the persistent data storage perspective of the system. This section is optional if there is little or no persistent data, or the translation between the Design Model and the Data Model is trivial.]

## 10. Size and Performance
[A description of the major dimensioning characteristics of the software that impact the architecture, as well as the target performance constraints.]

## 11. Quality

[A description of how the software architecture contributes to all capabilities (other than functionality) of the system: extensibility, reliability, portability, and so on. If these characteristics have special significance, such as safety, security or privacy implications, they must be clearly delineated.]


