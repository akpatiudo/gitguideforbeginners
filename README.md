# Mastering .NET Web App Deployment: A Comprehensive Guide with Azure DevOps and Azure Pipelines
## Introduction

Building and deploying a .NET web app can be a straightforward process when leveraging the aptitudes of Azure DevOps and Azure Pipelines. This guide will walk you through the essential steps to set up a continuous integration (CI) and continuous deployment (CD) pipeline for your .NET web application.

## Prerequisites
Before you begin, ensure that you have the following:
A .NET web application codebase hosted on a version control system (e.g., GitHub).
An Azure DevOps account with the necessary permissions to create pipelines.
Basic knowledge of .NET Core and Azure DevOps concepts.

I leveraged on the capabilities of Visual Studio Code to set up a .Net web app codebase and pushed my generated code to Githhub. These were the code lines used to generate my codebase  
1)	Dotnet new mvc -n DotNetWebApp, this will create a .Net web app template
2)	Dotnet restore, this will check if project is up to date and what needs to be restored
3)	Dotnet Build, builds the version and check if it is up to date
4)	Dotnet Publish, this will create and assemble all the files needed for the project
5)	Dotnet Test, this will test if everything is UpToDate and in “health”

The index.cshtlm file in Home folder was updated as shown in pics one and two, saved and pushed into GitHub repository

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/0fd374a3-a834-4800-a406-d1b90a302e05)

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/5a5dff68-7ffe-441c-a716-164eb1c885fa)

Let’s jump into the project:

## Step 1: Setting Up Azure DevOps Project
Create a new project in Azure DevOps to host your CI/CD pipelines.
Configure the project settings and connect it to your version control repository.

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/7c0f458a-8a16-4abd-894b-a649f46106dd)

## Step 2: Configuring CI Pipeline

Create a new CI pipeline in Azure DevOps.
Configure the pipeline to trigger on code changes.
Specify build steps, including restoring dependencies, building the solution, and running tests.

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/96700061-432d-4d56-acef-8329f60a244f)

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/54f564d5-f47f-49ac-903d-b1fc69f93fcc)









