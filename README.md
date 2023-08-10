# azure-functions-dapr-aca-deployment
This repo contains bicep script to deploye a Dotnet Azure Function with Dapr extension in ACA.

Bicep script will create below resources in Azure.

1. Azure Storage Account
2. App Insights
3. ACA managed environment
4. Azure Redis cache
5. Azure Function App

Currently Azure Function sample has below dapr bindings and triggers.

1. Dapr service invocation trigger
2. Dapr invoke output binding
3. Dapr state output binding
4. Dapr state input binding

# How to execute these Azure functions:

1. Once you run the bicep, you will get Azure Function URL in the Azure Portal, copy the URL and replace it in the postman, also make sure to replace the function name in the url
2. Now to create an entry in Redis, hit the Http Post call in Postman, this should return 200 OK
3. Once entry is created in Redis, you can read the same data using Dapr state input binding. To do this, execute the Http get call, this should return the value you created in http post call.
