This flow was put together in collaboration with Jake Gwynn, please check his GitHub repo for more amazing conent - https://github.com/JakeGwynn

This flow gets the list of users with the System Administrator for ALL environments. Thus, it only needs to be imported/configured on one environment, such as the environment running the CoE Starter kit. The account has to have the Power Platform Administrator role. The legacy Dataverse connector is used, which allows you to work with other environments apart from the one the flow is running on. The flow also grabs Dataverse for Teams System Administrators (Office 365 Group owners). All system admins are saved to an array variable. This data can be added to a SharePoint Online list, CSV file, spreadsheet, Dataverse table, etc.

The flow includes only user system administrators and application type users. It does not include other system (#) accounts with the System Adminstrator role. This can be of course twaked to include all accounts with the system administrator role.

# To use this flow in your environment follow these steps:

## Import the flow package

1. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to.
2. Click My Flows in the left menu.
3. Select Import.
4. Browse and choose the "GetallEnvironmentSystemAdmins_20230113024922.zip" package.
5. Choose create as new.
6. Choose Dataverse, Office 365 Groups and Power Plaform for Admins connections, or create them if these don't already exist.
7. Click Import.
8. Open the flow when import is complete.
9. Make any desired changes (update trigger to a scheduled trigger as currently it is a button trigger and decide where to store the output of system administrators)
10. Save the flow.