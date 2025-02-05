# Form Sync Data Impact Report

## Project Duration
**July 2024 - Ongoing**

## Project Overview
**Context:**
CDMS includes a critical feature called **Form Sync**, which allows users to clone a study, apply modifications, and then merge those changes back into the original study. 
This functionality is essential for adapting studies to regulatory updates or evolving study designs over time.

However, before this initiative, CDMS lacked a structured way to track the **impact** of these changes. 
Users had no visibility into potential consequences such as:
- Dropped signatures and locks
- Data loss
- Verification removals
- Other integrity issues

Without an impact tracking system, users were making changes blindly, risking unintended data corruption and compliance issues.

**Objective:**
Develop a robust tracking system to **analyze and report the impact** of changes made during the Form Sync process. 
This would provide users with **full transparency**, enabling them to make informed decisions before merging changes into a live study.

## My Role and Contributions
As the **lead engineer** on this initiative, I was responsible for designing and implementing the tracking system from the ground up. 
Throughout the project, I worked closely with the **Product Owner** Alexandra Marinescu to align the solution with business needs and collaborated with the **QA team** to ensure reliability and accuracy.

### **Key Actions:**
- **Problem Analysis:** Investigated the Form Sync workflow to identify potential risks and impact areas.
- **Impact Categorization:** Defined different types of changes (signatures dropped, data loss, verification removals, etc.).
- **Database Design:** Implemented an optimized storage mechanism in **MySQL** to efficiently persist impact reports.
- **Cross-Functional Collaboration:** Worked closely with the **Product Owner** to refine requirements and define business-critical impact scenarios.
- **Testing & Validation:** Partnered with the **QA team** supporting then writing extensive test cases, ensuring the system accurately captured changes under various conditions.
- **Performance Optimization:** Enhanced the system to handle **large-scale** Form Sync report generations without significant overhead.

## Outcome and Impact
Although the project is still ongoing, the impact tracking system is already delivering major benefits:
- **Full Visibility:** Users now receive **detailed impact reports** before applying Form Sync changes, preventing unintended data loss.
- **Data Integrity:** The system enforces **better decision-making**, reducing errors that could compromise study data.
- **Cross-Team Alignment:** Close collaboration with **Product and QA teams** resulted in a well-defined, thoroughly tested feature that meets business needs.
- **Scalability & Efficiency:** Optimized processing ensures the tracking system performs well even on large datasets.
- **Improved User Confidence:** Early feedback from users has been positive, with increased trust in the Form Sync feature.

## Technologies and Tools
- **Backend:** PHP, Symfony Messenger
- **Database:** MySQL
- **Observability:** Datadog
- **Development Tools:** PhpStorm, Git
- **Project Management:** Jira, Confluence
- **Communication:** Slack, Google Meet  
