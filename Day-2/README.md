Salesforce Platform Basics & Architecture:
1. What is the Salesforce Platform?
   The Salesforce Platform is a cloud-based development environment that extends the reach and functionality of the CRM. It acts as an integrated foundation that unites marketing, sales, commerce, service, and IT teams with a single, shared view of the customer.
   Core Architecture Layers:
   Trust: Salesforce’s top priority, ensuring data security and transparency via trust.salesforce.com.
   Multitenancy: Like an apartment building, multiple organizations share the same infrastructure and resources while maintaining private, secure data spaces.
   Metadata: "Data about data." This defines the structure (shells) of the org, such as objects and fields, allowing the platform to auto-generate the user experience.
   APIs: Robust interfaces that allow different software systems to connect and exchange information seamlessly.
2. Platform Building Blocks
   App: A collection of objects, tabs, and functionality that supports a specific business process.
   Object: A database table used to store a particular kind of information (e.g., Accounts, Contacts, or custom objects).
   Tab: A visual element that allows users to access objects and features within an App.
3. Configuration vs. Coding (Declarative vs. Programmatic)
   Salesforce allows for high-impact development with low effort through its no-code and low-code tools.
   Feature:Configuration (No-Code/Low-Code) | Coding (Programmatic)
   Tools:"Lightning App Builder, Flow Builder, Schema Builder. | Apex, Lightning Web Components (LWC), JavaScript."
   Benefit:"Fast implementation, easy maintenance, no coding skills required. | Handles complex logic and integrations that ""clicks"" cannot solve."
   Example 1:"Creating a Currency Field for ""Loan Amount"" on the Contact object. | Writing an Apex Trigger to automate complex record reassignments.
   Example 2:Building a Screen Flow to guide users through a new property listing | Developing a custom LWC Map to visualize property locations.
4. Event-Driven Architecture
   Platform Events enable a Publisher-Subscriber model, allowing decoupled systems to communicate in near-real-time.
   Publishing: Events can be sent via Apex (EventBus.publish()), Flows (Create Records), or APIs.
   Subscribing: Salesforce apps "listen" using Apex Triggers (after insert) or Flows to take immediate action.
5. System Design: College Management System
   Refining the Day 1 system design into the Salesforce Platform structure:
   App Name: University Excellence Hub
**Core Objects:
   Student (Student__c): Stores academic and personal records.
   Course (Course__c): Manages the curriculum and enrollment.
   Placement (Placement_Record__c): Tracks recruitment drives and job offers.
**Platform Customization:
   Field: Added a "Has_Placed" checkbox to the Student object.
   Automation: A Flow that triggers a Platform Event (Placement_Event__e) when a student is hired, notifying the external Alumni Badge system.
6. Trailhead Progress & Screenshots
  =>Agentforce 360 Platform Basics:
   <img width="1842" height="723" alt="platform" src="https://github.com/user-attachments/assets/91bae111-0efd-44bf-8790-2f8029fc54da" />
  =>Agentforce 360 Platform Development Basics:
   <img width="1891" height="680" alt="develop" src="https://github.com/user-attachments/assets/7be4c5a1-3895-482b-9e80-585a401d633a" />
  =>Agentforce 360 Platform Events Basics:
   <img width="1821" height="570" alt="events" src="https://github.com/user-attachments/assets/7ea6ef37-68bf-4b20-b736-019c4ef08c35" />
