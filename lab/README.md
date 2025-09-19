

These instructions are for participants of the **instructor-led** Workshop "LAB583 - Manage AI Capabilities for Copilot+ PCs and Windows 11" at Microsoft Ignite 2025. 

# Lab Overview

In this lab you will gain hands-on experience with enabling and managing AI experiences for Windows. 
You will explore the customizations available to users and the controls available to IT admins. 
You will learn how to use Microsoft Intune to fine-tune popular features like Recall, Copilot, Click to Do, and Image Creator. 
You will also walk through managing privacy and compliance, and end user readiness.


# Pre-Requisites

To participate in this lab, you will need:

1. A Copilot+ PC
2. Lab credentials to log into the Copilot+ PC
3. Access to an Intune tenant
4. This lab will reference files and folders that need to be present on your Copilot+ PC. Log into your Copilot+ PC with your lab credentials and then download the zip file [ZIP FILE NEEDS A LOCATION] and extract it into your Documents folder.

## Exercise One: Meet your Copilot+ PC

<b>Objective</b>: Understand the Copilot+ PC out of box experience

1. Launch the <b>Settings</b> application.
2. Navigate to <b>System</b>
3. Scroll down to <b>AI Components</b> and click on <b>AI Components</b>

<img src="/img/Exercise1-Settings-AI Components.png" alt="Agentic search experience in Settings" width="600" />


> Note: On Windows 11 24H2, by default all AI Components are set to a disabled state. On Windows 11 25H2, some AI features are enabled by default: <i>Agentic search experience in Settings, Improved Windows Search, and Click to Do</i>

4. You will see the following AI Components installed locally:
 
<img src="/img/Exercise1-System-AIComponents.jpg" alt="Installed AI Components" width="600" />

### Explore Agentic Search Experience in Settings

In the Settings app, you will see the search experience is now AI-enabled through the visual cue next to the magnifier.

<img src="/img/Exercise1-AgenticSearch-Settings.jpg" alt="Agentic Search in Settings" width="600" />

End users can now search for settings using a natural language query as opposed to needing to know precisely which section in Settings they need to be in, or how the Setting is named. Try the following examples to see the types of natural language searches Settings can now handle.

1. In the search field, type in <b>Add a bluetooth device</b>, allow the search results to populate, and hit Enter.  
2. In the search field, type in <b>change mouse pointer</b>, allow the search results to populate, and hit Enter. 
3. In the search field, type in <b>change time zone</b>, allow the search results to populate, and hit Enter.
4. <b>Close</b> the <b>Settings</b> app

 > Note: On a non-Copilot+ PC Settings app, you would see "No results for *the search you made*" if you attempted these same searches

### Explore Improved Windows Search

In the Windows Search Bar, you will see the Windows search experience is now AI-enabled through the visual cue next to the magnifier as shown below:

<img src="/img/Exercise1-ImprovedWindowsSearch.png" alt="Improved Windows Search" width="100" />

Improved Windows Search provides end users with the ability to perform searches that extend beyond just file and folder names. Windows can leverage on-device AI to understand the file contents as well, including image recognition.

INSERT STEPS HERE BASED ON SOME OF OUR SAMPLE PICTURES AND DOCUMENTS (TO BE INCLUDED IN ZIP)


### Explore Click to Do

Click To Do is a new AI-powered feature that enables users to take contextual actions on anything visible on their screen - text or images - using simple keyboard shortcuts. 

1. Launch the Settings application.
2. In the Search bar, type in "How do I turn on click to do", wait for the results and then hit enter. You will be taken to <b>Privacy & security > Click to Do</b>

<img src="/img/Exercise1-ClickToDo-Settings.jpg" alt="Click to Do Settings in Privacy and Security" width="600" />

3. As you can see, on Windows 11 25H2, Click to Do is enabled by default, but can be disabled via Intune policy.
4. Launch Click to Do by pressing <b>Windows key + Q</b> together
5. The first time a user launches Click to Do, they are presented with an interactive tutorial.

