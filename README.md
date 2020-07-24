# fass

# Django-APP-Project

django is a Python framework that follows model-template-view architecturl pattern.

## Prerequisites for building and deploying your application locally.

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install django.

```bash
pip install django

```

## Set Up Database

To set up the database.

```bash
python manage.py migrate
```

## Run
Use following command to run the server and access the site.
```bash
python manage.py runserver
```

## Requirement

python version 3

## Build and Deploy instructions for web application on AWS EC2 instance .
create code deployment agent for the instance on which deployment is to performed.

create code deployment group attached to the code deployment agent.

setup a circle ci project to trigger the the web application .

set up circle ci config file to send the web app to code deployment agent in aws .

code deployment agent will deploy the web app to the instance.

## Steps to perform code deployment using terraform

step-1:- bulid the AMI for the instance using curl command
```bash
curl -u account number of circleci \-d build_parameters[CIRCLE_JOB]=build \link of the git AMI repository 
```

step-2: Build the infrastructure i.e terraform 
```bash
terraform apply
```

step-3:- after applying terraform deploy the web app code to circle ci using curl command
```bash
curl -u account number of circleci \-d build_parameters[CIRCLE_JOB]=build \link of the git Web-app repository
```