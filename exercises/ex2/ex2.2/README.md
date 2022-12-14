# Exercise 2.2 - Create an SAP Fiori App Using SAP Business Application Studio

In this exercise, you will develop a simple SAPUI5 freestyle application, adhering to SAP Fiori design guidelines. The flow consists of two parts:

1. Running a wizard that creates a multi-target application (MTA) project that is configured to use Managed Application Router. 
2. Creating an SAPUI5 app from a template within this project and preview it.

<br>

### Step 1: Create new Multitarget Application project

> An MTA is required in order to create the deployment artifact for SAP BTP, Cloud Foundry environment. If you are not familiar with the MTA concepts, read this [guide](https://www.sap.com/documents/2016/06/e2f618e4-757c-0010-82c7-eda71af511fa.html). Creating the MTA project upfront does not take long and will allow you to save time later in the exercise.

The search window on top of the page gives you easy access to search across your files. It also allows you to search for commands. 

1. Enter **>** into the Search window to search for a command. 

   ![Open command palette](images/n01-search-command.png)

> You could also access the command palette via the **menu** icon on the top left of the screen and **View > Command Palette** 

2.  Type `fiori: open` in the search field and select the **Fiori: Open CF Application Router Generator** command.

    ![Find CF Application Router Generator](images/n02-search-fiori.png)

4. The **Application Router Generator Wizard** tab is opened. For **Application Router Configuration**, select the following, and click **Finish**.

    | Step | Parameter | Value |
    |:-----|:----------|:------|
    | A | Application router project path | **/home/user/projects** (default) |
    | B | MTA ID | **`FioriDemo`** |
    | C | MTA Description | Can be left empty (default) |
    | D | Add route module | **Managed Approuter** |

    ![Fill-in cf mta and approuter wizard](images/n03c-CreateRoute.png)

    >When end-users access an app in the Cloud Foundry environment, they actually access the Application Router first. The application router is used to serve static content, authenticate users, rewrite URLs, and forward or proxy requests to other micro services while propagating user information.

    >The recommendation is to use **Managed Application Router** that provides many benefits, when compared to Standalone Application Router, such as save resources, lower maintenance efforts, etc. Standalone Application Router should only be used in advanced cases, for example when application router extensibility is required. More information is available in [Developing HTML5 Applications in the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/11d77aa154f64c2e83cc9652a78bb985.html)

5. Wait until the creation of project is completed. A notification that "The files have been generated" appears at the bottom right of the screen.

    ![project creation completed](images/04c-FilesGenerated.png)

<br>

### Step 2: Add your folder to a workspace

Your workspace is an entity containing your project's settings, debug configurations, and task configurations. You can choose to create a new workspace or for each project or you can set up a multi-root environment that holds several projects. You can find out more about **Workspaces** in the SAP Business Application Studio [documentation](https://help.sap.com/viewer/9d1db9835307451daa8c930fbd9ab264/Cloud/en-US/0919ce1ca4a342628e49c0f5e9c8cdcf.html).

1. Click the menu icon and select **File | Add Folder to Workspace...** to open the **Add Folder to Workspace** dialog.

    ![open workspace dialog](images/n04c-add-to-workspace.png)

2. The **Add Folder to Workspace** dialog is opened at the center of the SAP Business Application Studio window. Select the **projects** folder. 

    ![open workspace dialog](images/n05-select-projects.png)
   
3. Now select the **`FioriDemo`** project and click **OK**.

    ![select-FioriDemo](images/n06-confirm.png)

3. SAP Business Application Studio reloads with the `FioriDemo` project open in a yet untitled workspace. In the Explorer view you can see the `FioriDemo` project, its folder structure, and files.

    >The status bar color changes to blue, indicating that a workspace is open.

    ![workspace_open](images/n07-untitled-workspace.png)

<br>

### Step 3: Create an SAPUI5 app from a template

Using the app creation wizard you can at any point click the Back button to go back to the previous step, or click a specific wizard step to go back to that step.

1. In the *Get Started* tab click **Start from template**.

   ![Start from Template](images/n07a-start-from-template.png)

2. Select the **SAP Fiori Application** tile, and click **Start**.

   ![SAP Fiori](images/n08-fiori-app.png)

3. In the *Template Selection* screen, select *Application Type* **SAPUI5 freestyle** from the drop-down, then select the template **SAPUI5 Appliction** and click **Next**.

   ![SAPUI5 Freestyle](images/n09-sapui5-app.png)

4. For *Data Source and Service Selection*, select **None** from the drop-down as for this simple app, you will not consume any data from a backend system. Then click **Next**.

   ![Select Data Source](images/n10-data-source.png)

5. In the next step, you can change the name of the view. You can simply keep View1 here and click **Next**.

   ![View name](images/n11-view-name.png)

6. Select the following **Project Attributes**, then click **Next**.

    | Step | Parameter | Value |
    |:-----|:----------|:------|
    | A | Module name | **`helloworld`** |
    | B | Application title | **Hello World** |
    | C | Application namespace | **teched** |
    | D | Description | **An empty SAPUI5 freestyle application** |
    | E | Project folder path | **`/home/user/projects/FioriDemo`** (default)|
    | F | Minimum SAPUI5 version | **1.102.1** (default) |
    | G | Add deployment configuration | **Yes** (default)|
    | H | Add FLP configuration | **Yes** |
    | I | Configure advanced options | **No** (default) |

   ![Project Attributes](images/n12a-attributes.png)
    
7. For **Deployment Configuration**, keep the defaults **Cloud Foundry** and *Destination Name* **None**. Click **Next**.

   ![Deployment Settings](images/n13-deployment.png)

8. Finally, in the **Fiori Launchpad Configuration** screen, select the following, and click **Finish**.

    | Step | Parameter | Value |
    |:-----|:----------|:------|
    | A | Semantic Object | **helloworld** |
    | B | Action | **display** |
    | B | Title | **My Hello World** |
    | B | Subtitle (optional) | Add a subtitle of your choice |

    ![Launchpad configuration](images/n14-flp-config.png)


9. Wait until the installation of project dependencies is completed. A notification that "The project has been generated" appears at the bottom right of the screen, The **Application Information** tab is opened, and the files and project structure in the **Explorer** view are updated.
    
    ![application generated](images/n15-project.png)

<br>

### Step 4: Run the App Locally in the Dev Space

To test your app, you can now run it locally within SAP Business Application Studio.

1.	In the *Application Information* tab, click the **Preview Application** tile. A set of run configuration options display in the top-center of the screen.

    ![Preview App](images/n16-preview-app.png)

2.	Select the first entry **`Start fiori run...`** to run the app locally in a sandbox launchpad shell.

    ![Start helloworld](images/n17-start-options.png)

3. A new browser tab opens showing the app. As you did not add any content, the app only shows a title.

    >If your browser does not allow opening a new tab, you may see a message in the upper left corner with a link where you can allow opening a new tab.

    ![App running locally](images/n18-app-preview.png)

<br>

## Summary

You've now created a simple app. In the next exercise you will build the app and deploy it to Cloud Foundry.

Continue to - [Exercise 2.3 - Build and Deploy your application ](../ex2.3/README.md)
