

# Workshop: DevOps with GitHub on Azure

>DevOps is great, if you have the people, processes and tools to support it.  In this session I’ll highlight the easiest ways for developers to work with their IT organizations and partners to deliver their code to the cloud using GitHub, including the best ways to reliably make updates and maintain production cloud code. The focus is on real-world examples using command line tools, free tools including GitHub Actions, and free SDKs and tools available on GitHub. 


## Workshop delivery 
I'm happy to deliver this workshop virtually at destinations worldwide, and also to support anyone else who wants to deliver this, especially in local languages.

### Past deliveries:
 - [4Developers conference, Virtually (CET) October 27, 2020](https://app.evenea.pl/event/4developers2021?smclient=0bfcef4a-99d1-11ea-999e-2841c6acdb70&utm_source=salesmanago&utm_medium=email&utm_campaign=default) 

## Prerequisites
Here are list of free and open source [prerequisites](001_workshop_Prerequisites.md)


# Agenda

## DevOps for Azure

### Introduction

### Exercise – Fork and Clone GitHub repositories for this workshop 

 - (Based on https://lab.github.com/githubtraining/introduction-to-github)
 - Instructions on forking and cloning a repo - https://docs.microsoft.com/en-us/learn/modules/create-a-build-pipeline/3-build-locally
 - Sample App: https://github.com/bbenz/devopswithgithub-TestABAzureDevOPs

 - Fork and clone a main branch
 - Making changes to the local repo
 - Staging
 - Committing

### Exercise – Run and test the local code in VS Code 
 - Opening the local folder 
 - Reviewing the code 
 - Running and testing the code
 - Reviewing VS Code Git/GitHub 
 - Pushing to GitHub
 - Add an Issue

### Azure Basics 
 - Resource Groups
 - Target environments - VMs, App Service, ACI, Kubernetes

### Exercise 
 - Create a resource group
 - Create a staging server
 - Create a production server
 - Create a deployment slot on the production server 
 - Set the deployment slot to 50% traffic
DevOps Introduction

### DevOps Introduction
 - People, process and products
 - Builds 
 - Releases 
 - Infrastructure as code
DevOps with Azure DevOps

### Azure DevOps Introduction 
 - Azure Organizations
 - Azure Projects
 - Boards
 - Repos
 - Pipelines
 - Release Pipelines 
 - Test Plans
 - Artifacts
 - GitHub Extensions

### Exercise – Azure DevOps for CI
 - Connect a repo to an Azure DevOps project using the Azure Pipelines extension in the GitHub marketplace
 - Choose the default build template
 - Replace the default template with a provided template
 - Add and run the customized build template
 - Review hosted agents
 - Review the build log

### Exercise – Azure DevOps for CD 
 - Create a new Release pipeline
	Staging
	Production
	Deployment Slot
 - Set up pre-and post deployment approvals
 - Review automated options
 - Set up CD trigger 
 - Run the release pipeline 
 - Review the release

### Exercise – A/B testing
 - Make a change in GitHub
 - Submit and accept a PR
 - Review the change 
	Build
	Release
	Staging
	Deployment slot
 - Review the changes and function of deployment slots
 - Approve the change – post-deployment approval
 - Approve the change – pre-deployment approval

DevOps with GitHub

### GitHub Actions Introduction (Based on https://docs.microsoft.com/en-us/learn/modules/github-actions-automate-tasks/)
 - Container actions
 - JavaScript actions
 - Workflows
 - Action blocks
 - Triggers
 - Runners
 - Checkin and Checkout
 - Logs
 - Sample App: https://github.com/bbenz/devopswithgithub-TestFeatureFlags
 - Based on: https://docs.microsoft.com/en-us/azure/azure-app-configuration/quickstart-feature-flag-aspnet-core?tabs=core3x

### Exercise (based on https://docs.microsoft.com/en-us/learn/modules/github-actions-cd/)
 - Choose the default build template
 - Replace the default template with a provided template
 - Add and run the customized build template
 - Review the build log


### GitHub Actions for CI (Based on https://docs.microsoft.com/en-us/learn/modules/github-actions-ci/)
 - Using a Template
 - Building
 - Working with Artifacts
 - Testing
 - Automating Reviews

### Exercise (based on  https://lab.github.com/githubtraining/github-actions:-continuous-integration)
 - Create a templated workflow
 - Review the workflow results
 - Review an Actions log
 - Merge the workflow pull request 
 - Customize the GitHub Actions workflow with new build target(s) in Windows
 - Use multiple jobs - separate build and test jobs
 - Upload build artifacts

### Feature Flags
 - Azure App configuration Manager
 - Options for filters
 - Connecting apps to Feature Manager
 - Feature flags in action

### Summary and Review



