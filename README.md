# az-app-insight-integration

From AD Group, create a new app registration using App Registration 

From App Registration created newly, create a secret from the "Certificates&secret section 

Copy the new client secret value. You won't be able to retrieve it after you perform another operation or leave this blade. 

Go to the keyvault and identify the url for your target keyvault ( This has to be added in your properties file) 

Now let the Keyvault know that the app registrated in step #1 can access the keyvault. 

Add Access Policy and select appropriate permission for your secret ( For example, GET,LIST if you only want the secrets read by your application) 

SElect principal and filter your app registration name and select.  

Select Add button 

Please click the 'Save' button to commit your changes.  

 

Application.properties file sample 

 

 

azure.keyvault.client-id=<App-registration-id> 

azure.keyvault.enabled=true 
azure.keyvault.tenant-id=<tenant-id-this-is-available-in-your-AD-group> 
azure.keyvault.uri=<uri-to-your-keyvault> 
azure.keyvault.token-acquire-timeout-seconds=60 
