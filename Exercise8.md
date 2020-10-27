
[Return to Agenda](README.md)
<br/>

## Workshop: DevOps with GitHub on Azure

### Exercise 8 - Generating a template with deployment manager

[Related Materials on Microsoft Docs](https://docs.microsoft.com/en-us/azure/app-service/deploy-github-actions?tabs=applevel)
 
 - Fork and clone the [Feature Flags Sample App](https://github.com/bbenz/devopswithgithub-TestFeatureFlags)
 - Run the app locally in VS Code 
 - Create a new Azure Web App by following the same steps in Exercise 3
 - Deploy to an Azure Web App using the Web App Deployment Center

 - Review the workflow results

 - Set up a connection string to the App Configuration store

 - Restart the application

 - Review the workflow template

## Fork and clone the Feature Flags Sample App
Use the same [Instructions on forking and cloning a repo](https://docs.microsoft.com/en-us/learn/modules/create-a-build-pipeline/) as in Exercise 1

## Run the app locally in VS Code 
There are a few items to set up to make this code connect to the Application configuration store and run:

## Add Secret Manager

A loal tool called Secret Manager stores sensitive data for development work outside of your project tree. This approach helps prevent the accidental sharing of app secrets within source code. Complete the following steps to enable the use of Secret Manager in the ASP.NET Core project:

#### [.NET Core 3.x]

Navigate to the project's root directory, and run the following command to enable secrets storage in the project:

```dotnetcli
dotnet user-secrets init
```

A `UserSecretsId` element containing a GUID is added to the *.csproj* file:

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">
    
    <PropertyGroup>
        <TargetFramework>netcoreapp3.1</TargetFramework>
        <UserSecretsId>79a3edd0-2092-40a2-a04d-dcb46d5ca9ed</UserSecretsId>
    </PropertyGroup>

</Project>
``` 
 ## Connect to an App Configuration store

1. Install the [Microsoft.Azure.AppConfiguration.AspNetCore](https://www.nuget.org/packages/Microsoft.Azure.AppConfiguration.AspNetCore) and [Microsoft.FeatureManagement.AspNetCore](https://www.nuget.org/packages/Microsoft.FeatureManagement.AspNetCore) NuGet packages by running the following commands:

    ```dotnetcli
    dotnet add package Microsoft.Azure.AppConfiguration.AspNetCore
    ```

    ```dotnetcli
    dotnet add package Microsoft.FeatureManagement.AspNetCore
    ```

1. Run the following command in the same directory as the *.csproj* file. The command uses Secret Manager to store a secret named `ConnectionStrings:AppConfig`, which stores the connection string for your App Configuration store. Replace the `<your_connection_string>` placeholder with your App Configuration store's connection string. You can find the connection string under **Access Keys** in the Azure portal.

    ```dotnetcli
    dotnet user-secrets set ConnectionStrings:AppConfig "<your_connection_string>"
    ```

    Secret Manager is used only to test the web app locally. When the app is deployed to [Azure App Service](https://azure.microsoft.com/services/app-service/web), use the **Connection Strings** application setting in App Service instead of Secret Manager to store the connection string.

 ## Create a new Azure Web App
  - Now that the aplpication runs locally, it's time to deploy it to an Azure Web application server.
  - Follow the same steps in Exercise 3 for the staging and production servers.  Use the same resource group and location.  
 
 ## Deploy to an Azure Web App using the Web App Deployment Center
 
You can quickly get started with GitHub Actions by using the App Service Deployment Center. This will automatically generate a workflow file based on your application stack and commit it to your GitHub repository in the correct directory.

1. Navigate to the webapp that you just created in the Azure portal
1. On the left side, click **Deployment Center**
1. Under **Continuous Deployment (CI / CD)**, select **GitHub**
1. Next, select **GitHub Actions**
1. Use the dropdowns to select your GitHub repository, branch, and application stack

1. On the final screen, you can review your selections and preview the workflow file that will be committed to the repository. If the selections are correct, click **Finish**

This will commit the workflow file to the repository. The workflow to build and deploy your app will start immediately.
 
## Review the workflow results
Note that the workflow fails, as we have not yet set up a connection string to the Application Configuration store.  
 
 ## Set up a connection string to the App Configuration store


Select your Web app. In the app's left menu, select **Configuration** > **Application settings**.

![Application Settings](./media/open-ui.png)



Connection strings are always encrypted when stored (encrypted-at-rest).

> [!NOTE]
> Connection strings can also be resolved from [Key Vault](../key-vault/index.yml) using [Key Vault references](app-service-key-vault-references.md).


To add a new connection string, click **New connection string**. 

The name sholud be **AppConfig** and the value should be the connection string from your App Configuration store.

When finished, click **Update**. Don't forget to click **Save** back in the **Configuration** page.
 
The application should restart at this time.  Open the Web Site Address from the overview, and you should see the Web site.  Refresh the app a few times and see if you notice any differences in the menu.





