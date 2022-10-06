# Exercise 2.3 - Create an SAP Fiori App Using SAP Business Application Studio

In this exercise, you will develop a simple SAPUI5 freestyle application, adhering to SAP Fiori design guidelines. The easiest way to develop an SAPUI5 freestyle app from scratch is to create it from a template. To continue developing an existing application, the best practice is to use git source code management and clone the repository.

Using the app creation wizard you can at any point click the Back button to go back to the previous step, or click a specific wizard step to go back to that step.


## Step 1: Create an SAPUI5 app from a template

1. In the *Welcome* tab click **Start from template**.

![Start from Template](1-StartfromTemplate.png)

2. Select the **SAP Fiori Application** tile, and click **Start**.

![SAP Fiori](2-SAPFioriApp.png)

3. For *Floorplan Selection*, select *Application Type* **SAPUI5 freestyle** from the drop-down, then select the floorplan **SAPUI5 Appliction** and click **Next**.

![SAPUI5 Freestyle](3-SAPUI5App.png)

4. For *Data Source and Service Selection*, select **None** from the drop-down as for this simple app, you will not consume any data from a backend system. Then click **Next**.

![Select Data Source](4-DataSource.png)

5. In the next step, you can change the name of the view. You can simply keep View1 here and click **Next**.

![View name](5-ViewName.png)

6. For **Project Attributes**, select the following, and click **Next**.

    | Step | Parameter | Value |
    |:-----|:----------|:------|
    | A | Module name | **`helloworld`** |
    | B | Application title | **Hello World** |
    | C | Application namespace | **teched** |
    | D | Description | **An empty SAPUI5 freestyle app** |
    | E | Project folder path | **`/home/user/projects`** (default)|
    | F | Minimum SAPUI5 version | **1.102.1** (default) |
    | G | Add deployment configuration | **Yes** |
    | H | Add FLP configuration | **Yes** |
    | I | Configure advanced options | **No** (default) |

    ![Project Attributes](6-Attributes.png)
    
7. For **Deployment Configuration**, select **Cloud Foundry** from the drop-down. Keep *Destination Name* **None** and **Yes** for using the managed app router, as you will not use a backend system for consuming data. Click **Next**.

![Deployment Settings](7-DeploymentSettings.png)

>When end-users access an app in the Cloud Foundry environment, they actually access the Application Router first. The application router is used to serve static content, authenticate users, rewrite URLs, and forward or proxy requests to other micro services while propagating user information.
>
>The recommendation is to use **Managed Application Router** that provides many benefits, when compared to Standalone Application Router, such as save resources, lower maintenance efforts, an easier integration into SAP Build Work Zone, etc. Standalone Application Router should only be used in advanced cases, for example when application router extensibility is required. More information is available in [Developing HTML5 Applications in the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/11d77aa154f64c2e83cc9652a78bb985.html)

8. Finally, for **Fiori Launchpad Configuration**, select the following, and click **Finish**.

    | Step | Parameter | Value |
    |:-----|:----------|:------|
    | A | Semantic Object | **helloworld** |
    | B | Action | **display** |
    | B | Title | **My Hello World** |
    | B | Subtitle (optional) | Add a subtitle of your choice |

    ![Launchpad configuration](8-LaunchpadConfig.png)


## Exercise 2.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc = 0.
    response->set_status( i_code = 200
                     i_reason = 'Everything is fine').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex2/images/02_02_0010.png)

## Summary

You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
