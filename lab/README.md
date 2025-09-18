

These instructions are for participants of the **instructor-led** Workshop "LAB583 - Manage AI Capabilities for Copilot+ PCs and Windows 11" at Microsoft Ignite 2025. 

## Lab Overview

In this lab you will gain hands-on experience with enabling and managing AI experiences for Windows. 
You will explore the customizations available to users and the controls available to IT admins. 
You will learn how to use Microsoft Intune to fine-tune popular features like Recall, Copilot, Click to Do, and Image Creator. 
You will also walk through managing privacy and compliance, and end user readiness.


## Pre-Requisites

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

<img src="../../img/Exercise1-Settings-AI Components.png" alt="Agentic search experience in Settings" width="600" />


> Note: On Windows 11 24H2, by default all AI Components are set to a disabled state. On Windows 11 25H2, some AI features are enabled by default: <i>Agentic search experience in Settings, Improved Windows Search, and Click to Do</i>

4. You will see the following AI Components installed locally:
 
<img src="../../img/Exercise1-System-AIComponents.jpg" alt="Installed AI Components" width="600" />

##### Explore Agentic Search Experience in Settings

In the Settings app, you will see the search experience is now AI-enabled through the visual cue next to the magnifier.

<img src="../../img/Exercise1-AgenticSearch-Settings.jpg" alt="Agentic Search in Settings" width="600" />

End users can now search for settings using a natural language query as opposed to needing to know precisely which section in Settings they need to be in, or how the Setting is named. Try the following examples to see the types of natural language searches Settings can now handle.

1. In the search field, type in <b>Add a bluetooth device</b>, allow the search results to populate, and hit Enter.  
2. In the search field, type in <b>change mouse pointer</b>, allow the search results to populate, and hit Enter. 
3. In the search field, type in <b>change time zone</b>, allow the search results to populate, and hit Enter.
4. <b>Close</b> the <b>Settings</b> app

 > Note: On a non-Copilot+ PC Settings app, you would see "No results for *the search you made*" if you attempted these same searches

##### Explore Improved Windows Search

In the Windows Search Bar, you will see the Windows search experience is now AI-enabled through the visual cue next to the magnifier as shown below:

<img src="../../img/Exercise1-ImprovedWindowsSearch.png" alt="Improved Windows Search" width="100" />

Improved Windows Search provides end users with the ability to perform searches that extend beyond just file and folder names. Windows can leverage on-device AI to understand the file contents as well, including image recognition.

INSERT STEPS HERE BASED ON SOME OF OUR SAMPLE PICTURES AND DOCUMENTS (TO BE INCLUDED IN ZIP)


##### Explore Click to Do

Click To Do is a new AI-powered feature that enables users to take contextual actions on anything visible on their screen - text or images - using simple keyboard shortcuts. 

1. Launch the Settings application.
2. In the Search bar, type in "How do I turn on click to do", wait for the results and then hit enter. You will be taken to <b>Privacy & security > Click to Do</b>

<img src="../../img/Exercise1-ClickToDo-Settings.jpg" alt="Click to Do Settings in Privacy and Security" width="600" />

3. As you can see, on Windows 11 25H2, Click to Do is enabled by default, but can be disabled via Intune policy.
4. Launch Click to Do by pressing <b>Windows key + Q</b> together
5. The first time a user launches Click to Do, they are presented with an interactive tutorial.

<img src="../../img/Exercise1-ClickToDo-TutorialStart.jpg" alt="Click to Do Tutorial" width="400" />

6. <b>Complete</b> the Click to Do tutorial
7. Now let's use Click to Do with documents and images on your Copilot+ PC
8. Open <b>File Explorer</b>, navigate to <b>Documents\Click to Do Samples</b>, and launch the sample file "FILE GOES HERE" (Note we can also use the Phi Silica Small but Mighty on Device SLM Blog contents for the file) 
9. Scroll down to the paragraph that starts with "Running the aforementioned stages..." until you have three full paragraphs on the screen.
10. Press Windows Key + Q to start up Click to Do again
11. With Click to Do running, highlight the text in the file. Note the options that appear after you finish highlighting the text. From the menu options, select "Rewrite > Refine." 
13. Observe the output in the Rewrite window. You have the option of copying the rewrite using the Copy in the lower right-hand corner. 

## Discussions

Build your first agent with Azure AI Agent Service is an open source project supported by Microsoft. See the [SUPPORT.md](../SUPPORT.md) file for details on how to raise issues or contribute. If you enjoyed this workshop please give the repository a ⭐ and share it with others.

## Source code

The source code for this session can be found in the [src folder](../src) of this repo.