<img src="/img/Exercise1-ClickToDo-TutorialStart.jpg" alt="Click to Do Tutorial" width="400" />

6. <b>Complete</b> the Click to Do tutorial
7. Now let's use Click to Do with documents and images on your Copilot+ PC
8. Open <b>File Explorer</b>, navigate to <b>Documents\Click to Do Samples</b>, and launch the sample file "FILE GOES HERE" (Note we can also use the Phi Silica Small but Mighty on Device SLM Blog contents for the file) 
9. Scroll down to the paragraph that starts with "Running the aforementioned stages..." until you have three full paragraphs on the screen.
10. Press Windows Key + Q to start up Click to Do again
11. With Click to Do running, highlight the text in the file. Note the options that appear after you finish highlighting the text. From the menu options, select "Rewrite > Refine." 
13. Observe the output in the Rewrite window. You have the option of copying the rewrite using the Copy in the lower right-hand corner. 

### Enable Recall

Windows Recall is a Copilot+ PC exclusive that provides a running "memory" for the end user of things they have done on their device. Using Recall, a user can quickly search for information that they had seen in an app, web site, or document.

By default, Windows Recall is not enabled. 

1. From the Start Menu, type in <b>Recall</b> and launch it
2. When Recall first starts, a tutorial will appear.

<img src="/img/Exercise1-RecallFirstTimeUse.jpg" alt="Recall First Time Tutorial" width="600" />

3. Proceed through the wizard, and on the last page you will be prompted to save Snapshots. Select <b>"Yes, save"</b>. You must next authenticate with Windows Hello to complete turning on Recall.
4. Recall has multiple settings available in the Privacy & Security node of the Settings app. After selecting <b>"Yes, save"</b> you should be redirected to the <b>Privacy & Security > Recall & snapshots</b> page. If you are not redirect, open <b>Settings</b> and navigate to <b>Privacy & Security</b> and then under the section titled <i>Windows permissions</i> select <b>Recall & snapshots</b>.

<img src="/img/Exercise1-Recall-Settings.jpg" alt="Recall Settings Page" width="600" />

> When there are no MDM policies applied to the device, the end user will have control over items such as how much storage can be used for Recall's snapshots, how long snapshots should persist before auto-deletion, as well as the option to delete snapshots at any time. 
There are user controls (and Admin controls that you will explore later) to manage sensitive information types, apps to be added or removed from Recall and websites to be added or removed from snapshots.

5. Scroll down to the <b>Advanced Settings</b> option and select <b>Advanced Settings</b>.

<img src="/img/Exercise1-Recall-AdvancedSettings.jpg" alt="Recall Advanced Settings Page" width="600" />

* Note that users can now Reset Recall through a single button. If we were in the European Economic Area, there would also be an option for the end user to export Recall data.
* When running, Recall will appear in the lower-right corner of the task bar.
* To ensure that some snapshots have been taken, <b>navigate</b> through the <b>Settings</b> app onto a few screens, launch <b>Notepad</b> and <b>type</b> in a short phrase and then close Notepad, or perform some other actions on the device.

<img src="/img/Exercise1-Recall-Icon-TaskBar.jpg" alt="Recall Taskbar Icon" width="200" />

6. Click on the Recall icon to open it.
7. Recall now opens to a "Home" view that shows most frequently accessed applications and websites. We are just starting this lab, so you will not have many snapshots to look through.
8. Recall also supports a Timeline view. Click the <b>Timeline</b> button just below the Home button on the left hand side of Recall.

<img src="/img/Exercise1-Recall-HomePage-Timeline.jpg" alt="Recall Home and Timeline Options" width="600" />

