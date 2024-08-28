# Castor CDMS Participant Signature

## Project Duration
**May 2022 - December 2022**

## Project Overview
**Context:**  
At Castor CDMS, an Electronic Data Capture (EDC) system, the need for an efficient and compliant way to manage participant data forms was identified, leading to the introduction of the "Participant Signature" feature. This feature was designed to allow clinicians to electronically sign all forms related to a participant collectively, reducing the manual effort required and ensuring compliance with FDA's Part 11 regulations on electronic records and signatures ([FDA Guidance](https://www.fda.gov/regulatory-information/search-fda-guidance-documents/part-11-electronic-records-electronic-signatures-scope-and-application)).

**Objective:**  
Develop a secure, scalable, and compliant electronic signature feature using a domain-driven design (DDD) approach. The feature aimed to streamline the signing process for clinicians and re-engineer existing signing and unsigning form workflows to improve performance.

## My Role and Contributions
I played a crucial role in the backend design and implementation of the "Participant Signature" feature, which was the first project, within the company, to be developed following a domain-driven design approach. This introduced significant challenges, particularly in integrating a new bounded context into a legacy codebase. Despite these challenges, the team successfully navigated the transition, resulting in a robust and scalable solution.

**Key Actions:**
- **Solution Design:** Led the design of the solution, collaborating closely with team mate Gabriele Martini and team leader Stefano Angaran to evaluate different approaches. Consulted with DDD expert Bas Van Vliet to ensure adherence to DDD principles.
- **Implementation:** Developed the "Participant Signature" feature, allowing clinicians to sign and unsign multiple participant forms in a single action, significantly streamlining workflows.
- **Legacy Integration:** Managed the integration of a new bounded context into the legacy codebase, ensuring smooth interaction between the new and existing systems.
- **Re-Engineering Workflows:** Proposed and implemented a lazy loading approach for the existing visit, form, repeating data instance, and repeating data form sign/unsign flows, reducing memory usage and improving request performance.
- **Testing and QA:** Worked closely with the QA team and implemented extensive automated tests, resulting in minimal production defects post-release.

## Outcome and Impact
- Successfully launched the "Participant Signature" feature, leading to a **significant reduction in clinician workload** and **improved system performance**.
- The transition to a domain-driven design approach was effectively managed, setting a precedent for future projects.
- The system experienced **minimal production defects** post-release due to comprehensive automated testing and QA collaboration.
- Enhanced the application’s performance through optimized data loading strategies, benefiting both the new and existing workflows.

## Technologies and Tools
- **Languages/Frameworks:** Laminas, PHP
- **Design Approach:** Domain-Driven Design (DDD)
- **Database:** MySQL
- **Project Management:** Jira, Confluence
- **Collaboration:** Worked closely with Gabriele Martini, Stefano Angaran, and consulted with Bas Van Vliet for DDD guidance.
