
[Return to Agenda](README.md)
<br/>

## Workshop: DevOps with GitHub on Azure

### Exercise 7 - Setting up feature flags in Azure app Configuration Manager 




 - https://docs.microsoft.com/en-us/azure/azure-app-configuration/quickstart-feature-flag-aspnet-core?tabs=core3x
 - Create an App Configuration Store
 - Add a feature Manager
 - Set the percentage filter


1. To create a new App Configuration store, sign in to the [Azure portal](https://portal.azure.com). In the upper-left corner of the home page, select **Create a resource**. In the **Search the Marketplace** box, enter *App Configuration* and select <kbd>Enter</kbd>.

    ![Search for App Configuration](media/azure-portal-search.png)

1. Select **App Configuration** from the search results, and then select **Create**.

    ![Select Create](media/azure-portal-app-configuration-create.png)

1. On the **Create App Configuration** pane, enter the following settings:

    | Setting | Suggested value | Description |
    |---|---|---|
    | **Subscription** | Your subscription | Select the Azure subscription that you used for the rest of the workshop. |
    | **Resource group** | *Workshop resource Group* | Use the same workshop resource group for your App Configuration store resource. |
    | **Resource name** | Globally unique name | Enter a unique resource name to use for the App Configuration store resource. The name must be a string between 5 and 50 characters and contain only numbers, letters, and the `-` character. The name can't start or end with the `-` character. |
    | **Location** | *Workshop location* | Use the same  workshop location as the other components of your application. |
    | **Pricing tier** | *Free* | Select the desired pricing tier. For more information, see the [App Configuration pricing page](https://azure.microsoft.com/pricing/details/app-configuration). |

1. Select **Review + create** to validate your settings.

1. Select **Create**. The deployment might take a few minutes.

1. After the deployment finishes, navigate to the App Configuration resource. Select **Settings** > **Access keys**. Find the primary read-only key connection string. You'll use this connection string later to configure your application to communicate with the App Configuration store that you created.

1. Select **Operations** > **Feature manager** > **Add** to add a feature flag called *Beta*.

     > ![Enable feature flag named Beta](media/add-beta-feature-flag.png)

    Leave **Label** empty for now. Select **Apply** to save the new feature flag.

1. Click on the ellipsis on the right, and select **Advanced Edit**.  Paste this in to the dialog and Select **Apply** to save the new feature flag:

```dotnetcli 
{
	"id": "Beta",
	"description": "",
	"enabled": true,
	"conditions": {
		"client_filters": [
			{
				"name": "Microsoft.Percentage",
				"parameters": {
					"Value": 50
				}
			}
		]
	}
}
```

This sets up a feature flag with the percentage filter, meaning 50% of users will see a new feature and 50% of users will not.  



