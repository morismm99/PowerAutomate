This flow gets the list of users with the System Administrator for the environment the flow is running on. The account has to have the Power Platform Administrator role or System Administrator role. The Dataverse list rows action has pagination enabled to be able to pull up to 100,000 records. The list of System Adminstrators is saved to an Excel file stored in SharePoint. 

The flow includes all system administrators including system (#) accounts. The flow could be edited further by excluding those system accounts either in the expand query or by adding a Filter Array action after the "List Users - Security Roles" Dataverse action.

The Excel File needs to have a sheet with a table in it with the following columns:

1. Username
2. First Name
3. Last Name
4. Email
6. Security Role

# To use this flow in your environment follow these steps:

## Import the ListSystemAdministrators unmanaged solution

1. You can download the PPEnvironmentSystemAdministrators.xlsx file and upload it to your SharePoint Online document library.
2. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to
3. Click Solutions in the left menu
4. Select Import Solution from the top menu
5. Browse and choose the "ListSystemAdministrators_1_0_0_2.zip" package.
6. Click Next
7. Click Next on the details page
8. Choose Dataverse and Excel Online Business connections, or create them if these don't already exist
9. Click Import
10. Open the "Get System Administrator" flow and update the "Add row into table" action, updating the Location, Document Library, File, and Table.
11. Save the flow