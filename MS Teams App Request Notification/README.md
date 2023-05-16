# MS Teams App Request Notification

Do you want to use your own app request process/form for requests to unblock apps in MS Teams? If so, this would allow you to create something like an MS Form and redirect users to fill it out which can kick off a Power Automate cloud flow to send notifications via Teams or drive further automation.

In the Teams Admin Center, [a Teams Admin can modify the default setting to receive user requests on your custom webpage.](https://learn.microsoft.com/en-us/MicrosoftTeams/user-requests-approve-apps#modify-the-default-setting-to-receive-user-requests-on-your-custom-webpage)

This (sample) custom solution uses the following:
 
1. MS Form owned by a group for users to submit app requests.
2. SharePoint Online list to store app requests.
2. Power Automate flow that triggers when new responses are submitted, stores them on the SPO list and sends a notification to a Team's channel.

Additional functionality/automation can be built, but keeping this simple as a starting point.

## MS Form

The first step is creating a [Microsoft Form](https://forms.office.com). It is recommended to create this form inside of an M365 Group. * *You can add additional questions of coure. If you do this, you will need to create additional columns to store that data in the SPO list.* * 

**Form questions**:

1. What is the name of the app you are requesting? (Text)
2. Please provide the link/URL to the app which can be found in MS Teams via the copy link right next to the Request Approval button. (Text)
3. Please provide a business justification for this application. (Text - Long answer)

**Form settings**:

![Form Settings](https://github.com/morismm99/PowerAutomate/blob/main/MS%20Teams%20App%20Request%20Notification/FormSettings.png?raw=true)


## SharePoint Online List

One list is needed - **MS Teams App Requests**

Custom columns needed:

1. Title (Single line of text)
2. Requestor (Person or Group)
3. AppURL (Hyperlink)
4. BusinessJustification (Multiple lines of text)
5. Status (Choice - choices: New, Review In Progress, Approved, Rejected)

## Power Automate Flow

**MS Team App Request Notification**

This flow triggers anytime a form is filled out. It grabs the form responses and stores these on the MS Teams App Requests SPO list and sends a notification via MS Teams message to let admins know a new request is submitted.

![Flow Part 1](https://github.com/morismm99/PowerAutomate/blob/main/MS%20Teams%20App%20Request%20Notification/FlowPart1.png?raw=true)

![Flow Part 2](https://github.com/morismm99/PowerAutomate/blob/main/MS%20Teams%20App%20Request%20Notification/FlowPart2.png?raw=true)


## MSTeamsAppRequestNotification_20230516162251.zip flow package

1. Go to https://make.powerautomate.com and make sure you are in the environment you want to import the flow to
2. Click My Flows in the left menu
3. Select Import
4. Browse and choose the "MSTeamsAppRequestNotification_20230516162251.zipp" package.
5. Choose create as new
6. Choose MS Forms, SharePoint and MS Teams connections, or create them if these don't already exist
7. Click Import
8. Open the flow when import is complete
9. Update the MS Form ID, SPO Site/List and MS Teams/Channel where the notification will be posted.
10. Save the flow - * *if the import fails, there will be a link that says **Save as new flow** click on that to be able to open it and edit it.* * 

## Update MS Teams Org-wide App settings

Follow these instrutions - [Modify the default setting to receive user requests on your custom webpage](https://learn.microsoft.com/en-us/MicrosoftTeams/user-requests-approve-apps#modify-the-default-setting-to-receive-user-requests-on-your-custom-webpage).

For step 4.b, grab the MS Form collaborate URL/Link and add it there. This is what will re-route end users to fill out your form when trying to request apps to be unblocked in MS Teams.