12. Users can move back and forth through their timeline using the slider at the bottom of the screen, or the arrow icons at the bottom of the screen. They can also explore snapshots individually with forward/backward arrows that appear on the screen next to each snapshot, or use the arrow keys on the keyboard.
13. Users can also Search their Recall history using the Search bar at the top. Search includes both text (through Optical Character Recognition) as well as images.
14. Each snapshot is enabled with Click to Do by default. You can highlight text or images in a snapshot and use Click to Do to perform actions against it.
15. <b>Navigate</b> to any snapshot in your Recall timeline. 
16. In the right corner above the snapshot you will see a set of icons. 
    1.  The first icon is to toggle Click to Do on or off within Recall.
    2.  The second icon is to perform a copy of the contents on the snapshot
    3.  The third icon is to delete - either delete all snapshots related to the app/page that is in the snapshot or delete just this specific snapshot
    4.  Finally, a "..." option is available to edit the image in Snipping Tool
17. Select the delete icon and select Delete snapshot. You will receive a confirmation message first, and then click Delete. Once deleted, snapshots <i>cannot be recovered</i> by any means.

<img src="/img/Exercise1-Recall-DeleteSnapshot.jpg" alt="Recall Delete Snapshot Option" width="200" />

18. Close the Recall window. The Recall icon should persist in the task bar. If you click on it, you can see you have the option to Pause snapshots. Leave Recall running for now, as you will be able to use your snapshot history later in this lab to search for actions you have performed.

## Exercise Two: Configure AI Policies in Intune

<b>Objective</b>: Gain hands on experience configuring commercial controls for Copilot+ PC AI Features

NOTE TO SELF - MAKE SURE USERS HAVE ACCESS TO INTUNE. ALSO MAY NEED TO REVISE THE POLICY INSTRUCTIONS AS MORE THINGS MOVE INTO SETTINGS CATALOG IN OCT/NOV

* Launch the Edge browser
* Navigate to intune.microsoft.com
* Authenticate with your lab credentials
* When creating policies, name your policies <i>lastname_firstname</i>_PolicyName to distinguish from other attendees

IF THIS IS A SHARED M365 TENANT, BE SURE TO EXPLAIN USERS SHOULD CREATE INDIVIDUAL POLICIES BUT WILL NOT BE ASSIGNING POLICIES

### Create Recall and Click to Do Policy using the Settings Catalog

Objective: Build an Intune policy that enables the use of Recall, but block capturing snapshots from your Contoso internal employee sites and two different customer relationship applications that contain customer data. You need to limit the snapshot storage space to 10 GB on devices, and set a limit of XX days to retain snapshots. You need to enable your European Economic Area (EEA) users to be able to export their snapshot data. 

1. Before you start with creating your Intune policy, you will need to create two separate text files in order to provide a block list for apps and a block list for websites (URIs).
2. Launch <b>Notepad</b>
3. Type or copy the following into your text file

     `https://employee.contoso.com`
     <br>
     `https://benefits.contoso.com`

4. <b>Save</b> the file to your <i>Documents</i> folder as <b>DenyUriListForRecall.csv</b> (change the <i>save as type</i> to all files first)
5. Create a new blank text file in Notepad
6. <b>Type</b> or <b>copy</b> the following into the new, blank text file

     `ContosoCRM.exe`
     <br>
     `HappyCustomers.exe`

7. <b>Save</b> the file to your <i>Documents</i> folder as <b>DenyAppListForRecall.csv</b> (change the <i>save as type</i> to all files first)
8. After both text files have been saved, you may close Notepad. Return to the Edge browser session with the Intune console.
9. In the Intune console, navigate to <i>Devices</i>. Under <i>Manage devices</i>, select <b>Configuration</b>
10. Select <b>Create > New Policy</b>
   1. Platform: <b>Windows 10 and later</b>
   2. Profile type: <b>Settings catalog</b>
   3. Click <b>Create</b>
11. The Create profile wizard starts
12. On the <i>Basics</i> page, enter the following information
   1. Name: <i>lastname_firstname</i><b>_Enable Copilot+ PC AI Features</b>
   2. Description: <b>Enable AI features</b>
   3. Click <b>Next</b>
