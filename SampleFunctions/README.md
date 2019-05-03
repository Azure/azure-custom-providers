# Sample Functions

The examples in this folder contain samples of custom providers along with the azure functions created to back them up. 


# Folder structure

Each folder has the following structure : 

```
    \<FunctionExample>\
                        Readme.md                           // A readme file that explains the function and how it works
                        azuredeploy.json                    // An Azure Resource Template that deploys the function and the custom provider
                        azuredeploy.customresource.json     // An Azure Resource Template that deploys the newly created custom resource.
                        Code\                               // The code required to create the azure function backing the custom provider
                        Artifacts\functionZip\              // the zip file that can be used to deploy the function
                        Artifacts\images\                   // images required to display the readme file
```


# Examples 

Deploy a custom provider with a simple user resource and a ping action : 
+ [** Creating a Custom Provider with resources **](CSharpSimpleProvider/README.md)






