---
layout: default
title: Design
---
# Project Design 

For a deeper look at my project, my desgin document can be seen here: 
**[Semester 1 Design Document]({{ 'assets/docs/20096529-JordonCoady-FYP-Semester-One-Report.pdf' | relative_url }})**

Follow my project here:
**[EduCase Repository](https://github.com/JRDNVI/Student-Legal-Consultation)**

## Architecture

### Backend 
- The backend will be created using CloudFormation, consisting of two stacks: one for authentication (AWS Cognito) and one for providing the PWA to access AWS services through API calls. The image below gives an overview of the backend architecture that will be constructed (note that this is an oversimplification, as more Lambdas will be used).

<div style="text-align: center; margin: 10px">
  <img src="{{'/assets/images/AWS.png' | relative_url }}" alt="AWS" style="width: 700px; border-radius: 10%;" />
</div>

--- 

## Database Design 
### CMS Entity-Relationship Diagram (ERD)

- The ERD below shows how the different entities relate to each other and what information will be stored. It provides a clear overview of the capabilities of the CMS system.

<div style="text-align: center; margin: 10px">
  <img src="{{'/assets/images/CMS.png' | relative_url }}" alt="CMS ERD" style="width: 700px; border-radius: 10%;" />
</div>

### Student/Mentor Entity-Relationship Diagram (ERD)
- Similar to the ERD above, this diagram demonstrates how each entity will relate to one another, providing a clear understanding of the information that will be stored for both students and clients

<div style="text-align: center; margin: 5px">
  <img src="{{'/assets/images/StudentERDV2.png' | relative_url }}" alt="CMS ERD" style="width: 700px; border-radius: 10%;" />
</div>

--- 

## Matching Algorithms

### Client Registration Flow

<div style="text-align: center; margin: 10px">
  <img src="{{'/assets/images/clientR.png' | relative_url }}" alt="CMS ERD" style="width: 700px; border-radius: 10%;" />
</div>

The above figure shows the flow of a new client creating an account. They will be asked
to complete a form that builds a client profile. This profile will contain the following
information:
  - Required legal service type (e.g., family law, business law).
  - Budget constraints.
  - Solicitor Characteristics:
    - Experience: Number of years of practice, areas of expertise.
    - Case History: Previous cases handled, success rate.
    - Languages Spoken

The client profile will be passed to an algorithm which will utilise rule-based matching. The algorithm will apply matching rules and calculate a ranking for solicitors.



### Student Registration Flow

<div style="text-align: center; margin: 10px">
  <img src="{{'/assets/images/StudentR.png' | relative_url }}" alt="CMS ERD" style="width: 700px; border-radius: 10%;" />
</div>

The above system will function the same as discussed in the client registration flow
section. The same algorithm will be used for mentor allocation, but using different
matching criteria, which can be seen in the above image . 

---

## Frontend 
### Site Map

<div style="text-align: center; margin: 10px">
  <img src="{{'/assets/images/siteMap.png' | relative_url }}" alt="CMS ERD" style="width: 700px; border-radius: 10%;" />
</div>

The above site map illustrates how each user type navigates through the Progressive Web App (PWA). It’s important to note that the PWA serves four distinct user types, which are represented by different colors in the site map. Additionally, the map highlights the features and access available to each user type.

