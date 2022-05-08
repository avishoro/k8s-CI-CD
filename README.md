
## Week 10 Project

## Azure DevOps

Clone the repository.
Follow these steps before creating the pipeline:
1. Follow https://kubernetes.io/docs/tasks/tools/ to install `kubectl' on your agent.<br/>
1. Follow https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt to install Azure CLI on LINUX.<br/>
1. Follow https://docs.microsoft.com/en-us/cli/azure/authenticate-azure-cli to login to Azure CLI.<br/>



Create an environment and connect it with AKS cluster.



Go to `Project settings` and create new service connection for Azure Container Registry.

Create new variable group in the library with your secrets.























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
