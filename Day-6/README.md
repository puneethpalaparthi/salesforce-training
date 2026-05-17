Triggers, SOQL, & Ecosystem Basics
 Repository Structure
/day6-triggers-soql/ - Core technical tasks and deep dives.  
/light-completion-day/ - Ecosystem exposure and quick reflections.
Part 1: Core Technical Learning:
1. What is SOQL?
   SOQL (Salesforce Object Query Language) is used to search your organization’s Salesforce data for specific information.
   Unlike SQL, it is specifically designed for Salesforce objects and is used only for retrieving records (SELECT operations) rather than modifying them.
2. What is an Apex Trigger?
   An Apex Trigger is a piece of code that executes before or after specific data manipulation language (DML) events occur, such as inserting, updating, or deleting records.
   They allow for custom automated actions that aren't possible through standard configuration.
3. Key Differences:
   Flow vs. Trigger: Flows are declarative (point-and-click) and preferred for simple automation like email notifications.
   Triggers are programmatic (code) and used for complex logic, high-performance bulk processing, or external API integrations.
   Before vs. After Trigger: Before triggers are used to update or validate record values before they are saved to the database.
   After triggers are used to access field values set by the system (like a Record ID) and to affect changes in other related records.
4. Trigger Use Cases (College Management System):
   Based on a College Management System, here are 5 automated cases:
   Student Registration: After a student record is created, automatically send a welcome email and generate a student ID.
   Course Enrollment: After a course reaches its maximum capacity, automatically notify the faculty head to open a new section.
   Low Attendance: After attendance data is updated, if it falls below 75%, trigger a warning notification to the student.
   Fee Payment: After a successful payment record is inserted, automatically update the student's "Eligibility Status" to active.
   Faculty Assignment: Before a course record is saved, verify if the assigned faculty is already teaching more than 3 courses.
5.English Query Examples
   Find all students currently enrolled in "Course A".
   List all courses currently handled by "Faculty X".
   Retrieve all students whose attendance percentage is below 75%.
6. Reflection: Why Event-Driven Behavior?
   Enterprise systems need event-driven behavior to ensure data integrity and real-time responsiveness.
   Instead of users manually checking for changes (polling), the system reacts instantly to data changes, reducing manual errors and increasing organizational efficiency.
Part 2: Ecosystem Exposure:
1. Modules Completed
   Search Solution Basics: Learned how Salesforce indexes data to find records efficiently.
   Agentforce 360 Platform Events Basics: Explored how different systems communicate asynchronously through events.
2. Key Learnings
   Search: Fast, accurate search is vital in enterprise systems to maintain user productivity when dealing with thousands of records.
   Platform Events: A single action (like a "Payment Completed") can notify multiple internal and external systems simultaneously without them being directly linked.
   CLI: Developers prefer CLI because it allows for scripting, automation, and handling complex tasks much faster than clicking through multiple GUI screens.
   Command-Line Interface (CLI): Understood why developers use terminal-based tools for faster workflows
   ScreenShots:
   <img width="1874" height="707" alt="Data1" src="https://github.com/user-attachments/assets/b9246c08-00c0-4efe-9272-ebb00eb11be9" />
   <img width="1850" height="662" alt="Data2" src="https://github.com/user-attachments/assets/9b99ea22-4b1d-494a-bd38-09bc2d50e9d7" />
   <img width="1863" height="723" alt="Data3" src="https://github.com/user-attachments/assets/02ee0176-8d1c-4bed-b7b2-8794a4575c25" />
   <img width="1845" height="721" alt="Data4" src="https://github.com/user-attachments/assets/ca2b78c2-eed5-4b2a-bda9-5610e3ff5270" />
   <img width="1900" height="719" alt="Data5" src="https://github.com/user-attachments/assets/4b956c46-6271-48a7-a260-ef5a120433e0" />
