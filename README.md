# Salesforce United Solar - Project 1 Solo
- [Project_1](/Project_1.xlsx)

United Solar is a solar panel production and installation company that needs your help to set up their new Salesforce environment. After a meeting with their corporate management, a number of use cases have been identified. We need you and your team in order to implement these features so that the United Solar team can start their work in their new Salesforce environment.
 
Directions: Each associate must choose use cases from a variety of categories (minimum of 3) and complete them. Submit to your trainer this document filled out with the associate assigned to each use case. Each use case is assigned a number of points. In order to receive 100%, you must score 100 points. Each category has a maximum number of points that can come from it. For larger use cases, multiple associates can be put as having responsibility but each associate must have at least 1 use case per category that they are the only one marked down for.
 
Analysis: Before starting work on the project, the team must perform analysis on the use cases. First, an ERD must be crafted to support the needs of United Solar mentioned below. In addition to this ERD, the team must submit a document analyzing the chosen use cases and the best tool to complete the use case. Compare the available tools and select the most appropriate one.

United Solar, as mentioned earlier, is a solar panel production and installation company. Their solar panel products are sold to both businesses and households and the sales representatives need to often get in contact with these places. Sometimes, our sales reps get some lead on a potential sale and they like to have that distinguished from the businesses that United Solar has already sold to. Businesses are often repeat customers, and our sales reps also like to have those upcoming deals tracked. Businesses can often pay the entire installation amount up front, but often times households need to pay in installations using payment receipts. In case of issues with the products, United Solar also would like a ticketing system set up. The installation of certain solar panels requires a certification, or multiple. United Solar wants to keep track of the certifications a solar panel needs for installation and which engineers hold that certification. When an installation is requested, it's tracked through a work order. Finally, internal employees, especially engineers, need to be able to make reimbursment requests for expenses when they're on installation.

PACKAGE ALL OF THIS INTO AN UNLOCKED PACKAGE; UPLOAD IT TO A REPO AS WELL!
 
# Categories
## Configuration and Setup (Max Points: 20)
### 2	points
United Solar does business in the United States, Korea, and Japan. They need to allow their employees to see prices in the dollar, won and yen currencies.
### 2	points
United Solar's fiscal year begins in February, but is otherwise the same as a normal fiscal year. They would like this reflected in Salesforce.
### 2  points
United Solar wants the New User email link to expire in 1 day instead of 7 days.
### 2  points
United Solar wants to have objects worked on by engineers to be in their own place and objects worked on by the support staff in another dedicated place so that these roles can easily access objects they work on.
### 10 points
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
### 2  points
United Solar wants to have 15 users with the Chatter External license for their partners. However, they do not want them to be able to log in yet, so make sure they don't get sent a password. You may assign them any name you want, since it will be changed later when United Solar is ready.


## Object Manager and Lightning App Builder (Max Points: 20)
###	12	points	
Implement the ERD. Add in custom fields you think would be useful to track on each object.

###	2	points	
United Solar sells to both businesses and households. Most of the values are the same between the two, but they would like a way of distinguishing if a business is a household or corporation. Fields not relevant to households should not be displayed for households and fields not relevant for businesses should not be displayed for businesses.

###	2	points	
Work Orders should have the field tracking the next action date hidden when they are completed.

###	4	points	
Orders should have a field that displays how much money is owed that subtracts the amount paid from the payment receipts related to the order from the amount of the order. This should only include payment receipts that have a status of approved.

###	2	points	
The engineering team only needs to use the following fields on business records, so de-clutter their view of the record:
Owner, Name, Phone Number, Fax, Website, Address. They should still have access to these fields, they simply don't need to see them on the record view.

###	2	points	
For business records, Owner, Name, Phone Number, Fax, Website and Address are all commonly used fields. United Solar wants them to be displayed in the most convenient place so that they are visible at all times on the record page.

###	2	points	
Make it easy to see all the users with certifications and all the products a certification certifies for - from a certifications record page.


