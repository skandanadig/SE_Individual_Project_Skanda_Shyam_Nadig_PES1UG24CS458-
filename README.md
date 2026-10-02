# Smart Cities Municipal Infrastructure Damage Reporting App

**Problem Statement #29 — Transport & Logistics**
**Course:** Software Engineering
**Student:** Skanda Shyam Nadig
**USN:** PES1UG24CS458
**Section:** H

## 1. Problem Statement

A citizen-centric municipal infrastructure damage reporting application that allows citizens to report issues such as **road potholes, broken streetlights, and water pipeline leaks** using geotagged photographs.

The system captures the reported damage, extracts relevant GPS information, creates a municipal service ticket, and automatically dispatches the ticket to the appropriate municipal engineering department for resolution.

The application aims to improve the efficiency, traceability, and responsiveness of municipal infrastructure maintenance.

## 2. Objectives

* Enable citizens to report infrastructure damage easily.
* Capture the location of reported damage using GPS metadata.
* Allow reports to be created even when the user is temporarily offline.
* Automatically route reported issues to the appropriate municipal department.
* Allow citizens to track the status of their submitted complaints.
* Enable municipal engineers to update ticket status as work progresses.
* Provide administrators with functionality to manage user accounts.

## 3. Actors

### Citizen Reporter

* Reports infrastructure damage.
* Provides photographs and relevant information.
* Tracks the status of submitted reports.

### Municipal Engineer

* Receives assigned infrastructure damage tickets.
* Reviews reported issues.
* Updates ticket status as the issue progresses toward resolution.

### System Administrator

* Manages user accounts.
* Maintains administrative access to the system.

## 4. Functional Requirements

The system includes the following major functional requirements:

* **FR-001:** Allow citizens to report infrastructure damage.
* **FR-002:** Extract GPS metadata from submitted photographs.
* **FR-003:** Support drafting reports when the user is offline.
* **FR-004:** Automatically dispatch reported issues to the appropriate municipal department.
* **FR-005:** Allow users and municipal personnel to track and update ticket status.

Detailed requirements, priorities, acceptance criteria, and rationales are provided in `Requirements_Table.docx`.

## 5. Non-Functional Requirements

The system also considers important non-functional requirements such as:

* **Usability:** The reporting process should be simple and accessible to citizens.
* **Reliability:** Reports and ticket information should be handled consistently, including support for offline report drafting.

The complete NFR specification is available in `Requirements_Table.docx`.

## 6. Use Cases

The system contains seven primary use cases:

| ID    | Use Case                 | Description                                                                           |
| ----- | ------------------------ | ------------------------------------------------------------------------------------- |
| UC-01 | **Report Damage**        | Citizen submits a report describing municipal infrastructure damage.                  |
| UC-02 | **Extract GPS Metadata** | System extracts location information from the submitted photograph.                   |
| UC-03 | **Draft Offline Report** | Citizen can prepare a report when an internet connection is unavailable.              |
| UC-04 | **Auto-Dispatch Ticket** | System automatically sends the generated ticket to the relevant municipal department. |
| UC-05 | **Track Ticket Status**  | Citizen can view the current status of a submitted ticket.                            |
| UC-06 | **Update Ticket Status** | Municipal engineer updates the progress/status of a ticket.                           |
| UC-07 | **Manage User Accounts** | System administrator manages user accounts and access.                                |

### UML Relationships

* **UC-01 `Report Damage`** `«include»` **UC-02 `Extract GPS Metadata`**

  * GPS metadata extraction is a required part of the reporting process.

* **UC-01 `Report Damage`** `«extend»` **UC-03 `Draft Offline Report`**

  * Offline report drafting is an optional/conditional extension of the reporting process.

## 7. Use-Case Flow — UC-01: Report Damage

### Preconditions

* The citizen has access to the application.
* The citizen is able to provide information about the infrastructure damage.
* A photograph may be provided as supporting evidence.

### Main Success Scenario

1. Citizen opens the damage-reporting feature.
2. Citizen selects the type of infrastructure damage.
3. Citizen captures or uploads a photograph.
4. System extracts GPS metadata from the photograph.
5. Citizen provides additional details about the issue.
6. System validates the submitted information.
7. System creates a municipal service ticket.
8. Ticket is automatically dispatched to the appropriate department.
9. Citizen receives confirmation of the submitted report.

### Alternate Flow

If the required information or location data cannot be obtained automatically, the system allows the citizen to provide the necessary information manually or modify the report before submission.

### Exception Flow

If the device is offline, the citizen can save/draft the report and submit it when connectivity becomes available.

## 8. Repository Structure

This repository follows the required folder structure for the Individual Project Submissions:

* **`1-RE/`**: Requirements Engineering documents (FR, NFR, RTM Table, Use Cases, flow diagrams).
* **`2-Architectural_Diagram/`**: Architectural Component Diagrams and Justification for the Municipal Infrastructure App.
* **`3-Project_Creation/`**: Project Creation screenshots in GitHub and Jira Tool.
* **`4-SRS_and_WBS/`**: Software Requirements Specification (SRS) and Work Breakdown Structure (WBS) steps.
* **`5-Copilot_Generated_Code/`**: Github Copilot generated code screenshots or repository links.
* **`6-Software_Testing/`**: Software Testing Tools practice and bug fix documentation.
* **`SELABS/Lab3/`**: Lab 3 Component Modelling & Architectural Pattern Selection deliverables.

## 9. UML Diagram

The repository contains the complete UML use-case diagram showing the interaction between:

**Citizen Reporter → Reporting System ← Municipal Engineer / System Administrator**

The diagram also represents the `«include»` and `«extend»` relationships between the relevant use cases.

## 10. Technologies / Concepts Used

This activity focuses primarily on **Software Engineering and Requirements Engineering concepts**, including:

* Requirements identification
* Functional and non-functional requirements
* Actors and system boundaries
* UML Use-Case Diagrams
* Use-case specifications
* `«include»` relationships
* `«extend»` relationships
* Main success scenarios
* Alternate flows
* Exception flows
* Acceptance criteria

## 11. Conclusion

The proposed application provides a structured approach for reporting and managing municipal infrastructure damage. By combining citizen reporting, geolocation, automated ticket dispatch, and status tracking, the system can improve communication between citizens and municipal authorities while providing a traceable workflow for infrastructure maintenance.

---

**Student:** Skanda Shyam Nadig
**USN:** PES1UG24CS458
**Section:** H