13. On the <i>Configuration settings</i> page, click the <b>+Add settings</b> option to open the Settings picker
   1. In the <i>Browse by category</i> list, scroll down to <b>Windows AI</b> and click <b>Windows AI</b>
   2. The Windows AI settings appear. <b>Select</b> the following settings:
      1. Allow Recall Enablement
      2. Allow Recall Export (Windows Insiders only)
      3. Disable AI Data Analysis
      4. Disable Click To Do (User)
      5. Set Deny App List For Recall
      6. Set Deny Uri List For Recall
      7. Set Maximum Storage Duration For Recall Snapshots
      8. Set Maximum Storage Space for Recall Snapshots
      9. You may now close the settings picker.
   3. The selected settings will appear in the left side of your Configuration Settings screen. You will now configure the settings as follows to meet your policy objectives.
      1. Set Maximum Storage Space for Recall Snapshots: Use the drop-down menu to select <b>10 GB</b>
      2. Set Maximum Storage Duration for Recall Snapshots: Use the drop-down menu to select <b>60 days</b>
      3. At the Set Deny Uri List for Recall setting, click the Import button, <b>de-select</b> the "My data has headers" option, and then browse to the DenyUriListForRecall.csv file you created and saved earlier. Click <b>"Select"</b> to complete the import of the file. <br> <img src="/img/Exercise2-SetDenyUriListForRecall.jpg" alt="Uri Deny List Settings Imported" width="600" /><br>
      1. At the Set Deny App List for Recall setting, click the Import button, <b>de-select</b> the "My data has headers" option, and then browse to the DenyAppListForRecall.csv file you created and saved earlier. Click <b>"Select"</b> to complete the import of the file. <br> <img src="/img/Exercise2-SetDenyAppListForRecall.jpg" alt="App Deny List Settings Imported" width="600" /><br>
      2. Set the Disable Click to Do (User) setting to "Click to Do is enabled" if it is not already set to this value
      3. Set the Disable AI Data Anlysis slider to "Enable Saving Snapshots for Windows" if it is not already set to this value.
      4. Set the Allow Recall Enablement setting to "Recall is available" if it is not already set to this value.
      5. Click <b>Next</b> to proceed in the Create profile wizard
1.  On the Scope tags page, leave the defaults and click <b>Next</b>
2.  On the Assignments page, leave the defaults (no groups selected) and click <b>Next</b>
3.  On the Review + create page, validate the configuration settings and then click <b>Create</b>

You did not necessarily need to use a text file to import the Uris and Apps, as you could simply enter them into the policy one row at a time. However, entering manually could be tedious if there are hundreds of entries. Knowing how to build the input files is critical for long-term maintenace in a complex environment.

You also could disable Recall, Snapshots and Click to Do with these settings. If your organization needs to disable these features (until they are approved by leadership) you would use the Allow Recall Enablement, Disable Click To Do, and Disable AI Data Analysis settings to disable the features. Once disabled, an end user will be unable to enable or use these features.

### Create AI Policy using Custom OMA-URI

Not all AI policy settings are available in the Settings catalog (yet). There are settings that govern AI image capabilities and the use of the search agent in the Settings app. In this part of the lab you will construct a custom MDM policy that enables these features.

1. In the Intune console, navigate to <i>Devices</i>. Under <i>Manage devices</i>, select <b>Configuration</b>
2. Select <b>Create > New Policy</b>
   1. Platform: <b>Windows 10 and later</b>
   2. Profile type: <b>Templates</b>
   3. The <i>Template name</i> list will appear. 
   4. Select the option <b>Custom</b>
   5. Click <b>Create</b> to start the policy creation wizard
3. On the <i>Basics</i> page, enter the following information
   1. Name: <i>lastname_firstname</i><b>_Enable Image and Settings Agent Copilot+ PC</b>
   2. Description: <b>Enable AI features that are not present in the Settings catalog</b>
   3. Click <b>Next</b>
4. On the Configuration Settings page, click <b>Add</b> 
