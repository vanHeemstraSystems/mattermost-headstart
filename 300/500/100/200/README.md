# 200 - Create the MinIO Service

Based on "Create the MinIO Service" at https://render.com/docs/deploy-mattermost

## Step 1: Go [here](https://dashboard.render.com/select-repo?type=pserv) to begin creating a new private service.

You have no connected repositories. Connect your GitHub or GitLab repository to Render.

Alternatively, to use an existing public repository simply enter the URL.

HINT: Connect [this GitHub repository](https://github.com/vanHeemstraSystems/mattermost-headstart/browse) to Render

## Step 2: Use this Mattermost repository.

https://github.com/vanHeemstraSystems/mattermost-headstart/browse

The above repository should have been connected to render in previous step. Select it from [here](https://dashboard.render.com/select-repo?type=pserv).

You are deploying a private service for vanHeemstraSystems/mattermost-headstart.

Name: mattermost

Environment: Docker

Region: Frankfurt (EU Central)

Branch: main

Plans: Starter $7/month, RAM: 512 MB, CPU: 0.5

Under ***Advanced*** add the following:

Dockerfile Path: ./containers/app/minio/Dockerfile

Click ***Create Private Service***

***NOTE***: The deployment may fail, but that is OK for now. In the next step we will add additional requirements taht will make it deploy successfully. 

## Step 3: Add these two environment variables:

Go (again) to [your private Service](https://dashboard.render.com/pserv/srv-c8tf51s41ls5dnacg3m0/deploys/dep-c8tf53441ls5dnacg3og).

In the Advanced section at the bottom of the form, choose to ***[Add Environment Variables](https://dashboard.render.com/pserv/srv-c8tf51s41ls5dnacg3m0/env)***:

KEY: MINIO_ACCESS_KEY

VALUE: Supply your own value or generate it (here we choose to have it generated)

KEY: MINIO_SECRET_KEY

VALUE: Supply your own value or generate it (here we choose to have it generated)

These values will be needed for the Mattermost service later.

Finally, choose to ***Save Changes***.

## Step 4: Add a disk with /data as the mount path.

## Step 5: Set the Docker build context directory to ```./minio``` and the Dockerfile path to ```./minio/Dockerfile```.

## Step 6: Create the service.

