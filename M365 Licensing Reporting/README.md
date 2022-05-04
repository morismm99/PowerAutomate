This flow queries the /subscribedskus MS Graph endpoint:

https://docs.microsoft.com/en-us/graph/api/subscribedsku-get?view=graph-rest-1.0&tabs=http

The flow needs an Azure App Registration with organization.read.all and directory.read.all application or delegated type permissions. This is because we are going to use the premium HTTP action to do REST API calls to the MS Graph.

To use this flow in your environment follow this steps:

1. Create a SharePoint Online list with the following columns:

Title
SkuID (single line of text)
ConsumedUnits (single line of text)
PrepaidUnits (single line of text)
RemainingUnits (single line of text)
Date (Date and time - date only)

2. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to
3. Click My Flows in the left menu
4. Select Import
5. Browse and choose the "GetM365usbscribedSKUSV1_20220504203506.zip" package.
6. Choose create as new
7. Choose SharePoint and Outlook 365 connections, or create them if these don't already exist
8. Click Import
9. The import will fail, but you can click "Save as new flow," and you will be able taken into edit mode for this flow
10. Update the HTTP action with your app registration information
11. Expand the Apply to Each, and set the connection for the Create item SharePoint action.
12. Replace the site and list accordingly - the columns should pre-populate along with the dynamic content as per the template
13. Set the connection for the Send an Email (v2) action - customize the html further if needed.
14. Save the flow
