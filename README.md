

# Workshop: DevOps with GitHub on Azure

>DevOps is great, if you have the people, processes and tools to support it.  In this session I’ll highlight the easiest ways for developers to work with their IT organizations and partners to deliver their code to the cloud using GitHub, including the best ways to reliably make updates and maintain production cloud code. The focus is on real-world examples using command line tools, free tools including GitHub Actions, and free SDKs and tools available on GitHub. 


## Workshop delivery 
I'm happy to deliver this workshop virtually at destinations worldwide, and also to support anyone else who wants to deliver this, especially in local languages.

### Next workshop: 
December 14, 15, and 16 11AM PST-12:30PM PST (3 days, 90 minutes per day)

[View the workshop on Learn TV](https://07f.ca/learntv)

### Past deliveries:
 - [4Developers conference, Virtually (CET) October 27, 2020](https://app.evenea.pl/event/4developers2021?smclient=0bfcef4a-99d1-11ea-999e-2841c6acdb70&utm_source=salesmanago&utm_medium=email&utm_campaign=default) 

## Prerequisites
Here are list of free and open source [prerequisites](001_workshop_Prerequisites.md)


# Agenda

## DevOps with Azure

### Introduction

### Exercise 1 – Fork and Clone GitHub repositories for this workshop 
[Go To Exercise](Exercise1.md)
 - Fork and clone a main branch
 - Making changes to the local repo
 - Staging
 - Committing

### Exercise 2 – Run and test the local code in VS Code 
[Go To Exercise](Exercise2.md)
 - Opening the local folder 
 - Reviewing the code 
 - Running and testing the code
 - Reviewing VS Code Git/GitHub 
 - Pushing to GitHub

### Azure Basics 
 - Resource Groups
 - Target environments - VMs, App Service, ACI, Kubernetes

### Exercise 3 - Set up Azure for this workshop
[Go To Exercise](Exercise3.md)
 - Create a resource group
 - Create a staging server
 - Create a production server
 - Create a deployment slot on the production server 
 - Set the deployment slot to 50% traffic

### DevOps Introduction
 - People, process and products
 - Builds 
 - Releases 
 - Infrastructure as code

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

### Exercise – 4 - Azure DevOps for CI
[Go To Exercise](Exercise4.md)
 - Connect a repo to an Azure DevOps project using the Azure Pipelines extension in the GitHub marketplace
 - Choose the default build template
 - Replace the default template with a provided template
 - Add and run the customized build template
 - Review hosted agents
 - Review the build log

### Exercise 5 – Azure DevOps for CD 
[Go To Exercise](Exercise5.md)
 - Create a new Release pipeline
	Staging
	Production
	Deployment Slot
 - Set up pre-and post deployment approvals
 - Review automated options
 - Set up CD trigger 
 - Run the release pipeline 
 - Review the release

### Exercise 6 - A/B testing
[Go To Exercise](Exercise6.md)
 - Make a change in GitHub
 - Commit and Push
 - Review the change 
	Build
	Release
	Staging
	Deployment slot
 - Review the changes and function of deployment slots
 - Approve the change – post-deployment approval
 - Approve the change – pre-deployment approval

## DevOps with GitHub

### GitHub Actions Introduction 
[Related materials on Microsoft Learn ](https://docs.microsoft.com/learn/modules/github-actions-automate-tasks/?WT.mc_id=java-0000-bbenz)

[Related Materials on Microsoft Docs](https://docs.microsoft.com/azure/azure-app-configuration/quickstart-feature-flag-aspnet-core?tabs=core3x&WT.mc_id=java-0000-bbenz)
 - Workflows
 - Action blocks
 - Triggers
 - Runners
 - Checkin and Checkout
 - Logs

### GitHub Actions for CI and CD 
 [Related materials on Microsoft Learn ](https://docs.microsoft.com/learn/modules/github-actions-ci/?WT.mc_id=java-0000-bbenz)
 - Using a Template
 - Building
 - Working with Artifacts
 - Testing
 - Automating Reviews
  
 ### Feature Flags
 - Azure App configuration Manager
 - Options for filters
 - Connecting apps to Feature Manager
 - Feature flags in action

### Exercise 7 - Setting up feature flags in Azure app Configuration Manager 
[Go To Exercise](Exercise7.md)

 [Related Materials on Microsoft Docs](https://docs.microsoft.com/azure/azure-app-configuration/quickstart-feature-flag-aspnet-core?tabs=core3x&WT.mc_id=java-0000-bbenz)
 - Create an App Configuration Store
 
 - Add a feature Manager
 - Set the percentage filter

### Exercise 8 - Generating a template with deployment manager
[Go To Exercise](Exercise8.md)

 - Deploy to an Azure Web App using the Web App Deployment Center
 - Review the workflow results
 - Set up a connection string to the App Configuration store
 - Restart the application 
- Review the workflow template

### Summary and Review



