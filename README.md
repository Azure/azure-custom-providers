# Developing Custom Providers
Collection of ARM templates and resources to get started with developing custom resource providers in ARM 


# About Custom Providers

Custom Providers gives publishers in Azure a way to extend azure and azure resources. They allow users to define resources and actions and have them behave as ARM resources and actions allowing features such as ARM template deployment of non-Azure resources, Integration of 3rd party tools and features as part of the template deployment and RBAC on these resources.

The customProviders resource providers also enables users to add actions and resources to managed apps to enable functionality on the managed apps to run programmatic commands on them.

# Usage

### Deploy To Azure
Each template file has an option to deploy to azure in the Readme.md file present at the the root of the folder


# Getting Started

Deploy a custom provider with a simple user resource and a ping action : 
+ [** Creating a Custom Provider with resources **](CustomRPWithFunction/README.md)

The above Custom resource provider is backed by an azure function app. You can read about how to create this function and update it in the following sample. Deploy the function app and understand the requirements for the api that backs the custom provider :
+ [** Creating an azure function **](/SampleFunction/CSharpSimpleProvider/README.md)

Please check out the othe examples of how you can use custom providers in the Sample functions folder:
+ [** Sample Functions**](/SampleFunction/README.md)

It is recommended to supply a swagger spec for custom providers when deploying them. 
To learm more about swagger and how to incorporate validation for custom providers:
+ [** Incorporating swagger into Custom Providers **](CustomRPWithSwagger/README.md)


# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