## Sales and Marketing Applications (Max Points: 12)
###	1	points	
United Solar wants to be able to see if an opportunity is affecting a current marketing campaign from the opportunity record page.
###	6	points	
United Solar wants to ensure their opportunities are always related to some solar products, so they want to have a prompt appear to have users add these solar products to their opportunities when the opportunity does not have products associated with it.
###	2	points	
For work orders, United Solar uses the following process to track progress on them:
New > Assigned > Planning > Working > New Estimate Required > Done
United Solar wants this process displayed prominently on a work order record page, ideally as some kind of banner.
###	1	points	
United Solar would like all leads from the engineering industry assigned automatically to Lisa.
###	2	points	
United Solar would like a list of people to be emailed when opportunities reach or exceed a $500,000 amount with a 75% likelihood. This list is currently just Lisa, but may change in the future and the delegated admin responsible for it will not understand flows, so make sure he doesn't have to update a flow.
###	2	points	
United Solar would like a premier set of prices for their products that are at a 15% discount.
###	4	points	
United Solar plans on making a number of reports on their opportunity pipeline using Salesforce's forecast category. However, they would like to modify the existing process a bit:
- They would like three additional stages after Proposal/Price Quote - Hot with 95% probability and Best Case forecast category, Warm with 90% probability and Commit forecast category, Cold with 85% probability and Commit forecast category.
- They would like to remove the Negotiation/Review stage
- United Solar does some work for charities for heavily reduced cost. They would like these opportunities tracked using the same process as Salesforce's default, but they would like all forecast categories changed to omitted except for Closed Won, so that they don't contributue to the pipeline until won.


## Service and Support Applications (Max Points: 11)
###	1	points	
United Solar wants to make sure that contacts and support reps have a quick way of communicating with each other besides email. This should be visible to the support rep on the support ticket page.
###	2	points	
United Solar wants support tickets that have had a "New" status for over 2 days to be escalated and assigned to Alexandra.
###	3	points	
United Solar plans on adding more support specialists in the future, but just to get started they would like all support tickets to be assigned to a queue that has both the admin and Alexandra. If a ticket's reason is for Breakdown or Perfomance, they would like it automatically assigned to Alexandra though.
###	3	points	
United Solar would like to send an automated email when a customer submits their ticket and when the ticket changes status to "Accepted".
###	2	points	
United Solar would like all emails sent to a specific email address to be made into a case. They don't have the email set up right now, so just use your own email until then.
###	8	points	
United Solar wants to ensure that the expert understanding of certain tickets are available for all their support reps, so they would like a place for their experts to write and share this information. To organize things, they want these articles to be divided into 4 categories: Missing Part, Installation Error, Capacitor Overheat, and Faulty Charge Capture. Write a placeholder article for all of these categories.
###	3	points	
United Solar uses a unique process for working through support tickets. Their process uses these steps:
New > Accepted > In Progress > Delayed > Closed (Success) > Closed (Failed)


## Productivity and Collaboration (Max Points: 7)
###	2	points	
United Solar would like their mobile branding to match their company colors: #E92425 as a brand color and #FFBE58 as a loading page color with the United Solar logo on the loading page.
###	2	points	
United Solar would like for Certifications and Work Orders to be able to be put on calendars and have tasks related to them.
###	3	points	
The CEO of United Solar would like a place in Salesforce to make announcements to the entire company.


## Data and Analytics Management (Max Points: 14)
###	2	points	
United Solar is interested in keeping a backup of their Salesforce data. Present a written document analyzing the options available and the pros and cons of each solution.
###	2	points	
The Next Payment Due Date field on Orders should always be in the future when being set.
###	2	points	
The Payment Amount on a Payment Receipt should never be more than the remaining amount to be paid on an Order.
###	8	points	
The Finance team would like to have a place to see several reports easily. Here are the reports that they would like:
- A report on the amount of money owed on active orders
- A report on the number of hot rated business, broken down by region
- The amount of money spent on reimbursments
###	3	points	
Lisa would like to be updated to the report on the money owed on active orders when there is more than a 10% difference between the amount charged and amount paid. For example, if $100 is charged but only $85 have been paid, Lisa would like to know
###	3	points	
Import some sample data to aid in your development. 10 records of each should be helpful. Make sure to create a .csv so that your team can import the data as well


## Workflow/Process Automation (Max Points: 16)
###	3	points	
United Solar would like each reimbursment request to go through approval first by the manager of whoever created the request, and then a member of Finance.
###	5	points	
Every month, United Solar would like to send out a thank-you email to their hot rated businesses.
###	6	points	
Engineers should be automatically given read access to the solar products they are certified to work on
###	5	points	
When the Next Payment Due Date is in two days, a contact from the business that made the order should be emailed a reminder
###	3	points	
An engineer should be emailed when they are assigned to a work order
