Hands-on Implementation: Defining a Platform Event
In this challenge, I designed a Platform Event to facilitate real-time communication between an external order system and Salesforce. Unlike standard objects, this event acts as a secure, scalable notification.
 Step-by-Step Procedure:
  =>Locate Platform Events: Entered Platform Events in the Setup Quick Find box and selected the menu item.
  =>Define Event Metadata:
  =>Label: Order Event.
  =>Plural Label: Order Events. 
  =>Object Name: Order_Event.
  =>Description: Information about a customer order.
  =>Configure Publish Behavior:
  =>Set to Publish Immediately.
Note: This ensures the event is broadcast as soon as the call is made, without waiting for the database transaction to commit.
Create Custom Fields:
  =>Field 1: Selected Text data type, labeled it Order Number, and set the length to 10.
  =>Field 2: Selected Checkbox data type and labeled it Has Shipped.
  =>Finalize: Clicked Save.
Technical Verification:
  =>API Name: Order_Event__e (The __e suffix identifies it as a Platform Event).
  =>Retention: The event is stored in the Salesforce Event Bus for 72 hours, allowing for replay if connection issues occur.
  =>Visibility: Confirmed that while data exists in the bus, it is not viewable via standard UI reports or list views.
Subscribing to the Event (Apex Trigger)
To make this event functional, I implemented an Apex Trigger to "listen" for these notifications and take action.
 Procedure:
  =>Open Developer Console: Navigated to File | New | Apex Trigger.
  =>Define Trigger: Named it OrderEventTrigger and tied it to the Order_Event__e sObject.
Implement Logic:
  =>Wrote an after insert trigger.
  =>Added logic to check if Has_Shipped__c == true.
If true, the trigger automatically creates a Task record for the user to follow up on the shipment.
ScreenShots:
Order Creation :
<img width="1465" height="614" alt="order" src="https://github.com/user-attachments/assets/8b9862f4-6f97-432f-8629-957b99672781" />
Custom Feild Creation:
<img width="1468" height="590" alt="subs" src="https://github.com/user-attachments/assets/19c80adb-f6a6-4b67-b7b0-a74886e871a3" />
Final Output:
<img width="1546" height="467" alt="Screenshot 2026-05-11 193437" src="https://github.com/user-attachments/assets/1b4082d2-1233-4df1-a178-1c3d23bf5f47" />
<img width="1555" height="371" alt="Screenshot 2026-05-11 193455" src="https://github.com/user-attachments/assets/43bbc7cc-69aa-4646-83c8-251b52abc11f" />
