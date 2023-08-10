# azure-functions-dapr-aca-deployment
This repo contains bicep script to deploye a Dotnet Azure Function with Dapr extension, currently it has below dapr building blocks.

1. Dapr Service Invocation Trigger
2. Dapr Invoke output binding
3. Dapr state output binding
4. Dapr state input binding

How to execute these Azure functions:

1. Once you run the bicep, you will get Azure Function URL in the Azure Portal, copy the URL and replace it in the postman, also make sure to replace the function name in the url
2. Now to create an entry in Redis, hit the Http Post call in Postman, this should return 200 OK
3. Once entry is created, you can read the same data using Dapr state input binding. To do this, execute the Http get call, this should return the value you created in http post call.
