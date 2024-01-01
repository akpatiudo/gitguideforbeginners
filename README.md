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
the build, restore, test and publish of you code will be run as soon as the CI pipeline is configure and trigger, in this project, one artifact was build, this 
can be seen in agent job

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/96700061-432d-4d56-acef-8329f60a244f)

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/54f564d5-f47f-49ac-903d-b1fc69f93fcc)

## Note:

I created a webapp with azure porter and copy the link to a new browser as shown in the pictures below. my code will deploy into this webapp.

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/8e8b82bf-a311-446d-811c-a3917344c999)

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/75a98fe9-b03a-4590-a5d5-44529744608f)

## Step 3: Configuring CD Pipeline
Create a new CD pipeline for deploying to Azure.
Specify the deployment target (e.g., Azure App Service).
Configure release stages and deployment settings.

CD pipeline starts by clicking the release button and setting up the artifacts and staging it, enable the continues deployment trigger as shown below:

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/5c48e28c-ab00-4ec0-bba0-0094eec1032a)

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/93587531-c504-42bc-8681-1297a0c95159)

you can see the red cycle top right of the pictures by task, it shows the configuration is not complete, click on the one job task and chose your subscription, app type and app name. your azure devops should be able to see you azure porter if you setup the connections. once you saved the create release button will be highlighted, click on it.

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/79abf180-9dac-4b18-abd2-3c5953bc214b)

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/ee5f7183-51a7-42d7-bc0b-52aa944068ec)

The next slide shows release one and stage one succeeded, once this is done, go to your browser and refresh it, everything deployed will be shown

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/de9b9814-0b3d-40ff-8b2b-37b9ea7426a3)

## Step 4: Monitoring and Testing

Integrate testing steps within the CI/CD pipeline to ensure code quality.
Set up monitoring and logging for your deployed application.

## Step 5: Triggering Deployments
Commit code changes to your repository and observe the automatic triggering of the CI/CD pipeline.
Monitor the pipeline progress and review logs for any issues.

the next slide shows ux/dx codebase added and pushed to GitHub, the process will trigger automatically based on the configuration, slide two shows the pipeline was ran again and you see the commit updates and time difference, slide three shows deployment was trigger automatically, it succeeded, run on agent succeeded and it was release two. slide four shows what was deployed into the web app when the browser was refresh

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/82055179-6048-4b27-ad13-c9d35c5e6c67)

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/8838d4ad-4b12-434f-b1b5-c753444ac5ab)

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/cb224d28-3634-4464-9047-7d811018ff0d)

![image](https://github.com/akpatiudo/dotnetdevops/assets/118566096/abaff833-b3c0-40b6-807c-51766de34726)

## Conclusion
By following this guide, you've successfully established a robust CI/CD pipeline for your .NET web app using Azure DevOps and Azure Pipelines. This streamlined approach enhances collaboration, accelerates development cycles, and ensures the reliability of your application.


















