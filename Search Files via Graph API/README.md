This flows searches all content in SPO and OneDrive using the graph API https://graph.microsoft.com/v1.0/search/query URI endpoint. It leverages the "Invoke an HTTP Request" action to do a search for files that have a specific metadata value in a custom choice column. We then grab those files and copy them to an on premise location, to keep a local copy of these files.

https://learn.microsoft.com/en-us/graph/search-concept-files#example-4-search-all-content-in-onedrive-and-sharepoint 

# Pre-reqs

* The user account running this flow needs to have access to any SPO site the flow needs to search against
* A managed property has to be created in SharePoint Online and mapped to an existing RefinableString. In this flow, a managed property has been created for a column called 'Process' and it has been ampped to RefinableString00 - more info here: https://sharepointmaven.com/how-to-create-a-managed-property-in-sharepoint-online/
* This flow uses the 'File Sytem' connector which requires a standard on premises data gateway to be install on the box where we will be copying files to
* This is a premium flow, so a standalone Power Automate license is needed

# To use this flow in your environment follow these steps:

## Setup on-premise data gateway for File System connector

1. Download the standard on premise data gateway and install to the on prem box where you want to create files on -https://learn.microsoft.com/en-us/data-integration/gateway/service-gateway-install#download-and-install-a-standard-gateway
2. Setup the gateway with the account that will be running the flow
3. Once the gateway is installed and configured go to https://flow.microsoft.com > Data > Connections > add a File System Connection
4. Root Folder example: C:\Shared\
5. Authentication Type example: Windows
6. Type in Username and Password for account with access to that machine
7. Choose the newly configured gateway

## Import the flow package

1. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to.
2. Click My Flows in the left menu.
3. Select Import.
4. Browse and choose the "SearchFilesGraphAPI-Custom-UsingAzureADInvokeWebRequest_20230113024209.zip" package which can be downloaded from this repo.
5. Choose create as new.
6. Choose the HTTP with Azure AD, SharePoint and File Sytem connections, or create them if these don't already exist.
7. The HTTP with Azure AD connection needs to be created and both base resource URL and Azure AD Resource URI need to point to https://graph.microsoft.com
8. Once all connections are configured, click Import
8. Open the flow when import is complete
9. You can now make any necessary modifications to the flow, add error checking (configure run after), etc.
10. Save the flow