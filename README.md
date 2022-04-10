
## Week 7 Project

# CI/CD with Azure DevOps

__Configure CI/CD pipelines to deploy the Node Weight Tracker application for 2 environments: Staging and Production.__

- __IaC with Terraform- Provisioning of two identical environments, and Configuration Management with Ansible - Installing all the dependencies and deploying the application for the first time on the remote machine : [ansible project](https://github.com/avishoro/ansible) .__

Project environment:
![week-6-envs](https://user-images.githubusercontent.com/90269123/138599669-1a2ac0cb-9e71-4100-a3a7-eb1d9d0c2afa.jpg)

## Continuous Integration
The YAML `azure-CI.yml` responsible for the CI pipeline.

__steps:__

1. Install npm in the source directory.

1. Copy the files to the artifacts directory.

1. Publish it to Azure DevOps artifacts.

## Continuous Deployment and Continuous Delivery
For the CI/CD I've created a pipeline which using Ansible to deploy the artifacts to the environments.
![image](https://user-images.githubusercontent.com/93486933/162642955-e67b186d-f1a5-43e4-bb13-a774c0403ef5.png)




**Stages Configuration:**

The Staging deployment stage is fully automatic and is triggered when there is a new artifact of Bootcamp Application.


![image](https://user-images.githubusercontent.com/93486933/162643058-7c9fdeef-787d-414b-bad0-fe2e82a58545.png)

The Production deployment stage is activated when a user with permissions approves the deployment after a successful deployment in the Staging environment.
In addition, the artifact that are deployed on the environment are exactly the same as the files that were deployed in the previous stage.

add two variables groups, one for the staging and one for the production.
![image](https://user-images.githubusercontent.com/93486933/162643151-776999a0-a9a5-43fb-afd5-e2cbc8bd996c.png)
example for vaiables group:
![image](https://user-images.githubusercontent.com/93486933/162643179-ad2a4917-af78-4ac6-8894-056068e17e7a.png)

match each variable group to the correct stage:
![image](https://user-images.githubusercontent.com/93486933/162643225-7f43e854-fea4-4fbc-b73b-15067c788543.png)


# Node.js Weight Tracker

![Demo](docs/build-weight-tracker-app-demo.gif)

This sample application demonstrates the following technologies.

* [hapi](https://hapi.dev) - a wonderful Node.js application framework
* [PostgreSQL](https://www.postgresql.org/) - a popular relational database
* [Postgres](https://github.com/porsager/postgres) - a new PostgreSQL client for Node.js
* [Vue.js](https://vuejs.org/) - a popular front-end library
* [Bulma](https://bulma.io/) - a great CSS framework based on Flexbox
* [EJS](https://ejs.co/) - a great template library for server-side HTML templates

**Requirements:**

* [Node.js](https://nodejs.org/) 14.x
* [PostgreSQL](https://www.postgresql.org/) (can be installed locally using Docker)
* [Free Okta developer account](https://developer.okta.com/) for account registration, login

## Install and Configuration

1. Clone or download source files
1. Run `npm install` to install dependencies
1. If you don't already have PostgreSQL, set up using Docker
1. Create a [free Okta developer account](https://developer.okta.com/) and add a web application for this app
1. Copy `.env.sample` to `.env` and change the `OKTA_*` values to your application
1. Initialize the PostgreSQL database by running `npm run initdb`
1. Run `npm run dev` to start Node.js

The associated blog post goes into more detail on how to set up PostgreSQL with Docker and how to configure your Okta account.
