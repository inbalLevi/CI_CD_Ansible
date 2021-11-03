# CI_CD_Ansible  <img src="https://avatars.githubusercontent.com/u/1507452?s=200&v=4" width="60" height="60"/>  


This playbook will create and provision all web servers within the network with the weight tracker app

https://developer.okta.com/blog/2020/06/01/node-postgres-weight-tracker

# steps:

* Install ansible on ubuntu 18.04 with the commands in this site: https://www.linuxtechi.com/how-to-install-ansible-on-ubuntu/
* Create ssh key and copy to remote machine by this command: ssh-keygen
* Configure remote machine to enable ansible to run it.
* Edit the hosts file: /etc/hosts and /etc/ansible/hosts
* Run a test to verify a connection exists with managed hosts
* Create 2 groups and a group of groups
* Verify connection
* Create a new playbook - mkdir playbook -> nano staging.yml/prod.yml
* Paste definition
* Run command to verify syntax
* in .env creation you should fill your detailes according to OKTA, POSTGRESQL, and IP ADDRESS HOST.
* Run playbook : ansible-playbook staging.yml /prod.yml
* you can add few flags for debugging: </br>

this command will show debugging output ansible-playbook -i hosts <location of the hosts> <location of playbook> -u <username> -vvv

this command will ask you to confirm each step ansible-playbook -i hosts <location of the hosts> <location of playbook> -u <username> --step

this command will start the playbook on the requested task name ansible-playbook -i hosts <location of the hosts> <location of playbook> -u <username> --start-at-task:"<name of the task>"



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

* [Node.js](https://nodejs.org/) 12.x or higher
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

