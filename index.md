---
layout: home
---

Jordon Coady (20096529) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; BSc (Hons) in Computer Forensics and Security


## Project Overview

EduCase is a Progressive Web Application (PWA) designed to streamline the process of matching students with mentors and clients with solicitors, ensuring tailored guidance and legal assistance.

For students, EduCase provides a seamless way to connect with suitable mentors based on their academic background, career goals, and personal preferences. The platform offers educational resources, time management tools, and mental well-being support to help ease the transition into higher education.

For clients, EduCase simplifies the process of finding the right solicitor by using a client allocation algorithm that considers the client’s legal needs and the solicitor’s expertise. The platform integrates a case management system (CMS) to help legal professionals efficiently organise and manage their caseloads.

---

## Key Features

### Educational Side 

- Algorithm designed to match students with mentors based off their profiles to ensure a suitable match (See design page for details).

- Time management tool that utilises AWS Textract to convert students timetable/assessment schedules into a customisable format, which will allow custom notes and reminders to be set. 

- System for providing students access to schedule meetings with their assigned mentors, view work assigned by their mentors, and message their mentor through the PWA.

### Legal Side

- Algorithm designed to match clients with solictors, again, based of their profiles, but using different input parameters (See design page for details).

- A comprehensive Case Management System (CMS) implementation with detailed statistics.

- A System for clients to monitor their case status, communication with their solicitor, and upload any required documentation.

---

## Technologies

### Frontend:
- **React**: Framework for creating a modular, responsive user interface. React has a strong ecosystem of prebuilt components that will allow me to build the frontend quickly while also enabling component reuse across different parts of the PWA.  
- **Bootstrap**: CSS framework with pre-designed classes that simplify styling the PWA.  
- **Workbox (Service Workers)**: For caching resources and enabling offline functionality, as well as handling features like background sync and push notifications.  

### Middleware:
- **React Query**: Library for managing server-state, handling data fetching, caching, and synchronization within the React application.  
- **WebSocket API**: Provides a full-duplex communication channel, allowing the client and server to communicate simultaneously—ideal for facilitating the in-app messaging system.  

### Backend:
- **AWS CloudFormation**: Allows me to manage and develop the below services as code. It will be used to build a serverless REST API and deploy it as a stack.  
- **AWS Lambda**: Serverless compute for executing backend logic.  
- **AWS API Gateway**: For managing and exposing secure and scalable endpoints.  
- **AWS Cognito**: Will be used for user authentication and authorization.  
- **AWS Textract**: Used to extract users’ assessment schedules into a customizable format.  
- **AWS S3**: Used to store documents and images provided by users.  

### Database System:
- **Amazon RDS (MySQL)**: The case management system and student consultation will have complex relations and data structures that are unlikely to change, making SQL the best choice for this type of system.

### Additional Tools:
- **GitHub**: Source control management.  
- **GitHub Actions**: For creating a CI/CD Pipeline to automate code builds, testing, and deployment processes.  
- **SonarQube (via CI/CD)**: SAST tool that will analyse my codebase for vulnerabilities and ensure secure coding practices.  
- **Zed Attack Proxy (ZAP)**: DAST tool that will dynamically analyse the application during runtime for vulnerabilities.  
- **D3.js**: Enables data visualisation for students, clients, solicitors, and mentors.  
- **AWS CloudWatch**: Used to monitor backend logs.  
- **Postman**: For testing API functionality.  



