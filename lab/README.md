# Introduction

Welcome to the **Ignite 2025 Hands-on Lab: Manage AI Capabilities for Copilot+ PCs and Windows 11**.

This lab is designed to give you practical experience with the latest AI-powered features in Windows 11 and Copilot+ PCs. 

By the end of this session, you will:

* Understand the AI components available on Copilot+ PCs.
* Explore features like **Click to Do**, **Live Captions with Translation**, and **Windows Studio Effects**.
* Learn how to configure and manage these features using **Microsoft Intune** policies.
* Gain insights into integrating AI tools for productivity and accessibility.

### What You'll Need
- A Copilot+ PC with Windows 11 25H2.
- Files used for various exercises already extracted to <b>C:\LAB583</b>
- Credentials for the lab environment (see the resource tab above).
- An M365 Copilot license for certain exercises.
- Access to a test Intune tenant for policy configuration.

> **Tip:** This lab combines local AI experiences with enterprise management scenarios. Follow each exercise step-by-step for the best experience.

Let's get started!

 
# Exercise One: Meet your Copilot+ PC

<b>Objective</b>: Understand the default Windows-enabled AI features on your Copilot+ PC and the components that are installed.

>Note: On Windows 11 24H2, by default all AI Components are set to a disabled state. On Windows 11 25H2, some AI features are enabled by default: <i>Agentic search experience in Settings, Improved Windows Search, and Click to Do</i>

1. Launch the <b>Settings</b> application.
2. Navigate to <b>System</b>
3. Scroll down to <b>AI Components</b> and click on <b>AI Components</b> 

