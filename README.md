Salesforce United Solar - Project 1 Solo

United Solar is a solar panel production and installation company that needs your help to set up their new Salesforce environment. After a meeting with their corporate management, a number of use cases have been identified. We need you and your team in order to implement these features so that the United Solar team can start their work in their new Salesforce environment.
 
Directions: Each associate must choose use cases from a variety of categories (minimum of 3) and complete them. Submit to your trainer this document filled out with the associate assigned to each use case. Each use case is assigned a number of points. In order to receive 100%, you must score 100 points. Each category has a maximum number of points that can come from it. For larger use cases, multiple associates can be put as having responsibility but each associate must have at least 1 use case per category that they are the only one marked down for.
 
Analysis: Before starting work on the project, the team must perform analysis on the use cases. First, an ERD must be crafted to support the needs of United Solar mentioned below. In addition to this ERD, the team must submit a document analyzing the chosen use cases and the best tool to complete the use case. Compare the available tools and select the most appropriate one.

United Solar, as mentioned earlier, is a solar panel production and installation company. Their solar panel products are sold to both businesses and households and the sales representatives need to often get in contact with these places. Sometimes, our sales reps get some lead on a potential sale and they like to have that distinguished from the businesses that United Solar has already sold to. Businesses are often repeat customers, and our sales reps also like to have those upcoming deals tracked. Businesses can often pay the entire installation amount up front, but often times households need to pay in installations using payment receipts. In case of issues with the products, United Solar also would like a ticketing system set up. The installation of certain solar panels requires a certification, or multiple. United Solar wants to keep track of the certifications a solar panel needs for installation and which engineers hold that certification. When an installation is requested, it's tracked through a work order. Finally, internal employees, especially engineers, need to be able to make reimbursment requests for expenses when they're on installation.
 
# Categories

## Configuration and Setup (20 points)
### 2	points
    United Solar does business in the United States, Korea, and Japan. They need to allow their employees to see prices in the dollar, won and yen currencies.
### 2	points
    United Solar's fiscal year begins in February, but is otherwise the same as a normal fiscal year. They would like this reflected in Salesforce.
### 2	points
    United Solar wants the New User email link to expire in 1 day instead of 7 days.
### 2	points
    United Solar wants to have objects worked on by engineers to be in their own place and objects worked on by the support staff in another dedicated place so that these roles can easily access objects they work on.
### 10	points
    At the start, United Solar wants 5 users to be able to access Salesforce:
    Jon is an Engineer who needs to see certifications he holds, work orders he is assigned, and reimbursement requests he has made. He also needs to see all businesses and households.
    Lisa is the Engineering Lead and needs to see and edit all certifications, solar products, and work orders. She also needs to be able to see all businesses, reimbursement requests, leads and opportunities.
    Damian is in HR and needs to see all records except certifications.
    Alexandra is a Support Rep and needs to see and edit support tickets, orders, payment receipts, business and household records, and contact records. She also needs to see all solar products.
    Cory is in Finance and needs to see solar products, work orders, business and household records, contact records, reimbursement requests and payment receipts. He only needs to see these records and should only be able to edit the "Status" field of payment receipts, which should be one of 3 values: New, Approved, Rejected
    Don't forget, you are a user as well! You are the Salesforce Admin!
### 2	points
    Lisa wants to be able to easily add new certifications to an engineer while they're looking at that engineers information.
### 2	points
    While still setting everything up, we don't want users to be able to log in. However, you still need to verify security for each user. Make sure that you can log in as that user, but they cannot log in themselves and are not given the chance to login.
### 1	points
    HR should not be able to log in outside of work hours (9:00am - 5:00pm).
### 1  points
	All login attempts outside of the company building (IP Address 198:172:1:38) should have to complete some multifactor authentication step.
### 2	points
    United Solar wants to make sure the sensitive data accessible by HR representatives remains secure. In order to accomplish this, they request that HR passwords should expire every 30 days. They also want all users to have the last 4 passwords remembered when setting a new password.
### 2	points
    United Solar wants to have 15 users with the Chatter External license for their partners. However, they do not want them to be able to log in yet, so make sure they don't get sent a password. You may assign them any name you want, since it will be changed later when United Solar is ready.
