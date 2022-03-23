# 300 - Create the Mattermost Service

Based on "Create the Mattermost Service" at https://render.com/docs/deploy-mattermost

## Step 1: Go [here](https://dashboard.render.com/select-repo?type=web) to begin creating a new web service.

## Step 2: Use [our mattermost repository](https://github.com/vanHeemstraSystems/mattermost-headstart/browse).

## Step 3: Add the following environment variables:

Go to [the form](https://dashboard.render.com/web/new).

Name: mattermost

Environment: Docker

Region: Frankfurt (EU Central)

Branch: main

Plans: Starter $7/month RAM 512 MB, CPU 0.5

Under ***Advanced***:

Choose ***Add Environment Variable***:

Add the following environment variables:

KEY: MM_SQLSETTINGS_DRIVERNAME

VALUE: postgres
___

KEY: MM_USERNAME

VALUE: The username from the database created earlier (here: )
___

KEY: MM_PASSWORD

VALUE: The password from the database created earlier (here: )
___

KEY: MM_DBNAME

VALUE: The database name from the database created earlier (here: )
___

KEY: DB_HOST

VALUE: The hostname from the database created earlier (here: )
___

KEY: MM_FILESETTINGS_DRIVERNAME	

VALUE: amazons3
___

KEY: MM_FILESETTINGS_AMAZONS3BUCKET

VALUE: mattermost
___

KEY: MM_FILESETTINGS_AMAZONS3ACCESSKEYID

VALUE: The MINIO_ACCESS_KEY from MinIO created earlier
___

KEY: MM_FILESETTINGS_AMAZONS3SECRETACCESSKEY

VALUE: The MINIO_SECRET_KEY from MinIO created earlier
___

KEY: MM_FILESETTINGS_AMAZONS3ENDPOINT

VALUE: The host:port from the MinIO created earlier
___

KEY: MM_FILESETTINGS_AMAZONS3SSL	

VALUE: false
___

## Step 4: Add a disk with ```/mattermost/config``` as the mount path.

## Step 5: Set the Docker build context directory to ```./containers/app/app``` and the Dockerfile path to ```./containers/app/app/Dockerfile```.

## Step 6: Create the service.

Your Mattermost cluster should be ready to use with regular backups and disk snapshots!
