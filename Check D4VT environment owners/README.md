This flow can be used and ran on a schedule to take action (send an email for example) on Dataverse for Teams environments who are currently ownerless.

This flow requires the account configuring the flow to be a Power Platofrorm Administrator and have the User Administrator role in AAD.

# To use this flow in your environment follow these steps:

## Option 1: Import the flow package

1. Go to https://flow.microsoft.com and make sure you are in the environment you want to import the flow to.
2. Click My Flows in the left menu.
3. Select Import.
4. Browse and choose the "GetD4VTEnvironmentOwners_20230331185024.zip" package which can be downloaded from this repo.
5. Choose create as new.
6. Choose the Azure AD, Office 365 Groups and Power Platform for Admins connections, or create them if these don't already exist.
8. Once all connections are configured, click Import.
8. Open the flow when import is complete.
9. You can now make any necessary modifications to the flow, add error checking (configure run after), etc.
10. Save the flow.