# 100 - Introduction

[Mattermost](https://mattermost.com/) is an open source messaging platform with an easy-to-use and familiar web interface. It is customizable and can run as a simple standalone web server or as a complex, clustered, multi-process service connected to separate database, object storage, LDAP directory, search engine, and mail service, among other things. All of these configurations can be installed on Render.

In this tutorial, you’ll run a Mattermost instance consisting of a Mattermost web service, a PostgreSQL database, and a [MinIO](https://min.io/) object store backed by a [persistent, snapshotted disk](https://render.com/docs/disks).

This is an example repository with multiple Dockerfiles and a render.yaml for running a Mattermost server with disk backed by PostgreSQL and Minio for uploaded artifacts such as images and videos.

We will follow [this guide](https://render.com/docs/deploy-mattermost).
