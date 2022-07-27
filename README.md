# Docker_CI-CD

## Project Overview:

watch a short intro for this project:
https://www.youtube.com/watch?v=nLIFdDiyX7s

# How to use this repository?
- connect files preferably to Azure Devops (you can also use a private github repo)
- open up a new pipeline, the azure-pipelines.yml file will gets picked up automatically.
if not, make sure it does.
- in the pipeline section go over to library and add 2 variable groups:
+ staging
+ production
for each group add the following key value vars:
* PORT=""
* HOST=""
* NODE_ENV=""
* HOST_URL=""
* COOKIE_ENCRYPT_PWD=""
* OKTA_ORG_URL=""
* OKTA_CLIENT_ID=""
* OKTA_CLIENT_SECRET=""
* PGHOST=""
* PGUSERNAME=""
* PGDATABASE=""
* PGPASSWORD=""
* PGPORT=""


<p>
<img src="https://img.shields.io/badge/Terraform-starter-lightgrey" height="25">
<img src="https://img.shields.io/badge/azure-devops-yellowgreen" height="25">
<img src="https://img.shields.io/badge/docker-pro-green" height="25">

my Devops journey (hand drawn by me) :

<center><img src="https://raw.githubusercontent.com/johnmogi/password/main/my_devops.jpg" height="400"></center>

This week’s project consists on writing a Dockerfile to package the NodeWeightTracker application

**Weight Tracker application into a Docker Container on a load balancer spinning staging and production virtual machines with <b>full CI CD automation.</b>**
</br>

<p>
<img src="https://bootcamp.rhinops.io/images/docker-cicd.png" height="300">
<img src="https://bootcamp.rhinops.io/images/branch-policy.png" height="300">
<br/>
## The Necessary Steps

- **Terraform- build 2 enviroments, load balance and postgres db : [preview](https://github.com/johnmogi/CICD_pipeline1_terraform_build) .**

- **NodeWeightTracker - a demo nodejs app from Okta [preview](https://github.com/johnmogi/bootcamp-app) .**

Terraform >> azure cloud >> azure devops >> docker >> docker-compose
A CI/CD process to automate the deployment.
best practices - practice of Pipeline as Code.

after stabilizing Terraform template, using modules for the virtual machines, and using modules for the postgres db we proceed to deploy the application.

![docker-envs](https://bootcamp.rhinops.io/images/docker-envs.png)

merge a feature branch into main to make a production push

![feature-branch](https://bootcamp.rhinops.io/images/feature-branch.png)

# pipeline: Using multi Stages Pipeline

1. the ci cd process start when the project is commited to master.
2. continous integration - the pipeline will run, but in order to deploy to production, we need to merge the feature branch into master.
   - approve the pull request
   - merge the feature branch into master

# feature branch merge instruction

1. create a new branch
2. commit changes to the branch
3. push the branch to the remote
4. open a pull request
5. approve the pull request

make sure you update the correct values in the azure devops library:

- staging - the host url should contain a new ip
- staging - the postgres db name - look it up in the azure portal.
- production - the host url should contain a new ip
- production - the postgres db name - look it up in the azure portal.

will run over the required steps tp install application configuration over your server fleet.
I hope you enjoy the experience.

renamed master to main then back again (:
# Docker_CI-CD
