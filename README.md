# AD280 - A Beginning to End Workshop on Configuring SAP Launchpad Service

## Description

This repository contains the material for the SAP TechEd 2022 session called Session AD280 - A Beginning to End Workshop on Configuring SAP Launchpad Service.  

## Overview

This session introduces attendees to the creation of SAP Launchpad service site in their free trial account. Attendees will learn how to consume federated content from an SAP S/4HANA systems and how to add a custom developed app to the site. 

## Requirements

This exercise is run in an SAP BTP trial environment. You need to first register to get your own free trial accoount. You can register to a trial account using this link: Create a trial account. Scroll down and click Get trial now.

## Exercises

Provide the exercise content here directly in README.md using [markdown](https://guides.github.com/features/mastering-markdown/) and linking to the specific exercise pages, below is an example.

Before getting started with the exercises, please take a look at the following [general overview of SAP Build Work Zone, standard edition](intro/overview.md).

In the first part of this SAP TechEd workshop, you will create your first site. Before you can do this, you first need to create a subscription to the service on the SAP Business Technology Platform cockpit and assign the administrator role to your user. You will then enter the administration environment to create your first site and add an application to the site. To make the application visible on the site, you will assign it to a group and to a role. Please check the [introduction into the admin environment and the content structure](intro/admin.md) for more details.

- [Exercise 0 - Set up SAP Launchpad service in your trial account](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started.html)
- Exercise 1 - Create your first launchpad site with a URL app
    - [Exercise 1.1 - Create your first site](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-create-sitelaunchpad.html)
    - [Exercise 1.2 - Add an application to your site](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-new-sapui5.html)


The next part of the SAP TechEd workshop is not an exercise for participants, but just a demo, as it requires an SAP S/4HANA system to be available to participants that is connected to the BTP trial subaccount using the SAP Cloud Connector and a destination in SAP BTP and configured for content federation. This goes beyond the scope of this workshop. Instead the content federation and consumption is shown as a demo. Learn more about [content federation](intro/federation.md).

Attendees who would like to run this exercise **after the TechEd workshop**, would need to have administrator access to an SAP S/4HANA 2020 system or higher available, e.g. using an [SAP S/4 HANA Fully Activated Appliance 30-day trial system](https://www.sap.com/products/erp/s4hana/trial.html) from the SAP Cloud Appliance Library. See this [Quick Start Guide](https://www.sap.com/documents/2019/04/4276422b-487d-0010-87a3-c30de2ffd8ff.html#page=1) for more information. Please follow the instructions in this [Enhance Your SAP Launchpad Site with Federated SAP S/4HANA Content tutorial](https://developers.sap.com/mission.launchpad-s4hana.html), but note that not all parts of this tutorial are shown in the demo at the TechEd workshop.

Finally, you will now create your own custom developed app with the Business Application Studio and easily integrate it into your site. To do this, you first need to create a subscription of the Business Application Studio and create a dev space. In the fourth part of this exercise, you will enhance the application. This is optional due to time constraints, as this exercise is not mandatory for the integration of the app into your site, but will show you how easily you can display business content from a real backend system.

- Exercise 2 - Integrate a custom developed SAPUI5 app into your site
    - [Exercise 2.1 - Set Up SAP Business Application Studio for Development](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-create-sitelaunchpad.html)
    - [Exercise 2.2 - Create a Dev Space for SAP Fiori Apps](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-new-sapui5.html)
    - [Exercise 2.3 - Create an SAP Fiori App Using SAP Business Application Studio](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-new-sapui5.html)
        
        This exercise creates a very simple app. If you want to learn how to create an app consuming data from an SAP system, you can also do [this advanced exercise](https://developers.sap.com/tutorials/appstudio-fioriapps-create.html) instead. But note that you would first need to [create an account on the SAP Gateway demo system](https://developers.sap.com/tutorials/gateway-demo-signup.html) and then [connect your BTP trial to it](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-gateway-connection.html). So this will take about 20 minutes longer.
    - [Exercise 2.4 - Optional: Enhance your SAP Fiori App using the Content Editor](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-new-sapui5.html)
    - [Exercise 2.5 - Build and Deploy Your SAP Fiori App to SAP Business Technology Platform](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-new-sapui5.html)
    - [Exercise 2.6 - Integrate Your SAPUI5 App into Your Launchpad Site](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-create-sitelaunchpad.html)


**IMPORTANT**

Your repo must contain the .reuse and LICENSES folder and the License section below. DO NOT REMOVE the section or folders/files. Also, remove all unused template assets(images, folders, etc) from the exercises folder. 

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2022 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
