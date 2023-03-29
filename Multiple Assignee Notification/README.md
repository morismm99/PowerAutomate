This flow example leads to an email notification being sent to an assignee, with a list of items assigned to them. The assignees column allows for multiple selection. This will send 1 email to each assignee with a list of items that meet the criteria per the ODATA filter specified in the Get Items action.

Credit to Tom, as he has a great blog post outlining this process - https://tomriha.com/get-items-for-each-user-in-multiple-people-picker-field-power-automate/


# To use this flow in your environment follow these steps:

## Option 1: Import the flow package

1. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to.
2. Click My Flows in the left menu.
3. Select Import.
4. Browse and choose the "MultipleAssigneeNotification-IndividualEmailwithlistofitemsassigned_20230329154653.zip" package which can be downloaded from this repo.
5. Choose create as new.
6. Choose the SharePoint and Outlook connections, or create them if these don't already exist.
8. Once all connections are configured, click Import.
8. Open the flow when import is complete.
9. You can now make any necessary modifications to the flow, add error checking (configure run after), etc.
10. Save the flow.

## Option 2: Import the solution (if flow package import fails)

1. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to
2. Click Solutions in the left menu
3. Select Import Solution from the top menu
4. Browse and choose the "MultipleAssigneeNotifications_1_0_0_2.zip" package.
5. Click Next
6. Click Next on the details page
7. Choose SharePoint and Outlook connections, or create them if these don't already exist
8. Click Import
9. Open the "Multiple Assigneed Notification - Individual Email with list of items assigned" flow and update the flow accordingly.
10. Save the flow (you may also want to save a coyp of this flow if you don't need to be inside of a solution or inside of another existing solution)