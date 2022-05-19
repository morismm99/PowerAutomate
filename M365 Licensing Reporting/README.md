This flow queries the /subscribedskus MS Graph endpoint:

https://docs.microsoft.com/en-us/graph/api/subscribedsku-get?view=graph-rest-1.0&tabs=http

The flow needs an Azure App Registration with organization.read.all and directory.read.all application or delegated type permissions. This is because we are going to use the premium HTTP action to do REST API calls to the MS Graph.

To use this flow in your environment follow this steps:

1. Create a SharePoint Online list with the following columns:

Title;
SkuID (single line of text);
ConsumedUnits (single line of text);
PrepaidUnits (single line of text);
RemainingUnits (single line of text);
Date (Date and time - date only)

2. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to
3. Click My Flows in the left menu
4. Select Import
5. Browse and choose the "GetM365usbscribedSKUSV2_20220519143721.zip" package.
6. Choose create as new
7. Choose SharePoint and Outlook 365 connections, or create them if these don't already exist
8. Click Import
9. Open the flow when import is complete
10. Update the AzureTenantID, AppRegistrationID, AppSecret, SiteURL, SPO List, and AdminEmail variables with your actual tenant information.
14. Save the flow