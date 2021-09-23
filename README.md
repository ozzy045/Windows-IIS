# Windows-IIS
Windows server app

### Recommendations
* Use *Visual Studio 2019*
* install all the prerequisites. follow these: 
  * https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/?view=aspnetcore-3.1#iis-configuration  
  * https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/?view=aspnetcore-3.1#install-the-net-core-hosting-bundle
* Use *Remote Desktop Connection*


## Part 1: Create and build a website
* Create “ASP.NET Core Web App” project :heavy_check_mark: **Create new project with VS 2019 and search “ASP.NET Core Web App”**
* Check your csproj content :heavy_check_mark: **That is the main project file**
* Add “Newtonsoft.Json” :heavy_check_mark: **Use package manager**
* Check your csproj again, what changed?
* Restore Nuget Packages
* Compile (rebuild) your project :heavy_check_mark: **right click on your project and rebuild!**
* Which files and folders were created? 
* Publish your application 
  * Right click on your project and publish
  * On the publish popup select target 'folder'
  * This should create a new file called "publish" in the same directory as your build files.
  * Click on 'finish' and press the "publish" button at the top right corner
  * locate this folder - you will use these files to deploy your app

## Part 2: Create website on your Microsoft machine
* Add IIS to your windows server :heavy_check_mark: **follow the first recommendation link**
* Create a new IIS application pool 
  * run IIS and navigate to the "Aplication Pools" tab.
  * Add a new Application pool, give it a proper name and select "No Managed Code" in ".Net CLR Version"
* Create website (use port 5100 and your new application pool)
  * Go to "Sites" and click on "Add Website"
  * Give your site a proper name and select the Application pool you just created
  * In the "Physical Path" navigate to "\interpub\wwwroot\" and make a new folder, then select this folder and click OK
  * use port 5100 and click OK
* Copy your website to your windows server
  * Right click your new site and click "Explore" 
  * You see an empty folder, this is where you locate the app files we published before
  * Best-Practice: stop the application pool before making any changes in this folder.
  * if you having trouble copying your files, try this:
     https://www.ionos.com/help/server-cloud-infrastructure/dedicated-server-for-servers-purchased-before-102818/servers/transfer-files-using-remote-desktop/
* Browse to “http://localhost:5100/” from your microsoft machine 
* Does it works? If not, make it work by following the Instructions again.

**Make sure you get this result:**

![GitHub Logo](https://github.com/ozzy045/Windows-IIS/blob/master/Example.JPG)
