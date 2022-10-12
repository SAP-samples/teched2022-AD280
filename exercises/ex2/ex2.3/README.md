# Build and Deploy Your SAP Fiori App to SAP Business Technology Platform

In this exercise you will learn:
- how to build and deploy an application to SAP BTP, Cloud Foundry environment
- how to configure Cloud Foundry settings in SAP Business Application StudioBuild and deploy your SAP Fiori MTA project to your SAP BTP, Cloud Foundry environment.

<br>

### Step 1: Build the application


1. Go back to the **Explorer** pane.

![Go to Explorer](images/1-GotoExplorer)

2. Right-click the `mta.yaml` file and select **Build MTA Project**.

> You can collapse the *Open Editors* area for a better overview. 

![build mta](images/2-BuildMTA.png)

> The build process creates a multi-target archive (`MTAR`) file in your project that packages all the project modules for deployment. 
> You can find the `MTAR` file in the `FioriDemo/mta_archives` folder.

![terminal mbt build results](3-MTAArchives.png)

<br>

### Step 2: Set Cloud Foundry preferences

If you are not logged in to a Cloud Foundry space - Before you can deploy your new application, set your Cloud Foundry preferences.

1. In the menu bar, select **View | Find Command** to open the **command palette**.

2. Select the command **CF: Login to cloud foundry**.

    > Type `cf` to filter commands.

    ![Command Palette-Login to CF](images/5-LoginCF.png)

3. A **Cloud Foundry Sign In** tab opens in SAP Business Application Studio. Select the API endpoint, provide your credentials, and click **Sign in**.

    ![Cloud Foundry Login dialog](images/6-Credentials.png)

4. Select the Cloud Foundry organization, Cloud Foundry space, and click **Apply**.

    ![Cloud Foundry Login dialog](BAS-CF-Login-4-.png)

    > A *You have been logged in* notification appears at the bottom-right of your screen.
    

    ![Logged in to CF](BAS-CF-Login-5-.png)

<br>

### Step 3: Deploy your application to SAP BTP, Cloud Foundry environment

1. Right-click the `mtar` file and select **Deploy MTA Archive**.

    ![deploy mtar](images/5-Deploy.png)

    >The application deployment to the space you are connected to starts and a notification appears. You can follow the deployment progress in the **Task: Deploy** console at the bottom of your screen.

3. Wait for the deployment to complete.

    >The deployment process takes a few minutes. When the deployment process is complete, the notifications **Process finished.** and **Terminal will be reused by tasks.** will appear at the bottom of the **Task: Deploy** console.

    > ![deploy success](BAS-Deploy-2-.png)



## Summary

With this, you have successfully completed the deployment of your SAP Fiori app to SAP BTP using SAP Business Application Studio.

Continue to - [Exercise 2.4 - Integrate Your SAPUI5 App into Your Site](../ex2.4/README.md)

