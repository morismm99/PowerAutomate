This flow gets the list of users with the System Administrator for the environment the flow is running on. The account has to have the Power Platform Administrator role or System Administrator role. The Dataverse list rows action has pagination enabled to be able to pull up to 100,000 records. The list of System Adminstrators is saved to an Excel file stored in OneDrive. This can be updated to a file in SharePoint Online or to update a SharePoint Online list.

The Excel File needs to have a sheet with a table in it with the following columns:

1. Username
2. First Name
3. Last Name
4. Email
6. Security Role

# To use this flow in your environment follow these steps:

## Import the flow package

1. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to
2. Click Solutions in the left menu
3. Select Import Solution from the top menu
4. Browse and choose the "ListSystemAdministrators_1_0_0_1.zip" package.
5. Click Next
6. Click Next on the details page
6. Choose Dataverse and Excel Online Business connections, or create them if these don't already exist
7. Click Import
8. The import will complete with warnings as the Excel action needs updated to point to your own Excel file
9. Update the flow as desired.
10. Save the flow