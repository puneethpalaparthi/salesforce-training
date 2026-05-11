Hands-on Implementation: Custom Field Creation
In this task, I extended the standard Salesforce data model by adding a custom currency field to the Contact object to track financial data for clients.
Step-by-Step Procedure:
 =>Navigate to Setup: Clicked the Gear Icon in the top-right corner and selected Setup.
 =>Access Object Manager: Selected the Object Manager tab from the top navigation bar.
 =>Locate Target Object: Searched for and clicked on the Contact object.
Initiate New Field:
 =>Selected Fields & Relationships from the sidebar.
 =>Clicked the New button.
Configure Data Type:
 =>Selected Currency as the Data Type to ensure the field handles monetary values correctly.
 =>Clicked Next.
Define Field Details:
 =>Field Label: Entered Loan Amount.
 =>Field Name: Automatically populated as Loan_Amount.
 =>Clicked Next.
Set Security & Visibility: * Accepted default field-level security to ensure visibility for all standard profiles.
 =>Added the field to all Contact Page Layouts so it appears on the user interface.
 =>Finalize: Clicked Save.
Technical Verification:
 =>Object: Contact
 =>API Name: Loan_Amount__c
Deployment Status: Successfully rendered on the Contact record detail page in the Dreamhouse app.
