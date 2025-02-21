---
layout: default
title: Design
---
# Project Design 

For a deeper look at my project, my desgin document can be seen here: 
**[Semester 1 Design Document]({{ 'assets/docs/Report.pdf' | relative_url }})**

## Architecture

### Backend 
- The backend will be created using *Cloud Formation*. There will be two stacks one that provides authentication (AWS Cognito) and one that provides the PWA to access AWS services through API calls. The below image give an overview of the backend that will be constructed. (This is an oversimplification, there will be more lambdas used)

<div style="text-align: center; margin: 10px">
  <img src="{{'/assets/images/AWS.png' | relative_url }}" alt="AWS" style="width: 700px; border-radius: 10%;" />
</div>

--- 

## Database Design 
### CMS Entity-Relationship Diagram (ERD)

- The below ERD shows how the different enities relate to each other and what information will be stored. This gives a good overview of the capabilities of the CMS system.

<div style="text-align: center; margin: 10px">
  <img src="{{'/assets/images/CMS.png' | relative_url }}" alt="CMS ERD" style="width: 700px; border-radius: 10%;" />
</div>

### Student/Mentor Entity-Relationship Diagram (ERD)
- Much like the above ERD, this diagram demonstrates how each enity will relate to each other. Again, giving a good idea of the information that will be stored on both; student and client.

<div style="text-align: center; margin: 10px">
  <img src="{{'assets/images/StudentERDV2.png' | relative_url }}" alt="CMS ERD" style="width: 700px; border-radius: 10%;" />
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

The above site map shows how a particular user type will filter through the Progress Web App. It's important to note that the PWA is serving four distinct user types, which can be seen by the colours in the site map. It also shows what each user will have access to.

