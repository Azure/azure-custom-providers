# Incorporating swagger into Custom Providers

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-custom-providers%2Fmaster%2FCustomRPWithSwagger%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/> 
</a>


Custom providers provide an excellent way to extend azure ARM capabilities. This extension takes the form of a RESTful endpoint and so it is highly recommended that the API be accompanied by a swagger specification. To learn more about the advantages of specifying swagger and details on how to do it please visit: 
https://swagger.io/specification/ 


# Tools

Following tools can help you with the creation of swagger documents: 

- **Visual Studio Code**
Visual studio code comes with various extensions that can help you with the creation of swagger specifications. Get it here: 
https://code.visualstudio.com/

- **Swagger Doc Viewer VS Code extension**
This is an extension for visual studio code that helps with easy visualization and writing of swagger specifications. More details here. 
https://marketplace.visualstudio.com/items?itemName=mimarec.swagger-doc-viewer 



# How to specify the Swagger during creation of Custom Providers

In the resource deployment section for custom providers, the following section defines the swagger specification: 

```
"Validations" :[
                                {
                                    "ValidationType": "swagger",
                                    "Specification": "https://raw.githubusercontent.com/Azure/azure-custom-providers/master/CustomRPWithSwagger/Artifacts/Swagger/pingaction.json"
                                },
                                {
                                    "ValidationType": "swagger",
                                    "Specification": "https://raw.githubusercontent.com/Azure/azure-custom-providers/master/CustomRPWithSwagger/Artifacts/Swagger/userresource.json"
                                }
                            ]

```

# Swagger File Path requirements 
The swagger file paths specified should be on a public github repository and the links should point to the raw links for the URI. 


# Swagger validations done by the Custom Providers

There are 2 types of validations done by the resource providers for swagger: 

- **Deployment Time validation**
During deployment of the custom resource provider, validation is done to make sure that the swagger file provided is a valid swagger as per specifications 

- **Runtime Validations**
When the calls are being made to the custom resource provider, we will make checks against the swagger specifications to make sure that the endpoint is following the specifications for all calls made. Failure to follow the specifications will be flagged as a violation


Swagger specifications make sure that the API's created for custom providers follow the Open API specifications which makes sure that these  : 
- Are usable 
- Follow Best practices
- Make API modelling easier.







