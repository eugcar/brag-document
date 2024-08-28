# Study Creation Flow Optimization

## Project Duration
**May 2024**

## Project Overview
**Context:**  
In May 2024, I decided to tackle one of the major pain points in our application: the study creation flow. This process 
involved provisioning a new database schema and running migrations, which were identified as significant bottlenecks. 
Through data analysis on our observability solution, feedback from the customer success team, and discussions with 
fellow engineers, I prioritized improving this flow to enhance the overall user experience.

**Objective:**  
Reduce the time required to create a new study by optimizing the database provisioning and migration process, 
thereby improving application performance and customer satisfaction.

## My Role and Contributions
I took the initiative to design and implement a solution that dramatically improved the efficiency of the study 
creation process. My approach involved creating a pool of pre-provisioned study databases, which could be quickly 
assigned during the study creation process, significantly reducing the time required for this operation.

**Key Actions:**
- **Problem Identification:** Analyzed observability data and gathered insights from the customer success team and engineering peers to identify the study creation flow as a critical bottleneck.
- **Solution Design:** Developed a mechanism to maintain a pool of pre-provisioned study databases, configured by a property that specifies the number of available ones.
- **Implementation:** Implemented a messaging system where, upon study creation, a message is sent to a message bus. A consumer picks up this message to provision the study database and run migrations asynchronously.
- **Performance Improvement:** Reduced the study creation time from **15-20 seconds to just 2 seconds**, significantly enhancing user experience.

## Outcome and Impact
- **90% reduction** in study creation time, improving customer satisfaction and overall application performance.
- Streamlined the study creation process, leading to increased efficiency and allowing users to start working with new studies almost immediately.
- Set a new standard for addressing application bottlenecks by proactively identifying and solving high-impact issues.

## Technologies and Tools
- **Languages/Frameworks:** PHP, Symfony Messenger
- **Database:** MySQL
- **Observability Tools:** Datadog
