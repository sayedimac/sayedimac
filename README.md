### Howzit ;)

I added some course examples from my Microsoft cpourses in the [Coursecontent](https://github.com/sayedimac/coursecontent). Clone that repo, do not fork it, I am consolidating 4-5 repos all in this one. 

It contains:
 - Azure PowerShell and CLI examples
 - DSC examples (IIS on Windows and LAMP stack  on Linux)
 - Great diagrams about Github relational structures
 - Bicep examples


For Azure App Serive related demos, clone or fork [Slots](https://github.com/sayedimac/slots)
 1. Create an App Service
 2. Configure an Environment Variable for each of the custom preperties in the appsettings.json file in the root of the repo (dbconn, site, colour and auth - dont' forget to save 😉)
 3. Create a second application Slot - make sure to copy the config of the Production slot, else you will have to recreate the fields as opposed to just setting new values (both slots will merely render the appsettings.json file config settings if not set in the app service slots
 4. In the second slot (I will call mine UAT as I setup Github [Approval](https://docs.github.com/en/actions/deployment/targeting-different-environments/using-environments-for-deployment#required-reviewers) for a UAT [Environment](https://docs.github.com/en/actions/deployment/targeting-different-environments/using-environments-for-deployment) in that Repo hehehe), 
 5.  
