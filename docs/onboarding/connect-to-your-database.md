---
title: Connect to your database
subtitle: Understand how to connect your application to your PlanetScale database.
date: '2022-09-13'
---

{% vimeo src="https://player.vimeo.com/video/766936973" caption="Connecting to your PlanetScale database" /%}

## Overview

Now that you have your database set up, the next step is to connect it to your application. Most database systems, including PlanetScale, allow applications to connect using connection strings. Connection strings are strings that contain your database credentials and other connection information needed to connect to your database.

In this guide, you’ll learn how to generate a connection string for your application and how branches affect the connection strings.

{% callout %}
This guide continues from the [previous entry](/docs/onboarding/branching-and-deploy-requests) describing how branching & deployments work. Please follow the steps in that guide before proceeding.
{% /callout %}

## Create a connection string

Open the `travel_db` and click the **"Connect"** button.

![The Overview tab of the database with the Connect button highlighted.](/docs/onboarding/connect-to-your-database/the-overview-tab-of-the-database-with-the-connect-button-highlighted.png)

The following modal will provide the information required to connect to your database. If this is your first time accessing the **Connect** modal, the password will be displayed in plain text, otherwise, the password will be masked.

![The Connect to modal.](/docs/onboarding/connect-to-your-database/the-connect-to-modal.png)

If you need to generate a new password, simply click the **"New password"** button to generate a new set of credentials.

![The Connect to modal after the New password button has been clicked.](/docs/onboarding/connect-to-your-database/the-connect-to-modal-after-the-new-password-button-has-been-clicked.png)

If you want a language/framework-specific connection string, you can use the **"Connect with"** dropdown and pick the option that best suits what you are building with.

![The language/framework selector of the Connect modal.](/docs/onboarding/connect-to-your-database/the-language-framework-selector-of-the-connect-modal.png)

Selecting any of these options not only provides the connection string specific to your environment, but also a sample file that can be used in your code. For example, if you select **"Go"** from the list of options, you’ll be provided a sample **.env** file that contains the connection string as well as a **main.go** file that has the necessary code to connect to PlanetScale using that connection string.

![The Connect modal with Go selected.](/docs/onboarding/connect-to-your-database/the-connect-modal-with-go-selected.png)
![The main.go file provided with the connection details.](/docs/onboarding/connect-to-your-database/the-main-go-file-provided-with-the-connection-details.png)

## Branches and connection strings

Connection strings allow your application to securely connect to PlanetScale, but since branches are effectively separate copies of your database, it’s important to know how to generate a connection string for the branch you want to connect to. In the above section, we generated a connection string from the Overview tab of the database. This will create a connection string to the default `main` branch, which is our production database.

When you're working in development, you'll want to connect your dev (local or staging) application to a PlanetScale development branch.

To create a connection string for another branch, simply navigate to the branch, and click the Connect button from the overview tab of that branch. Let's create a connection string for the `dev` branch we created in the previous guide.

Click on **"Branches"**, then select the **"dev"** branch from the list.

![The branches tab.](/docs/onboarding/connect-to-your-database/the-branches-tab.png)

In the Overview tab of the `dev` branch, there is a Connect button. Clicking that button will display the same modal as earlier, but the connection string will be for that specific branch instead of `main`.

![The Connect button of the dev branch.](/docs/onboarding/connect-to-your-database/the-connect-button-of-the-dev-branch.png)

## What's next?

At this point, you should have a good understanding of how to work with and manage databases on PlanetScale, including branching, deployments, and connecting to your database.

Use the resources below to determine next steps for your application.

## Connect your code

Use one of the following quick-starts to get up and running using your preferred language/framework.

{% quickstart-guides /%}

## Import your database

Learn how to import an existing MySQL database from supported cloud providers.

{% import-guides /%}