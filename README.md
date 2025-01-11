### [Howzit](https://sayedimac.github.io/) ;)

I added some course examples from my Microsoft courses in the [Coursecontent](https://github.com/sayedimac/coursecontent). Clone that repo, do not fork it, I am consolidating 4-5 repos all in this one. It contains:
 - Azure PowerShell and CLI examples
 - DSC examples (IIS on Windows and LAMP stack  on Linux)
 - Great diagrams about Github relational structures
 - Bicep examples
 - More Azure related content


#### Azure App Service related demos, clone or fork [Slots](https://github.com/sayedimac/slots)
 1. Create an App Service
 2. Configure an [Environment variable](https://learn.microsoft.com/en-us/azure/app-service/configure-common?tabs=portal#configure-app-settings) for each of the custom properties in the appsettings.json file in the root of the repo (dbconn, site, colour and auth - don't forget to save 😉)
 3. Create a second [deployment Slot](https://learn.microsoft.com/en-us/azure/app-service/deploy-staging-slots?tabs=portal) - make sure to copy the config of the Production slot, else you will have to recreate the fields as opposed to just setting new values (both slots will merely render the appsettings.json file settings if not set in the app service slots)
 4. In the second slot (I will call mine UAT as I setup Github [Approval](https://docs.github.com/en/actions/deployment/targeting-different-environments/using-environments-for-deployment#required-reviewers) for a UAT [Environment](https://docs.github.com/en/actions/deployment/targeting-different-environments/using-environments-for-deployment) in that repo hehee Mr fancypants)
 5.  Got to the second Slot Deployment blade, and [deploy the app from Github](https://learn.microsoft.com/en-us/azure/app-service/app-service-sql-asp-github-actions) into your second slot. You should see the values you set fo rhte second slot in the app UI
 6.  Swap slots or you can opt for [auto Swap](https://learn.microsoft.com/en-us/azure/app-service/deploy-staging-slots?tabs=portal#Auto-Swap) which will basically not allow for testing but rather give you a [zero downtime type deployment](https://learn.microsoft.com/en-us/azure/app-service/deploy-continuous-deployment?tabs=github%2Cgithubactions)

#### For container (Docker) demos, clone or fork [docker-app](https://github.com/sayedimac/docker-app). It has several folders but once pushed to ACR, you can easily deploy the container image to ACI, ACA, App Services and AKS. There is a workflow for thislast one, follow these steps:
- In the root of the repo there is a Dockerfile referencing the actual app in /src directory
- There is Github workflow called "Build and deploy an app to AKS" which will require you to [setup a service principal in Github](https://github.com/Azure/arm-deploy) for your Azure Subscription (Service Princial needs Contribute to Subscription)
- deployment.yaml will be referenced in the  Workflow and deploy the app to an AKS cluster so you should update this file with the corresponding changes in the workflow file where relevant

