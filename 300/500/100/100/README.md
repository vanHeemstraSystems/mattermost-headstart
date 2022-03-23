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

Name: mattermost

Created: 27 minutes ago

Status: Available

PostgreSQL Version: 14

Region: Frankfurt (EU Central)

Plan: Starter

Read Replica: Add Read Replica

Storage: Unavailable

Hostname: dpg-c8te977h8vlc3sq39q9g

Port: 5432

Database: mattermost_xic8

Username: mattermost_xic8_user

Password: ***** (accessible when logged in)

Internal Connection String: ***** (accessible when logged in)

Connecting from outside of the cluster

External Connection String: ***** (accessible when logged in)

PSQL command: ***** (accessible when logged in)

Access Control

Only the following sources (in CIDR block notation) are allowed access to your database from outside of your private network.

Source: 0.0.0.0/0

Description: everywhere

## Metrics


## Backups


## Logs
