# Integrate Your SAPUI5 App into Your Launchpad Site

In this exercise, you will learn how to a custom-developed SAPUI5 app that has been deployed to SAP BTP, Cloud Foundry environment to your site.

## Prerequisites
 - You've already created the `JobCore` launchpad site.
 - You've deployed your SAPUI5 app (including the navigation properties), to SAP BTP, Cloud Foundry environment.


Once you've deployed your SAPUI5 app to SAP BTP, it becomes available to add to your launchpad site.


### Step 1: Fetch updated content using the Provider Manager

1. Go back to the Administration environment of SAP Build Work Zone, standard edition.

2. Click the **Provider Manager** icon to view any available content providers.

    ![Open Provider Manager](0-open-provider-manager.png)

3. Select the **HTML5 Apps** content provider.

    >The **HTML5 Apps** content provider is created automatically. Any app that you deploy to SAP BTP is automatically added as content to this provider.

    !![Select the HTML5 Provider](3-HTML5-provider.png)

4. Click the **Fetch updated content** icon.

    ![Fetch updated content](00-fetch-updated-content.png)

The **HTML5 Apps** content provider will now expose any newly deployed app for integration.



### Step 2: Add your deployed SAPUI5 app to your content

1. Click the Content Manager icon in the side panel to open the **Content Manager**.

    !![Open Content Editor](1-open-content-editor.png)

    >The **Content Manager** has two tabs: **My Content** where you can manually configure content items and view any other available content items, and the **Content Explorer** where you can explore exposed content from available content providers, select the content, and add it to your own content.

2. Click the **Content Explorer** tab to explore content from the available content providers.

    ![Open Content Explorer](2-content-explorer.png)

3. Select the **HTML5 Apps** provider.

    ![Select the HTML5 tile](3a-select-HTML5-tile.png)

4. You'll see that your `Hello World` app that you've just created in SAP Business Application Studio, already exists in this provider. Select it and click **+ Add to My Content**.

    !![Add app to My Content](4-add-app-my-content.png)

5. Click the **My Content** tab.

    ![Click My Content](5-click-my-content.png)

    Note that your `Hello World` app is in the list of content items.


### Step 3: Create group and assign app to it

In this step, you'll create a new group and assign the `Hello World` app to it.

1. Click **+ New** in the **Content Manager** and select **Group** to create a new group.

    ![Add new group](6-add-group.png)

2. Enter `Simple Apps` as the **Title**.

3. In the **Assignments** panel on the right, click in the search box to see a list of apps.

    >If you have many apps, you can type some letters of your app name in the search bar, (for example, `he`) to search for the app.

4. Next to the `Hello World` app, click the **+** icon to assign your app to this group.

    ![Assign app to group](7-assign-app-to-group.png)

    You'll see that the icon changes.

4. Click **Save**.

    ![Save](8-save.png)



### Step 4: Assign app to Everyone role

In this step, you'll assign the `Hello World` app to the `Everyone` role. This is a default role - content assigned to the `Everyone` role is visible to all users.

1. Open the **Content Manager** from the side panel.

    ![Open Content Manager](9-open-content-manager.png)

2. Click the `Everyone` role to open the role editor.

    ![Everyone role](9a-everyone-role.png)

3. Click **Edit**.

    ![Edit role](10-edit-role.png)

4. Click the search box in the **Assignments** panel on the right. Any available apps are shown in the list below.

5. Next to the `Hello World` app, click the **+** icon. You'll see that the icon changes.

6. Click **Save**.


### Step 5: Review your site

1. Click the **Site Directory** icon to open the Site Directory.

    ![Open site directory](11-open-site-directory.png)

2. Click **Go to site** on the site tile.

    ![Open site](12-go-to-site.png)

    You'll see all the apps that you have created in your launchpad. In the `Our Suppliers` group, you'll see the `Suppliers` app that we've just created.

    ![See all apps](12a-view-launchpad.png)


3. Click the app to launch it.

    ![View app](13-suppliers-app.png)



