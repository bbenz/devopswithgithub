
[Return to Agenda](README.md)
<br/>

## Workshop: DevOps with GitHub on Azure


### Exercise 5 – Azure DevOps for CD 
 - Create a new Release pipeline
	Staging
	Production
	Deployment Slot
 - Set up pre-and post deployment approvals
 - Review automated options
 - Set up CD trigger 
 - Run the release pipeline 
 - Review the release

 Now that the build pipeline is complete, we can turn our attention to creating a release pipeline. 
 
 >Like the build templates, there are many packaged options available that cover common deployment scenarios, such as publishing to Azure. 

1.  From the left hand menu, under **Pipelines** click **Releases**. Click **New Pipeline** to create a new CD pipeline to deploy the artifacts produced by the build.

    ![](media/image13.png)

1.  Click **Empty job**.

    ![](media/image14.png)

    The first item to define in a release pipeline is exactly what will be released and when. In our case, it's the output
    generated from the build pipeline. Note that we could also assign a
    schedule, such as if we wanted to release the latest build every
    night.

1.  Select the associated artifact. 

    ![](media/image15-1.png)

1.  Set **Source** to the build pipeline created earlier and **Default
    version** to **Latest** and click **Add**. 

    ![](media/image16.png)

    As we did with continuous integration starting on a source commit, we also want to have this pipeline automatically start when the build pipeline completes. It's just as easy.

1.  Click the **Triggers** button on the artifact.

    ![](media/image17.png)

1.  **Enable** continuous deployment, if it is not already enabled.

    ![](media/image18.png)

   
    > Just like the build pipeline, the release pipeline is really just a set of tasks. There are many out-of-the-box tasks available, and you can build your own if needed. The first task our release requires is to set up the Azure deployment environment if it doesn't yet exist. After we add the task, I can authorize access to the Azure account I want to deploy
    to and instruct it to use the variable name we just specified for the resource group name.


1. Click the **Add task** button.

    ![](media/image24.png)

   Search for **"app service"** and **Add** an **Azure App Service
    Deploy** task.

    ![](media/image36.png)

1. Select the newly created task.

    ![](media/image37.png)

1. Select the same subscription as earlier.


1. Enter the **App Service name** of your **Staging Server**.
1. Name this task **Staging**
1. Clone this task using the **Clone** button below the task
1. Rename the new task **Production**
1. Change the **App Service name** to your **Production Server**
1. Clone the **Production** task using the **Clone** button 
1. Rename the task in the middle **Canary**
1. Click on the middle **Canary** task, then on the **Azure App Service Deploy** subtask. 
1. Inside the subtask, choose **Deployment Slot**.  Set the deployment slot to **Canary** inside your **Production Server**.
1. **Save** the pipeline.
1. Select **+ Release** and then select **Create a Release** 
    
1. Select **Create** to start a new release. 

1. Navigate to the release summary by clicking on the **Release-1** link that appears. Click **In progress** to follow the release process.
    
1. Note that it will take a few minutes for the app to finish deploying due to heavy first-time operations. 

    
1. Select the **App Service Deploy** task to view the detailed log. You should find the URL to the published website here. **Ctrl+Click** the link to open it in a separate tab.
