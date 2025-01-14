---
title: 'Web console'
subtitle: 'Query your database directly from the PlanetScale UI'
date: '2022-08-09'
---

## Overview

The PlanetScale web console is an interactive interface for running MySQL queries and DDL (Create, Alter, and Delete) against your PlanetScale database branches.

## Get started

The PlanetScale web console can be used to query to any database branch; however, it is [disabled for production branches](/docs/concepts/web-console#enable-for-production-branches) by default to prevent accidental data loss.

To access the web console, navigate to any web console enabled database branch and click on the Console tab in the database navigation.

![Console tab](/docs/concepts/web-console/tab.png)

You can also access the web console directly by adding `/console` to the URL from any databases branch page,
`app.planetscale.com/<org>/<database>/<branch>/console`.

Once you have accessed the web console, you can run queries against your database branch, or apply DDL to non-production branches.

The following are examples of MySQL statements you may find useful within the web console.

Use `SHOW TABLES;` to see a list of the tables in your database branch.

![SHOW TABLES; in the console](/docs/concepts/web-console/show.png)

Use `DESCRIBE table_name;` to obtain information about a given table's structure.

![DESCRIBE table_name; in the console](/docs/concepts/web-console/describe.png)

Use `EXPLAIN` in front of `SELECT`, `DELETE`, `INSERT`, `REPLACE` and `UPDATES` statements to learn how the database is executing a query. This can be useful for optimizing slow queries.

## Supported console commands

| Command   | Description                       |
| --------- | --------------------------------- |
| ?, \\?    | Synonym for `help`                |
| clear, \c | Clear the current input statement |
| help, \h  | Display list of commands          |
| ego, \G   | Send command to server            |
| go, \g    | Send command to server            |

## Enable for production branches

By default, the web console is disabled for production branches to prevent accidental data loss.

You can enable the web console for production branches in the settings page for the given database,
`app.planetscale.com/<org>/<database>/settings`.

Select the checkbox for "Production branch web console access". Then click the "Save database settings" button to save your changes.

![Enable product branch web console access](/docs/concepts/web-console/production.png)

This will enable the ability to use the web console to run queries against production branches for the given database.
