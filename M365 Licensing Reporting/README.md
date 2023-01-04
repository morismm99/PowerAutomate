This flow queries the /subscribedskus MS Graph endpoint:

https://docs.microsoft.com/en-us/graph/api/subscribedsku-get?view=graph-rest-1.0&tabs=http

The flow needs an Azure App Registration with organization.read.all and directory.read.all application or delegated type permissions. This is because we are going to use the premium HTTP action to do REST API calls to the MS Graph.

# To use this flow in your environment follow these steps:

## Create a SharePoint Online list with the following columns:

1. Title
2. SkuID (single line of text)
3. ConsumedUnits (single line of text)
4. PrepaidUnits (single line of text)
5. RemainingUnits (single line of text)
6. Date (Date and time - date only)

## Import the flow package

1. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to
2. Click My Flows in the left menu
3. Select Import
4. Browse and choose the "GetM365usbscribedSKUSV2_20220519143721.zip" package.
5. Choose create as new
6. Choose SharePoint and Outlook 365 connections, or create them if these don't already exist
7. Click Import
8. Open the flow when import is complete
9. Update the AzureTenantID, AppRegistrationID, AppSecret, SiteURL, SPO List, and AdminEmail variables with your actual tenant information.
10. Save the flow