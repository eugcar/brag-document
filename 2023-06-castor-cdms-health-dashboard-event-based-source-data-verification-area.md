# CDMS Health Dashboard - Event Based Source Data Verification (SDV) Area

## Project Duration
**June 2023 - April 2024**

## Project Overview
**Context:**  
During my time at Castor, I played a pivotal role in the development of a new area within the CDMS Health Dashboard 
focused on providing customers with insights into the status of their Source Data Verification (SDV) in clinical studies. 
Given the complexity of handling studies with hundreds of thousands of participants, coupled with intricate access and 
visibility rules based on user roles, field dependencies and others, our team had to devise a scalable and efficient 
solution that met stringent non-functional requirements, such as quick report generation times.

**Objective:**  
Create an event-based system to track and project all relevant events for SDV insights, ensuring the system could handle 
large-scale studies while providing accurate and timely reports.

## My Role and Contributions
As a core member of the team, I was deeply involved in the design, implementation, and optimization of the new SDV area. 
We adopted an event-driven approach to capture and project necessary events onto read models tailored to the specific needs of the SDV dashboard.

**Key Actions:**
- **Event Storming Sessions:** Participated in and contributed to several event storming sessions to thoroughly understand the scenario and define the required events.
- **Technical Spikes:** Collaborated on technical spikes to explore different approaches and finalize the event-driven architecture, considering performance and scalability.
- **Baseline Creation:** Significantly improved the script used to create a baseline for existing studies, ensuring that all studies could be brought into the new system efficiently.
- **Business Logic Implementation:** Implemented substantial portions of the business logic required to support the SDV insights, ensuring accurate event tracking and projection.
- **Changelog Concept:** Worked on introducing a new Changelog concept to collect and apply all events from large operations, such as copying forms, in a single, efficient batch.
- **Code Reviews and Collaboration:** Proposed technical solutions, actively participated in technical discussions, and reviewed pull requests from other team members to ensure code quality and alignment with the project goals.

## Outcome and Impact
- Successfully launched the new SDV area of the CDMS Health Dashboard, providing customers with reliable and fast insights into their SDV status, even for large studies.
- The event-driven architecture proved to be highly scalable, handling the complexity of large datasets and varied access controls efficiently.
- Improved the baseline creation process, reducing the time and resources required to integrate existing studies into the new system.
- Enhanced the overall performance and accuracy of the SDV reporting feature, leading to increased customer satisfaction and trust in the platform.

## Technologies and Tools
- **Project Management:** Jira, Confluence, Miro
- **Development:** PHP, EventSauce, Symfony Messenger
- **Architecture:** Event-driven architecture using event sourcing principles for efficient data processing and reporting