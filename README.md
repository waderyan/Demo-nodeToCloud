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

**Create Azure Website**

Create a website and deploy our application to it. 

```zsh
azure site create <site-name> --git
```

> site-name is the name of your website. 
>
> CL Options:
> Select location you want (ex. "West US")
> Fill out your git credentials. 

> Troubleshooting
> Occasionally and unpredictably I have seen the following error. 
> `Cannot find WebSpace with name westuswebspace.`
> 
> The best I can tell it occurs when I don't have any other website created. 
> To solve the issue I go to the azure portal and create a website there. 
> 
> Alternatively, removing ~/.azure and relogging in (with `azure login`) has
> solved this issue for me. 

Run the following command to find your site url. 

```zsh
azure site list
```

Locate the URL and navigate to it. 

You should see something like "This web app has been successfully created".

Now, let's publish our app. Run `git remote -v` and you'll notice you have an azure remote now. To publish 
we will push to the azure remote. 

```
git push azure master
```

By default `master` is the deploy branch. 

To demo how easy it is to get things out to production, let's make a change and redeploy. 

Edit views/index.jade. Add your name after `#{title}`

```zsh
git add views/index.jade
git commit -m "Testing deploy change."
git push azure master
```

Refresh your website. 

## Resources

* [Azure Portal](https://portal.azure.com)
* [NodeJS Web App in Azure](https://azure.microsoft.com/en-us/documentation/articles/web-sites-nodejs-develop-deploy-mac/)
