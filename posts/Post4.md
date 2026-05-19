---
title: Data Structures and Refining Technical Scope
date: 2026-04-30
author: Kieu-An Nguyen
summary: Define data requirements and key user relationships
tags:
  - DDD
  - ERD
  - Data Analysis
---
In class, we created a DDD and ERD to organise and assess the data requirements for our website. A key insight we found was that our platform, ‘After Dark’, heavily relies on structured and time sensitive data rather than free form social interactions. Since the primary purpose of the hub is to help connect users to relevant services that are available after standard business hours, information such as operating hours, services, location, and pricing are critical within the system. Using SQlite, these datasets will be utilised to build the filter function, allowing users to efficiently search for relevant services. Our aim is to improve long-term user retention by creating a quality product that is ensured to get the job done.

<details>
  <summary>ERD</summary>
<img src="https://raw.githubusercontent.com/kblkwan/DEV-Blog/refs/heads/main/posts/images/W4.png" width="720">
</details>

In addition, we realised that several proposed features would significantly increase development complexity without directly supporting the application’s core functional requirements. As a result, we refined the project scope and decided to keep non-essential features in the final prototype as icons or non-interactable static images. This decision allowed us to prioritise the core user interactions in the current prototype while leaving room for these additional features to be explored and potentially implemented in future upgrades. The development of these features can also be used as a road map to scale the website use cases in the future.

### Data Generation
For our prototype, we plan to AI-generate data to simulate platform usage without requiring active users. This will populate the database and allow us to test key features such as search, filtering, and service discovery. It also enables us to evaluate the system in a controlled environment, focusing on whether core interactions function as intended before introducing real user participation.
