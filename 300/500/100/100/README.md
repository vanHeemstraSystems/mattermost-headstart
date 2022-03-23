# 100 - Create the Database

Based on "" at https://render.com/docs/deploy-mattermost

Create a new PostgreSQL database on Render.

You’ll need various properties from this database when you’re creating the Mattermost service.

## Step 1 - Go to https://dashboard.render.com/new/database

## Step 2 - Signin / Signup with Render

## Step 3 - Create a new PostgreSQL Database

Go to https://dashboard.render.com/new/database?next=/new/database

Fill in the form:

***New POstgreSQL***

Name: ***mattermost***

Database: randomly generated unless specified (leave blank)

User: randomly generated unless specified (leave blank)

Region: Frankfurt (EU Central)

PostgreSQL Version: 14 (choose latest)

Plan: Starter $7/month, RAM: 256 MB, CPU: shared, STORAGE: 1 GB (as Free plan database will expire in 90 days and will be deleted if not upgraded)

Click ***Create Database***

After a successfull creation of the databse, you will be forwarded to its dedicated web page (here: https://dashboard.render.com/d/dpg-c8te977h8vlc3sq39q9g)

## Info



## Metrics


## Backups


## Logs
