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

Click ***Create Private Service***

***NOTE***: The deployment may fail, but that is OK for now. In the next step we will add additional requirements taht will make it deploy successfully. 

## Step 3: Add these two environment variables:

Go (again) to [your private Service](https://dashboard.render.com/pserv/srv-c8tf51s41ls5dnacg3m0/deploys/dep-c8tf53441ls5dnacg3og).

In the Advanced section at the bottom of the form, choose to ***[Add Environment Variables](https://dashboard.render.com/pserv/srv-c8tf51s41ls5dnacg3m0/env)***:

KEY: MINIO_ROOT_USER (was: MINIO_ACCESS_KEY)

VALUE: Supply your own value or generate it (here we choose to have it generated)

KEY: MINIO_ROOT_PASSWORD (was: MINIO_SECRET_KEY)

VALUE: Supply your own value or generate it (here we choose to have it generated)

These values will be needed for the Mattermost service later.

Finally, choose to ***Save Changes***.

***NOTE***: The deployment may fail still, but that is OK for now. In the next step we will add additional requirements taht will make it deploy successfully.

## Step 4: Add a disk with /data as the mount path.

In [your private service](https://dashboard.render.com/pserv/srv-c8tf51s41ls5dnacg3m0/deploys/dep-c8tf53441ls5dnacg3og) Choose the Disks menu item and click ***Add Disk***.

Name: mattermost

Mount Path: /data

Size: 1 GB (you can increase the size later, but you can't decrease it. Pick the lowest value that works for your app.

Click ***Save***.

## Step 5: Set the Dockerfile path to ```./containers/app/minio/Dockerfile``` and the Docker Build Context Directory to ```./containers/app/minio```.

Under ***Advanced*** add the following:

Dockerfile Path: ./containers/app/minio/Dockerfile

Docker Build Context Directory: ./containers/app/minio

Click ***Create Private Service***

## Step 6: Create the service.

If not done so before (i.e. if you made all above changes at once before creating the private service), click ***Create Private Servcie***

