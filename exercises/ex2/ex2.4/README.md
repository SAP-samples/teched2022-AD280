# Integrate Your SAPUI5 App into Your Launchpad Site

In this exercise, you will learn how to a custom-developed SAPUI5 app that has been deployed to SAP BTP, Cloud Foundry environment to your site.

## Prerequisites
 - You've already created the `JobCore` launchpad site.
 - You've deployed your SAPUI5 app (including the navigation properties), to SAP BTP, Cloud Foundry environment.


Once you've deployed your SAPUI5 app to SAP BTP, it becomes available to add to your launchpad site.


<br>

### Step 1: Fetch updated content using the Provider Manager

1. Go back to the Administration environment of SAP Build Work Zone, standard edition.

2. Click the **Channel Manager** icon to view any available content channels. In this screen, administrators can create content channels, e.g. to consume federated content from a provider system like SAP S/4HANA.

    ![Open Channel Manager](images/1-open-channel-manager.png)

3. In the **HTML5 Apps** row, click the **Update content** icon to consume any newly deployed apps for integration. You will see a message that the content is being updated. Wait till the status is set to **Updated**.

    >The **HTML5 Apps** content channel is available by default out of the box. Any app using the managed app router that you deploy to SAP BTP is automatically added as content to this channel.

    ![Update the HTML5 Provider](images/2-update-html5.png)

<br>

### Step 2: Add your deployed SAPUI5 app to your content

1. Click the Content Manager icon in the side panel to open the **Content Manager**.

    ![Open Content Editor](images/3-go-to-content-manager.png)

    >The **Content Manager** has two tabs: **My Content** where you can manually configure content items and view any other available content items, and the **Content Explorer** where you can explore exposed content from available content channels, select the content, and add it to your own content.

2. Click the **Content Explorer** tab to explore content from the available content providers.

    ![Open Content Explorer](images/4-content-explorer.png)

3. Select the **HTML5 Apps** provider.

    ![Select the HTML5 tile](images/5-select-HTML5.png)

4. You'll see that your `Hello World` app that you've just created in SAP Business Application Studio, already exists in this provider. Select it and click **+ Add to My Content**.

    !![Add app to My Content](images/6-add-hello-world.png)

5. Click the **My Content** tab.

    ![Click My Content](images/7-app-in-my-content.png)

    Note that your `Hello World` app is in the list of content items.


<br>


### Step 3: Create group and assign app to it

In this step, you'll create a new group and assign the `Hello World` app to it.

1. Click **+ New** in the **Content Manager** and select **Group** to create a new group.

    ![Add new group](images/8-add-group.png)

2. Enter `Simple Apps` as the **Title**.

3. In the **Assignments** panel on the right, click in the search box to see a list of apps.

    >If you have many apps, you can type some letters of your app name in the search bar, (for example, `he`) to search for the app.

4. Next to the `Hello World` app, click the **+** icon to assign your app to this group.

    ![Assign app to group](images/9-edit-group.png)

    You'll see that the icon changes.

4. Click **Save**.

    ![Save](images/10-save.png)


<br>

### Step 4: Assign app to Everyone role

In this step, you'll assign the `Hello World` app to the `Everyone` role. This is a default role - content assigned to the `Everyone` role is visible to all users. In addition, the `Everyone` role is by default assigned to every site, so that it is not necessary to assign this role to your site to make its content available.

1. Click the back icon to go back to the **Content Manager**.

    ![Open Content Manager](images/11-back.png)

2. Click the `Everyone` role to open the role editor.

    ![Everyone role](images/12-everyone-role.png)

3. Click **Edit**.

    ![Edit role](images/13-edit-role.png)

4. Click the search box in the **Assignments** panel on the right. Any available apps are shown in the list below.

5. Next to the `Hello World` app, click the **+** icon. You'll see that the icon changes.

6. Click **Save**.

    ![Assign app and save role](images/14-assign-and-save-role.png)

<br>

### Step 5: Review your site

1. Click the **Site Directory** icon to open the Site Directory.

    ![Open site directory](images/15-go-to-site-directory.png)

2. Click the **Go to site** icon on the site tile. The site opens in a new browser tab.

    ![Open site](images/16-go-to-site.png)

    You will see both apps that you have created in your site. In the `Simple Apps` group, you will see the `Hello World` app that you just created.

    ![See all apps](images/17-view-site.png)


3. Click the app to launch it. You see an empty app showing just its title `Hello World`.

    ![View app](images/18-view-app.png)

<br>

## Summary

With this, you have successfully added your SAP Fiori app to your SAP Build Work Zone site.

Continue to - [Exercise 3 - Access your site with SAP Mobile Start](../../ex3/README.md)

