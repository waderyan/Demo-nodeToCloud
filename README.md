# Node to Cloud

# Stage 3 - Azure

**Intro**

This stage shows you some tools for bringing your application to life on the web. 

There are many ways of doing this (see [Heroku](https://www.heroku.com/), [Google App Engine](https://cloud.google.com/appengine/docs)). Today we
are going to use Azure Web Apps. 
 
**Install Azure Tools**

Azure CLI allows you to interact with Azure via the command line. 

`$ npm install azure-cli -g`

**Setup Azure Subscription**

You can set up an Azure subscription for up to $200 / month. You can use all services. 

1. Navigate to [Azure.com](https://azure.com)
2. Click "My Account" in the to right navigation area. 
3. Sign Up for an Account
4. Navigate to [Free Subscription Sign Up](https://account.windowsazure.com/signup?offer=ms-azr-0044p&appId=102)

Now, connect your azure subscription to your azure CLI. 

```
$ azure login
$ # follow cl instructions
```


## Resources
