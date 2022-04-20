
## Week 8 Project

# CI/CD with Docker

__Configure CI/CD pipelines to deploy the Node Weight Tracker application for 2 environments: Staging and Production.__

- __ __IaC with Terraform- Provisioning of two identical environments  : [ansible project](https://github.com/avishoro/ansible) .__

Project environment:
![week-6-envs](https://user-images.githubusercontent.com/90269123/138599669-1a2ac0cb-9e71-4100-a3a7-eb1d9d0c2afa.jpg)

create a new pipeline selected your project repository and then selected a Docker template to connect your Azure Container Registry with the pipeline.
![image](https://user-images.githubusercontent.com/93486933/164212012-c8605f61-b932-4e7b-bca2-ce29b0d59ca2.png)

use 2 environments (staging / prod) with their resources to target the deployments from the pipline.
![image](https://user-images.githubusercontent.com/93486933/164212197-dc9a9f8b-64e6-4198-895c-da8bca3e7202.png)

![image](https://user-images.githubusercontent.com/93486933/164213300-59bb1c89-4d1c-465a-bd30-e4fd6b62d893.png)

## Continuous Integration

When there is any change in the feature branch the CI process builds a Docker Image.

__Only__ when a feature branch integrated to the master branch the CI process get back into action and in addition to building a new image pushes the image to the Azure Container Registry.


## Continuous Deployment and Continuous Delivery

The continuous deployment and continuous delivery pipelines are similar except that the continuous delivery requires manual approval.

Once a change pushed to the master branch the CD pipelines stops and deletes the old container and then starting running a new one by __pulling the latest image from the Azure Container Registry__.

The `run` command is executed with the environment variables passed to it directly from the variable group in the library.

example for var library:
![image](https://user-images.githubusercontent.com/93486933/164212895-e1a57b91-3052-4359-a57c-5b8b0338251e.png)




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
