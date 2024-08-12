# PubTech Ad Data Consumption

## Project Duration
**March 2021 - April 2021**

## Project Overview
**Context:**  
PubTech, a leading AdTech company, faced a critical scalability challenge with their ad data processing system. The existing batch processing system, reliant on MongoDB, struggled to handle the growing volume of ads across multiple websites, causing performance bottlenecks.

**Objective:**  
Scale the system to handle a significantly higher volume of ad messages, improving efficiency and ensuring seamless ad delivery across all managed platforms.

## My Role and Contributions
I played a key role in redesigning the system architecture, working closely with the CTO, Luca Coppola, to address the scalability issues. I led the migration from a batch processing system to a real-time, queue-based approach using CloudAMQP. This transition increased the system's capacity from processing **1 million to 10 million ad messages per day**.

**Key Actions:**
- Analyzed the limitations of the existing MongoDB batch processing system.
- Designed and implemented a queue-based architecture with CloudAMQP.
- Optimized message processing workflows, ensuring seamless integration with existing Symfony-based services.

## Outcome and Impact
- **10x increase** in daily processed ad messages, from 1 million to 10 million.
- Achieved near-real-time data processing, reducing latency and improving ad delivery efficiency.
- Significantly enhanced system scalability, positioning PubTech for future growth.

## Technologies and Tools
- **Languages/Frameworks:** Symfony, PHP
- **Messaging Queue:** CloudAMQP
- **Database:** MongoDB