![Settings AI Components](https://github.com/microsoft/ignite25-LAB583-manage-ai-capabilities-for-copilot--pcs-and-windows-11/blob/main/Exercise1-Settings-AI%20Components.png)


4. You will see the following AI Components installed locally:

![Installed AI Components](https://github.com/microsoft/ignite25-LAB583-manage-ai-capabilities-for-copilot--pcs-and-windows-11/blob/main/Exercise1-System-AIComponents.jpg)

As more AI features are enabled on your Copilot+ PC, additional AI components may be installed and will appear in this section of the Settings app. 

Leave the Settings app open for the next Exercise.

 
# Exercise Two: Explore Agentic Search Experience in Settings

<b>Objective</b>: Use natural language to quickly find the setting you are looking for in the Windows 11 Settings app.

At the top of the Settings app, you will see the search experience is now AI-enabled through the visual cue next to the magnifier.

![Agentic Search in Settings](https://github.com/microsoft/ignite25-LAB583-manage-ai-capabilities-for-copilot--pcs-and-windows-11/blob/main/Exercise1-AgenticSearch-Settings.jpg)

End users can now search for settings using a natural language query as opposed to needing to know precisely which section in Settings they need to be in, or how the Setting is named. The following steps illustrate the types of natural language searches Settings can now handle.

1. In the Settings search box, type in +++Add a bluetooth device+++, allow the search results to populate, and press <b>Enter</b>. Notice that you are brought to the right Settings page to pair devices with bluetooth.
2. In the Settings search box, type in +++change mouse pointer+++, allow the search results to populate, and press <b>Enter</b>. Again, you are brought to the right Settings page to adjust the mouse pointer and other mouse settings.
3. In the Settings search box, type in +++change time zone+++, allow the search results to populate, and press <b>Enter</b>. You should be at the Settings page to change your system's time zone.

>Note: On a non-Copilot+ PC Settings app, you would see "No results for *the search you made*" if you attempted these same searches

4. <b>Close</b> the <b>Settings</b> app
 
# Exercise Three: Explore Click to Do feature in Windows

<b>Objective</b>: Gain hands-on experience with Click to Do

Click To Do is a Copilot+ PC feature that enables users to take contextual actions on anything visible on their screen - text or images - using simple keyboard shortcuts. There are three ways to launch Click to Do and each portion of this exercise will use a different method so you gain familiarity with each option.

### Launch Click to Do

1. Launch the <b>Settings</b> application.
2. In the Settings Search box, type in +++How do I turn on click to do+++, wait for the results and then press <b>Enter</b>. You will be taken to the <b>Privacy & security > Click to Do</b> settings page. 

![Click to Do in Settings](https://github.com/microsoft/ignite25-LAB583-manage-ai-capabilities-for-copilot--pcs-and-windows-11/blob/main/Exercise1-ClickToDo-Settings.jpg)

3. As you can see, on Windows 11 25H2, Click to Do is enabled by default. However, it can be disabled via Intune policy (you will learn how in Exercise Seven).
4. Launch Click to Do by pressing <b>Windows key + Q</b> together
5. The first time a user launches Click to Do, they are presented with an interactive tutorial.

![Click to Do Tutorial Start](https://github.com/microsoft/ignite25-LAB583-manage-ai-capabilities-for-copilot--pcs-and-windows-11/blob/main/Exercise1-ClickToDo-TutorialStart.jpg)

6. <b>Complete</b> the Click to Do tutorial

>Note: There are two additional methods to launch Click to Do: Swipe in from the right-side of the screen, or use <b>Windows key + left mouse click</b>

### Using Click to Do with Documents

Click to Do offers integrated AI text generation functions like rewrite and summarize without having to first copy the content into M365 Copilot or other prompt-based generative AI. In this part of the exercise you will use Click to Do with a PDF based off of our Phi Silica blog to rewrite several paragraphs and copy the content into Notepad.

1. Open <b>File Explorer</b>, navigate to <b>C:\LAB583\Exercise3-ClickToDo</b>, and <b>double-click</b> the file <b>PHI-SILICA-BLOG.pdf</b>
2. Scroll down the PDF until you reach the paragraph that begins with "<i>Running the aforementioned stages</i>" and position the text so that you see 3 or more paragraphs of information as shown in the image below.

!IMAGE[Exercise3-PhiSilica.png](instructions310362/Exercise3-PhiSilica.png){500}

3. Press <b>Windows Key + left mouse click</b> to launch <b>Click to Do</b>
4. With Click to Do running, <b>hover over</b> the text in the file.
5. <b>Right-click</b> in the highlighted area to expose menu options

!IMAGE[Exercise3-ClickToDoMenuOptionsText.png](instructions310362/Exercise3-ClickToDoMenuOptionsText.png){500}

6. From the menu options, select <b>Rewrite > Refine</b>
7. Observe the output in the Rewrite window. Click the <b>Copy</b> button in the lower-right corner to copy the text to the clipboard.

!IMAGE[Exercise3-ClicktoDoRewrite.png](instructions310362/Exercise3-ClicktoDoRewrite.png){300}

8. Press <b>Esc</b> to close Click to Do
9. Launch <b>Notepad</b>
10. If a first-time wizard starts, complete the wizard before proceeding.
11. <b>Paste</b> in the rewritten text. 
12. You could use this rewritten content as a starting point for your own document, email, or presentation. 

### Using Click to Do with Optical Character Recognition

Click to Do provides a quick way to capture the text in an image. In this part of the exercise you are playing the role of a service desk administrator who is assisting the user with network connectivity issues. The user has shared their Settings app via a Teams meeting (simulated here with a PNG file) and you want to quickly extract the MAC address from the screenshare without typing it by hand.

1. Open <b>File Explorer</b>, navigate to <b>C:\LAB583\Exercise3-ClickToDo</b>, and <b>double-click</b> the file <b>Wi-Fi_Info.png</b>
2. With the image open, swipe in from the right-side of the screen to launch <b>Click to Do</b>
3. Once Click to Do highlights the screen, <b>left-click and drag your mouse</b> over the MAC address. 
4. The Click to Do text options appear when you finish highlighting.
5. Select <b>Copy</b> to copy the MAC address to the clipboard.

!IMAGE[Exercise3-CopyMACAddress.png](instructions310362/Exercise3-CopyMACAddress.png){500}

6. Switch to <b>Notepad</b>.
7. Create a new blank file.
8. <b>Paste</b> in the MAC address.
9. In your environment, you could easily paste this information into a ticket for a technician, or into a tool that allows you to quickly look up MAC addresses for network authorization.

### Using Click to Do with Images

1. Open <b>File Explorer</b>, navigate to <b>C:\LAB583\Exercise3-ClickToDo</b>, and <b>double-click</b> the file <b>RecallExample.png</b>
2. This sample image has separate, distinct images within it. Suppose you wanted to just copy out the second image that appears in the top row (outlined in the screenshot below)

!IMAGE[Exercise3-PickAnImage.png](instructions310362/Exercise3-PickAnImage.png){500}

3. Without Click to Do, you could open Snipping Tool, take a snip of it, and then copy it or save the file. Let's see how Click to Do could save you a few steps.
4. <b>Launch Click to Do</b> (your preference: <b>Windows + Q</b>, <u>or</u> <b>Windows + Left Mouse Click</b>, <u>or</u> <b>swipe in from the right</b>)
5. <b>Hover</b> over the <i>second image</i> and then <b>left-click</b> <u>or</u> <b>right-click</b> with your mouse and the options menu will appear. Select <b>Copy</b>

!IMAGE[Exercise3-CopyImage.png](instructions310362/Exercise3-CopyImage.png){300}

6. Open <b>Word</b>
7. Use <b>Ctrl + V</b> to paste the image into Word  

!IMAGE[Exercise3-PasteImageIntoWord.png](instructions310362/Exercise3-PasteImageIntoWord.png){300}

8. You could have pasted the image into PowerPoint, or into a help desk ticket, or any other application that accepts image input.
9. <b>Close</b> Word without saving the file.


===
# Exercise Four: Explore AI Features in Notepad

<b>Objective</b>: Gain hands-on experience with the built-in AI capabilities in Notepad

>[!NOTE]The AI features in Notepad require an <b>M365 Copilot license</b> to be assigned to an Entra ID account.


1. Notepad now has AI-enabled features that are <b>not</b> unique to Copilot+ PCs. You can run these features on a "regular" Windows 11 PC. This is because the Notepad AI will use the local CPU as opposed to an NPU.
2. Launch <b>Task Manager</b>
3. Move the <b>Task Manager</b> window to one side of the desktop.
4. In <b>Task Manager</b>, in the left-hand menu, <b>click</b> the icon for <b>Performance</b> as shown in the image below.

!IMAGE[Exercise1-TaskManagerPerformance.jpg](instructions310362/Exercise1-TaskManagerPerformance.jpg){600}

5. Launch <b>Notepad</b>.
6. <b>Sign into</b> Notepad with the M365 Copilot licensed Entra ID account provided to you. The sign-in is in the upper right corner of Notepad's menu bar.
7. <b>Move</b> the Notepad window to the other side of your desktop so you can see Task Manager and Notepad side by side.
8. Notepad should open to an empty canvas named "Untitled." If it doesn't, click the "+" button in the top menu to create a new empty file.

!IMAGE[Exercise1-NotepadFirstLaunch.jpg](instructions310362/Exercise1-NotepadFirstLaunch.jpg){400}

9. In the upper-right corner of Notepad you will see an AI drop-down menu with a Copilot icon. 
10. If a first-time wizard starts, complete the wizard before proceeding.
11. <b>Click</b> on the AI drop-down menu, and the first (and only available) option is <b>Write</b>. A Notepad file requires text in it to unlock the additional menu options.

!IMAGE[Exercise1-NotepadCopilotMenu.jpg](instructions310362/Exercise1-NotepadCopilotMenu.jpg){200}

12. From the AI drop-down menu, select the <b>Write</b> option. If this is the first time launching the option, you will see a tutorial that explains that you will write a prompt and AI will generate a draft in Notepad. Complete the wizard before proceeding.
13. In the Write prompt that appears,type or copy in +++Create a draft blog post about things to see and do in San Francisco.+++ and then submit the prompt.
14. Watch the changes in Task Manager - you should not see any additional NPU utilization as Notepad AI will leverage the CPU to generate its content.

!IMAGE[Exercise5-NoNPUUtilization.png](instructions310362/Exercise5-NoNPUUtilization.png){500}

15. Select <b>Keep Text</b> when the draft is complete.
16. Now that the text is in Notepad, you can highlight a paragraph and then using the AI menu, select "<b>Make Longer</b>" to build upon the paragraph. You will get a result, and you can either choose to replace the original text with the new text or discard it. You can also adjust the tone as well as the format. Notice the NPU utilization does not change when rewriting or using other AI options within Notepad.
17. <b>Select</b> the <b>entire text</b> in Notepad and from the AI menu, select <b>Change Tone > Casual</b> and compare the new text to the old text. 
18. <b>Close</b> Notepad and Task Manager

>[!NOTE]In Exercise Nine you will create an Intune policy to manage the use of AI features in Notepad. 

===
# Exercise Five: Explore AI Features in Paint

<b>Objective</b>: The AI Features in Paint are intended to assist end users in generating creative images using natural language prompts. In this Exercise you will discover some of the features available and learn how to use them to build fun images with minimal effort.

>[!NOTE]The AI features in Paint require an <b>M365 Copilot license</b> to be assigned to an Entra ID account.

1. From the Start menu, launch <b>Paint</b>
2. <b>Sign into</b> Paint with the M365 Copilot licensed Entra ID account provided to you. The sign-in is in the upper right corner of Paint's menu bar
3. In the Paint menu bar, locate the <b>Copilot</b> option and open it to see the available options

!IMAGE[Exercise7-Copilot-in-Paint.jpg](instructions310362/Exercise7-Copilot-in-Paint.jpg){700}

4. The first setting you will try is the <i>Image Creator</i>. Image creator uses natural language prompts to generate a picture. Select <b>Image Creator</b> from the Copilot menu inside of Paint.

!IMAGE[Exercise7-CreateImage.png](instructions310362/Exercise7-CreateImage.png){300}

5. The <i>Image Creator</i> wizard will start with a short explanation of the feature.

!IMAGE[Exercise7-ImageCreatorWizardStart.png](instructions310362/Exercise7-ImageCreatorWizardStart.png){300}

6. <b>Complete</b> the wizard
7. In the right-hand pane of Paint, the <i>Image Creator</i> is available for you to add information to. For this first exercise, let's use the simple prompt +++a bridge crossing water at sunset+++. You can then choose a style using the drop-down selector. Pick Oil Painting (or any option you prefer)

!IMAGE[Exercise7-Suggestion-With-Format.png](instructions310362/Exercise7-Suggestion-With-Format.png){300}

8. At the bottom of the Image Creator pane, click <b>Create</b>

!IMAGE[Exercise7-CreateButton.png](instructions310362/Exercise7-CreateButton.png){100}

9. Copilot will build three variant images based off of your prompt.

!IMAGE[Exercise7-ThreeGeneratedVariants.png](instructions310362/Exercise7-ThreeGeneratedVariants.png){300}

10. <b>Click</b> on a variant image that you like. This will place it into the Paint canvas where you can continue to make markups or just copy it into another application like Word or PowerPoint.
11. If you prefer a different art style, use the style drop-down to choose an alternate type of image (for instance, Watercolor). Select a differrent style than your original choice and click <b>Create</b> to create three new images based on the new style.
12. In the Paint canvas, use <b>Ctrl+A</b> to select everything and then click the <b>Delete</b> key to start over with a blank page.
13. In the Copilot menu, select Cocreator to launch the Cocreator option

!IMAGE[Exercise7-LaunchCoCreator.png](instructions310362/Exercise7-LaunchCoCreator.png){300}

14. Cocreator differs from the Image Creator in that you and Copilot are working together to create your image. Let's suppose you tried a few prompts with Image Creator but the image layout is not what you are looking for. You can use Cocreator so you can start to sketch how you want objects positioned in the picture and the drawing is generated based on your guidance.
15. In the Cocreator pane, type in +++a bridge at sunset+++, and then in the Paint canvas, begin to sketch out a bridge crossing water at sunset and watch the image get built in the Cocreator pane.

!IMAGE[Exercise7-UsingCocreator.png](instructions310362/Exercise7-UsingCocreator.png){300}

16. The image below is an example where a rudimentary sketch was built in the canvas. Cocreator simultaneously built an image from both the natural language prompt and what was sketched by the end user.

!IMAGE[Exercise7-SketchingBridge.png](instructions310362/Exercise7-SketchingBridge.png)

17. <i>Experiment</i> with your own prompt and sketch to see how Cocreator can help enhance your drawing. You also have additional controls over the Cocreator including the following:
    1. Adjust the creativity slider to allow Cocreator to stick closer to your original sketch or embellish it greatly.
    2. Use the style drop-down (it defaults to "No Selection") to change the art style.
    3. You can also have it "Try again" if you want to generate a brand new result.
    4. Click the <b>+ Apply</b> button to apply your drawing to the canvas.
18. While there are several other AI features in Paint, we are going to conclude this exercise with the <i>Sticker Generator</i>. 
19. Clear the canvas by using <b>Ctrl+A</b> and then press <b>Delete</b>
20. Under the Copilot menu, select <b>Sticker Generator</b>
21. In the Sticker Generator prompt, type or paste in +++a cat typing at a computer+++ and then click <b>Generate</b>

    > <i>If you prefer dogs, type in </i>+++a dog typing at a computer+++ <i>(or, for something completely different, try</i> +++a sea otter typing at a computer+++)

22. Clicking on one of the generated stickers will place it onto the canvas. This allows you to start with a base image on the canvas, but then generate individual stickers to overlay.
23. Putting it all together, try the following starting with a blank canvas in Paint:
    1. In Image Creator, use the prompt +++Draw a home office with a desk, a chair, bookshelves, a window, and a houseplant+++
    
    !IMAGE[Exercise7-Combo.png](instructions310362/Exercise7-Combo.png)

    2. <b>Generate</b> the image in an <i>Anime</i> style
    3. Select one of the variants, or generate again to build a new set of options. Once you have a picture you like, add it to your canvas.
    4. In the <i>Sticker Generator</i>, use the prompt +++a cat with large eyes sitting on a cat bed+++ and then select one of the results to paste into your canvas. 
    5. <b>Resize</b> the sticker (note it has a transparent background for easy overlay).
    
    !IMAGE[Exercise7-Combo2.png](instructions310362/Exercise7-Combo2.png)

24.When finished, <b>Close</b> Paint without saving your file(s). 

>[!NOTE]In Exercise Eight you will create an Intune policy to manage the use of AI features in Paint.

===
# Exercise Six: Explore AI Features in Photos

<b>Objective</b>: The AI Features in Photos are intended to assist end users in making edits to Photos without requiring additional software. In this lab you will gain hands on experience with several of these features without requiring formal training or third-party photo editing software.


1. To begin, you will need to open a Photo into the Photos app in order to take advantage of the AI features.
2. In File Explorer, <b>navigate</b> to <b>C:\LAB583\Exercise6-Photos</b>, <b>right-click PontiacGTO.jpg</b> and select <b>Open</b>. By default the picture will open in Photos.
    1. If prompted with "All your photos in one place" dialog, just click <b>Go to Photos</b> 
    2. If prompted with "Allow image categorization" dialog, select <b>Allow</b> 
3. After the photo is opened, in the <u>upper-left corner</u> of the Photos app, you will see an <b>Edit</b> button.

!IMAGE[Exercise8-OpenPhoto.png](instructions310362/Exercise8-OpenPhoto.png){500}

4. Click the <b>Edit</b> button to enter the editing mode.
5. Once in editing mode, AI features will be available in the top menu.

!IMAGE[Exercise8-AIMenuOptions.png](instructions310362/Exercise8-AIMenuOptions.png){500}

6. From left-to-right the AI features are as follows:
    1. <b>Erase</b>. This provides the ability to perform a generative erase of items from the picture. You can adjust the brush size to provide more fidelity of control. This feature works best with removing something small and distinct from the image. You will gain some erasing experience when exploring the Background option in the next step.
    2. <b>Background</b>. This feature will either blur, remove or replace the background. 
        1. Let's begin by removing the background. Select the <b>Remove</b> option in the middle of the available options.
        
        !IMAGE[Exercise8-BackgroundRemoval.png](instructions310362/Exercise8-BackgroundRemoval.png)

        2. You will see the background <i>mostly</i> get removed. There may still be some background artifacts in the image due to the complexity of this image.
        3. Enable the Background brush tool by <b>changing</b> the slider from "off" to "<b>on</b>".
        
        !IMAGE[Exercise8-BackgroundBrushEnabled.png](instructions310362/Exercise8-BackgroundBrushEnabled.png)

        4. The image now shows where the "background" has been identified through a set of diagonal lines. You can now use the brush tool to erase the remaining elements. Simply <b>hover</b> over the areas to remove, click the <b>left mouse button</b> and then <b>drag</b> the brush over the areas to erase.
        5. <b>Toggle</b> the brush tool <b>off</b> to see if you missed any areas. <b>Toggle</b> back <b>on</b> to continue removing until complete. Your image will likely look like the image below.
        
        !IMAGE[Exercise8-BackgroundRemoved.png](instructions310362/Exercise8-BackgroundRemoved.png)

        6. Click the <b>Replace</b> option to replace the background with a solid color. Change the color using the slider and click the color to the right of the slider to replace the background entirely with a solid color. In the image below, a solid brown background has been applied to the photo.
        
        !IMAGE[Exercise8-Replacebackground2.png](instructions310362/Exercise8-Replacebackground2.png)

        7. Click the <b>Reset background</b> button to restore the image to its original background.
    3. <b>Restyle image</b>. This feature requires the use of an MSA (Microsoft Account) because the resulting photo is processed through Microsoft's AI safety and security filters in a data center. Due to limitations in this lab environment, you will not be able to gain hands on experience with this feature. <b>Do not sign-in with your MSA!</b>
    
    !IMAGE[Exercise8-RestyleImage.png](instructions310362/Exercise8-RestyleImage.png){200}

    4. <b>Super resolution</b>. This feature uses AI to upscale a low resolution picture to a higher resolution. 
        1. To use <b>Super resolution</b> you will need to start with a lower resolution picture that the photo of the automobile. 
        2. In File Explorer, navigate to <b>C:\LAB583\Exercise6-Photos</b>, <b>right-click Farm_LowRes.jpg</b> and select <b>Open</b>
        3. <b>Click</b> on the Super resolution icon to launch the feature. 
        4. Provided this lab machine was reset between lab sessions, the AI model for this feature will not be available by default. As mentioned at the beginning of this lab, AI components are installed when features are enabled. The Super resolution feature in Photos is one example of this. If you are prompted with the dialog below, click <b>Download</b> to download the model.
        
        !IMAGE[Exercise8-DownloadAIModelSuperResolution.png](instructions310362/Exercise8-DownloadAIModelSuperResolution.png){300} 

        5. If you were prompted to install this component, you can confirm this by opening <b>Settings</b>, navigating to <b>System</b> and then selecting <b>AI Components</b>. You will see the AI component <b>AI Image Processing</b> installed.
        
        !IMAGE[Exercise8-NewAIComponentInstalled.png](instructions310362/Exercise8-NewAIComponentInstalled.png){600} 

        6. <b>Close</b> the Settings app and return to Photos.
        7. In the right-hand Super resolution menu, you can adjust the picture scale from 240x320 to a higher resolution. Adjust the slider to 1920 x 2560 and then the image will get upscaled.
        
        !IMAGE[Exercise8-AdjustScaleSlider.png](instructions310362/Exercise8-AdjustScaleSlider.png){400}

        8. The Super resolution feature will place a vertical bar in the middle of the picture. Moving the bar to the right shows the original image, moving it to the left will show the enhanced image. 
        9. Click the <b>Cancel</b> button in the upper-right corner to not save the upscale changes.
        
        !IMAGE[Exercise8-CancelButton.png](instructions310362/Exercise8-CancelButton.png){400}

        10. Confirm that you don't want to save changes.
        11. <b>Close</b> the file Farm_LowRes.jpg
    5. <b>Relight</b>. This feature will adjust the lighting in the picture. Return to the C:\LAB583\Exercise6-Photos\PontiacGTO.jpg photo that you were using previously.
        1. <b>Click</b> the Relight icon to launch the feature.
        2. The Relight menu will appear in the right-hand side of the Photo editor.
        
        !IMAGE[Exercise8-RelightEnabled.png](instructions310362/Exercise8-RelightEnabled.png)

        3. By default, light locations are enabled. Light locations show up as circled 1, 2, and 3 icons on your photo. Arrows indicate the direction the light is shining from that location. All three lights point to a single circle (currently in the middle of the photo). At the bottom of the Relight menu you will see options for disabling light 1, light 2 and light 3, as well as an option for enabling ambient light.
        4. There are six preset lighting options (Original, Softbox, Classic Portrait, Dynamic, Golden Hour, and Cyberpunk). Choose each preset to observe how the picture is adjusted based on the lighting changes. When done, return to the <b>Softbox</b> preset option.
        5. Move the light sources 1, 2, and 3 to the top of the picture and then move the focus point of the light to near the bottom of the picture and notice how AI will generate shadows based on where the light is not striking.
        
        !IMAGE[Exercise8-LightingAdjusted.png](instructions310362/Exercise8-LightingAdjusted.png)

        6. Notice that with this lighting arrangement the top of the car gets very bright. <b>Expand</b> the drop down next to the option for light 2 and reduce the intensity to <b>-1</b>. 
        
        !IMAGE[Exercise8-AdjustLight2.png](instructions310362/Exercise8-AdjustLight2.png){300}

        7. The photo changes to reduce the glare from the top and produce more dramatic shadows.
        
        !IMAGE[Exercise8-AdjustedLight2.png](instructions310362/Exercise8-AdjustedLight2.png)

        8. The lighting sources can also have a color tint to them. <b>Expand</b> light number three with the drop down, change the color to Hex <b>409c2d</b> (RGB 64, 156, 45). Increase the brightness to <b>50</b>. Light source 3 now has a color ring that matches the color value you set (Hex 409c2d). The entire photo now has a substantial green tint to it. It's probably not the most beautiful photograph, but it shows how you can quickly and easily adjust the lighting, tone, and color of a photograph.
        
        !IMAGE[Exercise8-GreenCar.png](instructions310362/Exercise8-GreenCar.png)
        
7. This completes the exploration of the AI features available in the Photos app. <b>Close</b> the Photos app before proceeding to the next Exercise.


===
# Exercise Seven: Build a Settings Catalog AI Policy in Intune

<b>Objective</b>: Gain hands on experience configuring MDM policies for Copilot+ PC AI Features. 

In this exercise, you will build an Intune policy that enables the use of Recall, but block capturing snapshots from your Contoso internal employee sites and two different customer relationship applications that contain customer data. 

You need to limit the snapshot storage space to 10 GB on devices, and set a limit of 60 days to retain snapshots. 

You need to enable your European Economic Area (EEA) users to be able to export their snapshot data. 

You also want to make sure your users have access to Click to Do both inside and outside of Recall.


Before starting, perform the following steps to access your Intune tenant:

* Launch the Edge browser
* Navigate to intune.microsoft.com
* Authenticate with the Entra account provided to you as part of this lab.
* <b>IMPORTANT</b>: When creating policies, please name your policies <i>lastname_firstname</i>_PolicyName to distinguish from other attendees

### Create Recall and Click to Do Policy Using the Settings Catalog

1. Before you start creating your Intune policy, you will create two separate text files to provide a block list for apps and a block list for websites (URIs).
2. Launch <b>Notepad</b> and start with a blank text file
3. Type or copy the following two lines into your new, blank text file

     +++https://employee.contoso.com+++

     +++https://benefits.contoso.com+++

4. Select <b>File->Save As</b>, change the <i>save as type</i> to <b>All Files</b> and then <b>save</b> the file to your <i>Documents</i> folder as <b>DenyUriListForRecall.csv</b>

>[!IMPORTANT]Save the file as .CSV, not .txt.

5. Create a new blank text file in Notepad
6. <b>Type</b> or <b>copy</b> the following two lines into the new, blank text file

     +++ContosoCRM.exe+++

     +++HappyCustomers.exe+++

7. Select <b>File->Save As</b>, change the <i>save as type</i> to <b>All Files</b> and then <b>save</b> the file to your <i>Documents</i> folder as <b>DenyAppListForRecall.csv</b>

>[!IMPORTANT]Save the file as .CSV, not .txt.

8. After both CSV files have been saved, you may close Notepad. 
9. Return to the Edge browser session with your Intune console.
10. In the Intune console, navigate to <i>Devices</i>. Under <i>Manage devices</i>, select <b>Configuration</b>
11. Select <b>Create > New Policy</b>
   1. Platform: <b>Windows 10 and later</b>
   2. Profile type: <b>Settings catalog</b>
   3. Click <b>Create</b>
12. The Create profile wizard starts
13. On the <i>Basics</i> page, enter the following information
   1. Name: <i>lastname_firstname</i><b>_Enable Copilot+ PC AI Features</b>
   2. Description: <b>Enable AI features</b>
   3. Click <b>Next</b>
14. On the <i>Configuration settings</i> page, click the <b>+Add settings</b> option to open the Settings picker
   1. In the <i>Browse by category</i> list, scroll down to <b>Windows AI</b> and click <b>Windows AI</b>
   2. The Windows AI settings appear. <b>Select</b> the following settings:
      - [ ] Allow Recall Enablement
      - [ ] Allow Recall Export (Windows Insiders only)
      - [ ] Disable AI Data Analysis
      - [ ] Disable Click To Do (User)
      - [ ] Set Deny App List For Recall
      - [ ] Set Deny Uri List For Recall
      - [ ] Set Maximum Storage Duration For Recall Snapshots
      - [ ] Set Maximum Storage Space for Recall Snapshots
      
      You may now close the settings picker.
   3. The selected settings will appear in the left side of your Configuration Settings screen. You will now configure the settings as follows to meet your business objectives:
      1. Set Maximum Storage Space for Recall Snapshots: Use the drop-down menu to select <b>10 GB</b>
      2. Set Maximum Storage Duration for Recall Snapshots: Use the drop-down menu to select <b>60 days</b>
      3. At the Set Deny Uri List for Recall setting, click the <b>Import</b> button, <b>de-select</b> the "My data has headers" option, and then <b>browse</b> to the <b>DenyUriListForRecall.csv</b> file you created and saved earlier. Click <b>"Select"</b> to complete the import of the file. 
      
      !IMAGE[Exercise2-SetDenyUriListForRecall.jpg](instructions310362/Exercise2-SetDenyUriListForRecall.jpg)

      1. At the Set Deny App List for Recall setting, click the <b>Import</b> button, <b>de-select</b> the "My data has headers" option, and then <b>browse</b> to the <b>DenyAppListForRecall.csv</b> file you created. Click <b>"Select"</b> to complete the import of the file. 
      
      !IMAGE[Exercise2-SetDenyAppListForRecall.jpg](instructions310362/Exercise2-SetDenyAppListForRecall.jpg)
   
      2. Set the Disable Click to Do (User) setting to <b>Click to Do is enabled</b> if it is not already set to this value
      3. Set the Disable AI Data Anlysis slider to <b>Enable Saving Snapshots for Window</b> if it is not already set to this value.
      4. Set the Allow Recall Enablement setting to <b>Recall is available</b> if it is not already set to this value.
      5. Click <b>Next</b> to proceed in the Create profile wizard
1.  On the Scope tags page, leave the defaults and click <b>Next</b>
2.  On the Assignments page, leave the defaults (no groups selected) and click <b>Next</b>
3.  On the Review + create page, validate the configuration settings and then click <b>Create</b>

>[!NOTE]You did not necessarily need to use a text file to import the URIs and Apps, as you could simply enter them into the policy one row at a time. However, entering manually could be tedious if there are hundreds of entries. Knowing how to build the input files is critical for long-term maintenance in a complex environment.

You also could disable Recall, Snapshots and Click to Do with these settings. 

If your organization needs to disable these features (until they are approved for use) use the Allow Recall Enablement, Disable Click To Do, and Disable AI Data Analysis settings to disable the features. 

Once disabled, an end user will be unable to enable or use these features.

>[!IMPORTANT]Before proceeding to the next exercise, navigate to your <b>Documents</b> folder and <b>delete</b> the two CSV files you created in this exercise.

===
# Exercise Eight: Create AI Policy using Custom OMA-URI

<b>Objective</b>: Create an MDM policy that manages AI settings in Paint and Settings.

Not all AI policy settings are available in the Settings catalog (yet). There are settings that govern AI image capabilities and the use of the search agent in the Settings app. In this part of the lab you will construct a custom MDM policy that enables these features.

1. In the Intune console, navigate to <i>Devices</i>. Under <i>Manage devices</i>, select <b>Configuration</b>
2. Select <b>Create > New Policy</b>
   1. Platform: <b>Windows 10 and later</b>
   2. Profile type: <b>Templates</b>
   3. The <i>Template name</i> list will appear. 
   4. Select the option <b>Custom</b>
   5. Click <b>Create</b> to start the policy creation wizard
3. On the <i>Basics</i> page, enter the following information
   1. Name: <i>lastname_firstname</i><b>_Enable Image AI and Settings Agent Copilot+ PC</b>
   2. Description: +++Enable AI features that are not present in the Settings catalog+++
   3. Click <b>Next</b>
4. On the Configuration Settings page, click the <b>Add</b> button.
5. For the first setting, copy in the following information:
   1. <i>Name</i>: +++Allow Paint CoCreator+++
   2. <i>Description</i>: +++Enables Cocreator in Windows Paint+++
   3. <i>OMA-URI</i>: +++./Device/Vendor/MSFT/Policy/Config/WindowsAI/DisableCocreator+++
   4. <i>Data Type</i>: Integer
   5. <i>Value</i>: +++0+++
   6. Click <b>Save</b> to save the setting into the policy
6. Click the <b>Add</b> button.
7. For the second setting, copy in the following information:
   1. <i>Name</i>: +++Allow Generative Fill+++
   2. <i>Description</i>: +++Enables the use of generative fill in Windows Paint+++
   3. <i>OMA-URI</i>: +++./Device/Vendor/MSFT/Policy/Config/WindowsAI/DisableGenerativeFill+++
   4. <i>Data Type</i>: Integer
   5. <i>Value</i>: +++0+++
   6. Click <b>Save</b> to save the setting into the policy
8. Click the <b>Add</b> button.
9.  For the third setting, copy in the following information:
    1. <i>Name</i>: +++Allow Image Creator+++
    2. <i>Description</i>: +++Enables use of Image Creator in Windows Paint+++
    3. <i>OMA-URI</i>: +++./Device/Vendor/MSFT/Policy/Config/WindowsAI/DisableImageCreator+++
    4. <i>Data Type</i>: Integer
    5. <i>Value</i>: +++0+++
    6. Click <b>Save</b> to save the setting into the policy
10. Click the <b>Add</b> button.
11. For the fourth setting, copy in the following information:
    1. <i>Name</i>: +++Allow Settings Agent+++
    2. <i>Description</i>: +++Enables Settings Agentic Search experience+++
    3. <i>OMA-URI</i>: +++./Device/Vendor/MSFT/Policy/Config/WindowsAI/DisableSettingsAgent+++
    4. <i>Data Type</i>: Integer
    5. <i>Value</i>: +++0+++
    6. Click <b>Save</b> to save the setting into the policy
12. Click <b>Next</b>
13. On the <i>Assignments</i> page, leave the policy unassigned and click <b>Next</b>
14. On the <i>Applicability</i> page, leave the rules blank and click <b>Next</b>
15. On the <i>Review</i> page, review the policy and then click <b>Create</b>

You also could disable these features as well. If your organization needs to disable these features (until they are approved for use) you would set the integer value to 1 to put each feature into a disabled state.

===
# Exercise Nine: Create Notepad AI (ADMX-backed) Policy

<b>Objective</b>: Gain hands-on experience building an Inutne policy to manage the use of AI in Notepad

To disable the AI features in Notepad requires an ADMX-backed policy in Intune. The Notepad policy definition file is available as a download from the Microsoft Download site, but to make it easier for lab participants, we have already included the necessary files in <b>C:\LAB583\Exercise9-NotepadADMX</b>.

The Notepad policy definition has a dependency on the Windows Administrative template, which can be found in the local policy store on a Windows 11 device and does not require additional downloading. 

1. In the Intune console, navigate to <i>Devices</i>. Under <i>Manage devices</i>, select <b>Configuration</b>
2. In the middle of the screen, there are three tabs - Policy (the default view), Import ADMX, and Monitor. 
3. Click on the <b>Import ADMX</b> tab
4. Click the <b>Import</b> button

!IMAGE[Exercise2-ImportADMXView.png](instructions310362/Exercise2-ImportADMXView.png)

5. <b>Selet</b> the <i>folder icon</i> for the ADMX file and then <b>navigate</b> to <b>C:\Windows\PolicyDefinitions</b> folder
6. <b>Select</b> the file <b>Windows.admx</b> and then select <b>Open</b>
7. Next you will import the Windows localized administrative template. To do this, select the <i>folder icon</i> for the ADML file and then <b>navigate</b> to <b>C:\windows\PolicyDefinitions\en-US</b>
8. Select the file <b>Windows.adml</b> and then select <b>Open</b> </b>. 

!IMAGE[Exercise2-ADMXandADMLImported.png](instructions310362/Exercise2-ADMXandADMLImported.png)
 
9. Click <b>Next</b>
10. Click the <b>Create</b> button
11. On the <i>Import ADMX</i> page, click <b>Refresh</b> to confirm the upload was successful 

!IMAGE[Exercise2-WindowsADMXImported.png](instructions310362/Exercise2-WindowsADMXImported.png)

12. After the Windows ADMX has been successfully imported, you will be able to import the Notepad ADMX/ADML files 
13. On the <i>Import ADMX</i> page, click <b>Import</b> again
14. Select the <i>folder icon</i> for the ADMX file and then <b>navigate</b> to <b>C:\LAB583\Exercise9-NotepadADMX\WindowsNotepadAdminTemplates</b>
15. Select the <b>WindowsNotepad.admx</b> file and import it.
15. Select the <i>folder icon</i> for the ADML file and then <b>navigate</b> to the en-US subfolder to locate the <b>WindowsNotepad.adml</b> file and import it.

!IMAGE[Exercise2-NotepadADMXADMLImported.png](instructions310362/Exercise2-NotepadADMXADMLImported.png)  

16. Click <b>Next</b>
17. Click the <b>Create</b> button
18. On the <i>Import ADMX</i> page, click <b>Refresh</b> to confirm the upload was successful 

!IMAGE[Exercise2-NotepadADMXSuccessful.png](instructions310362/Exercise2-NotepadADMXSuccessful.png)  

19. In the <b>Intune Devices | Manage Devices | Configuration</b> screen, click back on the <i>Policies</i> tab
20. Select <b>Create > New Policy</b>
   1. Platform: <b>Windows 10 and later</b>
   2. Profile type: <b>Templates</b>
   3. The <i>Template name</i> list will appear. 
   4. Select the option <b>Imported Administrative templates (preview)</b>
   5. Click <b>Create</b> to start the policy creation wizard
21. On the <i>Basics</i> page, name the policy <i>lastname_firstname_</i><b>Disable Notepad AI features</b>
22. Click <b>Next</b>
23. Under <i>Setting name</i>, click on <b>Windows Components</b>, then <b>Notepad</b>, and then <b>Disable AI features in Notepad</b>
24. This will bring up the policy configuration fly-out. Select <b>Enabled</b> to disable AI features in Notepad.

!IMAGE[Exercise2-DisableAIfeaturesInNotepad.jpg](instructions310362/Exercise2-DisableAIfeaturesInNotepad.jpg)  

25. Click <b>OK</b> to save the setting
26. Click <b>Next</b> to proceed in the wizard
27. On the <i>Scope Tags</i> page, leave the Scope tags set to Default and click <b>Next</b>
28. On the <i>Assignments</i> page, leave the policy unassigned and click <b>Next</b>
29. Review the policy settings on the <i>Review + create</i> page and then click <b>Create</b>

You have now successfully created three different kinds of policies in Intune to manage AI features on Windows 11 and Copilot+ PCs!


===
#Exercise Ten: Start an M365 Copilot Researcher task

In the very last exercise of this lab you will be using the output of M365 Copilot Researcher as the starting point for leveraging multiple Copilot+ PC AI features. 

It will take Researcher several minutes to complete its task. 

Starting the Reseracher now, and letting it run in the background, will save you "wait time" later in this lab. 

We will repeat this scenario in Exercise 13, but to provide context for this task, we have included it below:

<b>Scenario</b>: Your leadership has indicated that since Windows 11 25H2 supports Wi-Fi 7 Enterprise, they would like to upgrade network access points across all locations to support Wi-Fi 7. They would like you to come up with a phased migration plan to upgrade your branch offices and main locations with Wi-Fi 7 supported infrastructure. They would like a detailed plan for your peers, as well as high-level summarization to persuade stakeholders to fund the project. They would like you to also provide illustrations to be used in both documentation and presentations on this topic. And they want it all done before this lab is complete!

### Begin with an idea

Copilot+ PCs have several local AI features, but to start with you would likely want to use the power of a Large Language Model through M365 Copilot. 

1. Launch <b>M365 Copilot</b>
2. Ensure you are signed in with the M365 Copilot licensed Entra ID provided to you as part of this lab.
3. You will use the Researcher agent in M365 Copilot. You can do so by selecting Researcher under the available chat agents, or invoke Researcher  by typing +++@Researcher+++ in the M365 Copilot chat prompt and pressing <b>Enter</b>.

!IMAGE[Exercise13-InvokingResearcher.png](instructions310362/Exercise13-InvokingResearcher.png){500}

3. Use the following prompt (or modify it and use your own) in M365 Copilot Researcher:

+++You are an IT professional tasked with planning a network migration from legacy Wi-Fi access points to Wi-Fi 7. You need to construct a proposal on the recommended approach, important technical considerations, implementation plan, recommended timeline, test plan and user communications.+++

4. <b>Answer</b> any follow-on questions that Researcher may have about this request and confirm it is building a response.

>[!NOTE]<b>It will take several minutes for Researcher to build a response.</b> In the meantime, <b>minimize</b> M365 Copilot so that it continues to run in the background and then move on to the next exercise.


===
# Exercise Eleven: Live Captions with Translation

<b>Objective</b>: Learn how to turn on and use Live Captions with Translation.

Live captions helps <b>everyone</b> better understand spoken audio by providing automatic transcription. 

To make more content accessible to more people, live captions now has the ability to provide translations and will turn any audio that passes through your PC into a single caption experience. When using a Copilot+ PC, live captions instantly translate any live or pre-recorded video in any app or video platform from over 40 languages into English and 27 languages into Chinese (Simplified).

### Languages supported with Live Captions with Translation (as of October 2025)

---
| Originating Language | Translated in English | Translated into Simplified Chinese |
|:---------------------|:---------------------:|:----------------------------------:|
| Arabic | X | X |
| Basque | X |  |
| Bosnian | X |  |
| Bulgarian | X | X |
| Chinese (Cantonese) | X |  |
| Chinese (Mandarin) | X |  |
| Chinese (Simplified, China) | X |  |
| Czech | X | X |
| Danish | X | X |
| Dutch | X |  |
| English | X | X |
| Estonian | X | X |
| Finnish | X | X |
| French | X | X |
| Galician | X | |
| German | X | X |
| Greek | X | X |
| Hindi | X | X |
| Hungarian | X | X |
| Indonesian | X | |
| Irish | X | |
| Italian | X | X |
| Japanese | X | X |
| Korean | X | X |
| Latvian | X |  |
| Lithuanian | X | X |
| Macedonian | X | |
| Maltese | X | |
| Norwegian | X | X |
| Pashto | X | |
| Polish | X | X | 
| Portuguese | X | X |
| Romanian | X | X |
| Russian | X | X |
| Serbian | X |  |
| Slovak | X | X |
| Slovenian | X | X |
| Somali | X |  |
| Spanish | X | X |
| Swedish | X | X |
| Thai | X |  |
| Turkish | X | X |
| Ukrainian | X | |
| Vietnamese | X | |
| Welsh | X |  |

---
All live captions with translation processing occurs locally. The audio, voice data, and captions <b>never leave your device</b> and are not shared to the cloud or with Microsoft. The generated captions are not stored anywhere on the device or the cloud. 

>[!NOTE] What about if you are using a headset with your Copilot+ PC? Live Captions processes the sound that is coming through the system output. You can manage this by navigating to <b>System > Sound</b> in Settings and choosing to play sound all output sound through your headset. If System sounds are coming through onboard speakers, but Teams sound is redirected to your headset, the Live Captions will not process the sound in your headset. 

### Configure and use Live Captions with Translation

1.  There are several entry points to enabling live captions with translation: 
    1. <b>Option 1: Use quick settings</b>
        1. In the lower right-hand corner of the task bar, click the </i>battery, network, or volume icon</i> 
        2. The quick settings menu launches 
        3. Within the quick settings menu, click the <b>Accessibility</b> option as shown in the image below 
        
        !IMAGE[Exercise11-QuickSettingsFlyout.png](instructions310362/Exercise11-QuickSettingsFlyout.png){200}

        4. Scroll down the list of Accessibility options. Under <i>Hearing</i>, locate <b>Live captions</b>. 
        
        !IMAGE[Exercise11-LiveCaptionsOption.png](instructions310362/Exercise11-LiveCaptionsOption.png){300}

        5. To enable, you would toggle Live Captions from Off to On. <b>Do not make this change yet</b>, as there are two other ways to enable the feature.
        6. <b>Close</b> the quick settings menu.
    2. <b>Option 2: Use the Settings app</b> 
        1. Open the <b>Settings</b> app
        2. In the <i>left-hand menu</i>, select <b>Accessibility</b>, then under the <b>Hearing</b> section, select <b>Captions</b> 
        
        !IMAGE[Exercise11-OpenCaptionsInSettings-1.png](instructions310362/Exercise11-OpenCaptionsInSettings-1.png){600}

        3. Inside of this settings page is an option to toggle Live Captions from Off to On. Do not make this change yet, as there is one more way to enable the feature.
        4. <b>Close</b> the Settings app.
    4. <b>Option 3: Use a key combo</b>
        1. Press <b>Windows key + Ctrl + L</b> to enable captions. (Do not just press Windows and L together, as this will lock your screen!)
        2. At the top of your screen, you will be presented with the option to enable live captions with translation. 
        
        !IMAGE[Exercise11-LiveCaptionsWithTranslationPrompt.png](instructions310362/Exercise11-LiveCaptionsWithTranslationPrompt.png){500}

        3. Press the <b>Yes, continue</b> option 
        4. Live Captions with Translation are now enabled. By default, it enables to English (United States). Click the English (United States) drop-down to see the options for Chinese (Simplified, Mainland China) and Chinese (Traditional, Hong Kong SAR). Select the language option that you are most comfortable with before proceeding.
        5. Press the <b>Continue</b> button on the "Getting ready to show live captions" banner.
        6. You will now be asked to download the language file to show captions. Press <b>Yes, continue</b> to proceed with the download.
        7. Wait a few moments for Live Captions to be configured.

	>[!IMPORTANT] If Live Captions with Translation crashes, please see the "Manually Install English Translation Model" section below and then return to this step.

    3. Ensure you have the <b>sound turned on</b> on your lab PC with sound coming through the speakers. Live Captions with Translation works by processing the sound that is being played through the speakers.
    4. Open File Explorer and navigate to <b>C:\LAB583\Exercise11-Translation</b> and launch the file <b>LiveCaption.mp4</b>. If the video begins to auto-play, pause it.
    5. Press <b>Windows key + Ctrl + L</b> to enable captions
    6. Play or resume the video and observe the real-time captions.
    7. You can drag the captions bar from the top of the screen to any other position on your screen simply by clicking on it and moving the bar.
    8. You are also able to change the position and the caption style. Click the Settings icon in the right-corner of the live captions bar to show the available settings:
        1. You can select above screen, below screen or overlaid with the screen. Experiment with these settings to observe the results.
        2. You can also adjust the style by selecting <b>Preferences > Caption Style</b>. This will launch the Settings app where you can change the style to white on black, yellow on blue, or even edit it for a custom background color / font color that best suits you! You can adjust your fonts, the size, and opacity too!

<br>
### Manually Install English Translation Model (Only If Necessary)

If everything is configured correctly, your lab PC will be able to install and configure the language model to support translation. 

In the event that Live Captions with Translation crashes, you should be able to remedy by manually installing the translation pack. 

1. On your lab PC, open File Explorer and navigate to </b>C:\LAB583\Exercise11-Translation\English Translation Model</b>
2. There are four files in this folder. Look for the file <b>cd222ccc12254d1cb566849d38ec826a.msix</b>
3. <b>Double-click</b> the file <b>cd222ccc12254d1cb566849d38ec826a.msix</b>
4. A po-up window will appear asking if you want to install the model. Click <b>Install</b>.

!IMAGE[Exercise11-InstallSpeechTranslationPack.png](instructions310362/Exercise11-InstallSpeechTranslationPack.png){400}

5. Once the install is complete, return to the steps above to start Live Captions with Translation and complete this lab exercise.

===
# Exercise Twelve: Configure Windows Studio Effects

<b>Objective</b>: Learn how to turn on and use Windows Studio Effects

Windows Studio Effects leverages the NPU on the Copilot+ PC to enable AI effects including background blur, eye contact, auto framing and more. The effects are applied at the hardware level, so it works with any app that leverages the camera, <i>even if the app doesn't know about the effect</i>.

When a camera is opted into using Windows Studio Effects, the Windows Studio Effects package gets chained on to the end of the camera. This happens transparently so that the "real" camera is replaced with a "composite" camera consisting of the features of the camera plus the Windows Studio AI effects. 

There are two ways an end user can interact with Windows Studio Effects and in this exercise you will explore both methods.

### Access Windows Studio Effects through Quick Settings

1. In the lower right-hand corner of the task bar, click the <i>battery, network, or volume icon</i>
2. The quick settings menu launches
3. Within the quick settings menu, click the <b>Studio Effects</b> option

!IMAGE[Exercise12-StudioEffects.png](instructions310362/Exercise12-StudioEffects.png){300}

4. The first six Windows Studio Effects settings will appear. 
    1. <i>Portrait Light</i> applies a more natural lighting appearance to your face
    2. <i>Portrait Blur </i> is able to apply a light blur and keep you in focus 
    3. <i>Standard Blur</i> applies a strong background blur for when you want to minimize the background
    4. <i>Creative Filter: Illustrated</i> will change your video into an illustration
    5. <i>Creative Filter: Animated</i> will change your video into an animated cartoon
    6. <i>Creative Filter: Watercolor</i> will change your video into a watercolor painting
    7. Only one <i>Creative Filter</i> can be applied at a time (they cannot be stacked). These are intended for a more fun experience.
    8. Experiment with the different settings available by clicking on each to enable them. The camera preview will show you the results of enabling/disabling each Studio Effect.
5. You can scroll to the next Studio Effects settings by scrolling down with your mouse scroll, or clicking the downward triangle on the right-hand side of the Quick Settings.

!IMAGE[Exercise12-ScrollDownQuickSettings.png](instructions310362/Exercise12-ScrollDownQuickSettings.png){300}

6. The final three Windows Studio Effects settings will appear
    1. <i>Eye Contact: Standard</i> provides a subtle correction for a user who is looking down from the camera to the screen. It does not adjust the left or right movement of the eyes.
    2. <i>Eye Contact: Teleprompter</i> is a more aggressive correction for a user whose eyes move around the screen as they read teleprompter content
    3. <i>Automatic Framing</i> detects a person within the camera field of view and crops and zooms to keep them framed
7. Experiment with the eye contact and automatic framing settings. The camera preview will show you the results of enabling/disabling each Studio Effect.

### Access Windows Studio Effects through the Settings app

Users can also access Studio Effects through the Windows Settings app.

1. Launch the <b>Settings</b> app
2. In the left-hand menu, select <b>Bluetooth & devices</b>
3. Locate the <i>Cameras</i> option in the <i>Bluetooth & devices</i> page, and then click <b>Cameras</b>

!IMAGE[Exercise12-BluetoothDevicesPage.png](instructions310362/Exercise12-BluetoothDevicesPage.png){500}

4. The list of cameras should include a front-facing connected camera as shown in this image. <b>Click</b> the front-facing connected camera to open its settings.

!IMAGE[Exercise12-ConnectedCameras.png](instructions310362/Exercise12-ConnectedCameras.png){500}

5. The list of Windows Studio Effects will appear just below the camera preview.

!IMAGE[Exercise12-StudioEffectsInSettings.png](instructions310362/Exercise12-StudioEffectsInSettings.png){500}

6. In the Settings app, it is easier to see which options are mutually exclusive - for instance, you can either apply Standard blur or Portrait blur, but not both.

7. Experiment with turning different Studio Effects on and off to see how the camera is affected.


===
# Exercise Thirteen: Putting Copilot+ PC AI Features Together

So far in this hands on lab, you have had the opportunity to use AI features indepdendently on a Copilot+ PC. This exercise starts with a scenario and builds on it using the AI tools available. This exercise will generally lack screenshots, as we want you to experiment with the tools and the outcomes - and your outcomes could greatly vary from those around you!

The workflow below intentionally has you moving from tool to tool, even in cases where we could achieve the same result by staying within one tool. This is so that you get a feel for how you can achieve outcomes with different approaches.

<b>Objective</b>: Gain hands on experience using multiple AI features together to complete a business scenario.

<b>Scenario</b>: Your leadership has indicated that since Windows 11 25H2 supports Wi-Fi 7 Enterprise, they would like to upgrade network access points across all locations to support Wi-Fi 7. They would like you to come up with a phased migration plan to upgrade your branch offices and main locations with Wi-Fi 7 supported infrastructure. They would like a detailed plan for your peers, as well as high-level summarization to persuade stakeholders to fund the project. They would like you to also provide illustrations to be used in both documentation and presentations on this topic. And they want it all done before this lab is complete!

### Begin with an idea

1. You already prompted M365 Copilot Researcher a few minutes ago to build you your phased migration plan.
2. <b>Maximize</b> M365 Copilot to view the full response.
3. <b>Highlight</b> the response and copy / paste it into Word, or select the <b>Open in Word</b> option if it's available.
4. You now have a good start for your project plan.
5. Let's explore how Click to Do can help with project communications to project stakeholders.

### Click to Do

1. Scroll to the beginning of the proposal where there should be an introduction. It's likely that Copilot Researcher put in a lot of technical jargon and detail.
2. <b>Launch Click to Do</b> (Windows + Q, swipe in from right, or Windows + Left Mouse Click), <b>highlight</b> the introduction and select <b>Summarize</b>.
3. Click to Do should summarize the intro into a simpler, higher-level summary that is (hopefully!) appropriate for an email to leadership explaining the intent of the project. 
4. Select <b>Copy</b> from within the Click to Do results, then open <b>Notepad</b> and <b>paste</b> into Notepad.
5. Note that you have not changed any of the wording within the proposal itself. 


### Notepad AI

1. In Notepad, let's make the summary a little longer - your stakeholders will want to see more than a sentence to convince them this project is a great idea!
2. In the Notepad AI options, select <b>Make Longer</b>
3. After the summary has been rewritten to be longer, but <u>before</u> replacing the text, let's alter the tone. We want to persuade leadership that this is the right investment to make, so change the tone to Persuasive and click the "Try Again" button.
4. Click the <b>Replace</b> button to replace the original summary with a longer, more persuasive intro.

Let's suppose you have emailed this proposal summary to your stakeholders and one of them asks for an example of a site survey map your team will be producing as part of this project. 

### Visualize Ideas with AI in Paint

f you cannot remember how to use specific AI features in Paint, revisit Exercise Five and then return to this step to build an example site survey diagram.

1. Use <i>Cocreator</i> in Paint with the prompt +++an office floor plan with wireless access points highlighted+++ (or experiment with alternate prompts)
2. Begin sketching a rough office layout and Paint will cocreate with you. An example is shown below

!IMAGE[Exercise13-Cocreator.png](instructions310362/Exercise13-Cocreator.png){500}

3. After adding some walls and openings, click <b>+Apply</b> to apply the Cocreated image
4. Tip: AI often has issues with generating text an image, so remove any bad/grabled text with solid boxes in Paint.
5. Use the <i>Sticker generator</i> to build a sticker for a wireless access point 

!IMAGE[Exercise13-WirelessAccessPointSticker.png](instructions310362/Exercise13-WirelessAccessPointSticker.png){200}

6. Drop some Wireless Access Point stickers onto your floor plan
7. You are now a network engineer! (Just kidding...)

<i>Bonus exercise</i>: 

A fun, retro way to build a sample floor plan is to use the <i>Image Creator</i> feature with the prompt +++draw an example office floor plan with wireless access points+++ and select Pixel Art as the style. Generate some images and bask in the glory of the 90's.

### Enable Studio Effects for Collaboration Call

Your stakeholders have requested a video conference to collaborate on identifying resources for your migration plan. You want to make sure that your background is blurred, your eyes maintain camera contact as you read from your document, and the camera to track you in case you start to move. 

From memory, launch Studio Effects and enable the features that will help present the right video image during the call. 

If you are unable to remember how to launch Studio Effects, revisit Exercise Twelve and then return to this point of the exercise.


### Live Captions with Translation

During the call, one of your colleagues from France would like to bring up an issue on the call but says he isn't sure of the right way to say it in English and would prefer to use French.

1. Start Live Captions with Translation so that you can follow along as he speaks in his primary language. If you don't remember the key sequence to start Live Captions with Translation, revisit Exercise Eleven.
2. Launch the lab file <b>C:\LAB583\Exercise13\TeamsCall.mp4</b>


### Agent in Settings

During the call, one of your colleagues asks what information the end user will need to be able to discover the new Wi-Fi network and connect to it.

Using Agentic Search in Settings, search for +++connect to new wireless network+++ to show how the appropriate Settings page can be found easily using this search.


### Snipping Tool

The end user guide will need a screenshot of the <b>Network & internet > Wi-Fi > Wi-Fi</b> Settings page.

1. Launch Snipping tool to take a screenshot of the entire Wi-Fi Settings page, including the name and email address of the logged on user in the upper left corner.
2. With the image open in Snipping Tool, click on the "Text actions" option in the menu bar 

!IMAGE[Exercise13-TextActionsButton.png](instructions310362/Exercise13-TextActionsButton.png){400}

3. The third Text action option is Quick redact, which is set to redact email addresses and phone numbers. Click <b>Quick Redact</b> and a bar should appear over the email address of the logged on user. 

!IMAGE[Exercise13-QuickRedact.png](instructions310362/Exercise13-QuickRedact.png){300}

4. Use the Quick redact drop down menu to <b>Remove all redactions</b> and restore the image to its original state. 

===
# Completion

---
<br>
## <b>Thank you</b> for participating in our hands-on lab here at Ignite 2025.

<br>
## Please remember to provide <b>feedback</b> about this session.

<br>

## Please enjoy the remainder of Ignite 2025!
