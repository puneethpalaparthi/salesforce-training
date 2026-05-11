Hands-on Implementation: Subscribing with Apex Triggers
After defining the event, I implemented an Apex Trigger to act as a subscriber. This trigger "listens" for incoming event messages and automatically creates follow-up tasks, showcasing how Salesforce decouples publishers from consumers.
 Step-by-Step Procedure:
  =>Open Developer Console: Clicked the Gear Icon and selected Developer Console.
Create New Trigger:
  =>Navigated to File | New | Apex Trigger.
  =>Name: OrderEventTrigger.
  =>sObject: Selected Order_Event__e.
Implement Subscription Logic:
  =>Used the after insert event, which is the only trigger event supported by Platform Events.
  =>Created a List<Task> to handle bulk processing (Best Practice).
Define Business Rules:
  =>Iterated through Trigger.New. 
  =>Added a conditional check: if (event.Has_Shipped__c == true).
Mapped event data to new Task fields:
  =>Priority: 'Medium'.
  =>Subject: 'Follow up on shipped order ' + event.Order_Number__c.
  =>OwnerId: event.CreatedById.
  =>DML Operation: Executed insert tasks to commit the new records to the database.
Verify & Test:
  =>Used the Execute Anonymous window to publish a test event.
  =>Verified that a new Task was automatically generated under the correct user.
  <img width="1254" height="1001" alt="Screenshot 2026-05-11 193857" src="https://github.com/user-attachments/assets/fb13bff4-4a1b-431e-b084-a6f34aebfbf2" />

Final Output:
<img width="1262" height="1012" alt="Screenshot 2026-05-11 194012" src="https://github.com/user-attachments/assets/84c2f4b9-fbdd-455c-88b6-8973b56f39f4" />
