# Create a Azure Blob Storage account with a blob service and queue service

`dotnet-aspire-connect-storage` is a demo project that shows how to create an Azure storage account using the [Azure Developer CLI](https://learn.microsoft.com/en-us/azure/developer/azure-developer-cli/overview)(azd), and how to connect to the storage account locally using a console application to perform essential tasks.

## Prerequisites

The following prerequisites are required to use this application.  Please ensure that you have them all installed locally.

- [Azure Developer CLI](https://aka.ms/azure-dev/install)
  - Windows:

    ```powershell
    winget install microsoft.azd
    ```

  - Linux/MacOS:

    ```bash
    curl -fsSL https://aka.ms/install-azd.sh | bash 
    ```

  - Mac:
  
      ```bash
      brew tap azure/azd && brew install azd
      ```  

### Quickstart

The fastest way for you to get run this template and provision resources on Azure is to use the `azd up` command. This single command will create and configure all necessary Azure resources.

> Notes: you can run the project in your local environment or [DevContainer](https://code.visualstudio.com/docs/devcontainers/containers).

1. Run the following commands to initialize the project, provision Azure resources, and deploy the application code.

    ```bash
    # Download the repo assets from GitHub and initialize azd locally
    azd init --template dotnet-aspire-connect-storage
    
    # Login to azure
    azd auth login
    
    # Provision and deploy to Azure
    azd up
    ```

2. You will be prompted for the following information:

    - `Environment Name`: This will be used as a prefix for all your Azure resources, make sure it is globally unique and under 15 characters.
    - `Azure Subscription`: The Azure Subscription where your resources will be deployed.
    - `Azure Location`: The Azure location where your resources will be deployed

    The command creates a storage account in Azure for you to use. Click on the link in the console output to view the resource group in Azure.

### Clean up resources

In the preceding steps, you created Azure resources in a resource group. If you don't expect to need these resources in the future, delete the resource group by running the following command:

```bash
azd down
```

### Additional azd commands

The Azure Developer CLI includes many other commands to help with your Azure development experience. You can view these commands at the terminal by running `azd help`. You can also view the full list of commands on our [Azure Developer CLI command](https://aka.ms/azure-dev/ref) page.