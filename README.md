# Windows-IIS
Windows server app

### Recommendations
* Use Visual Studio 2019
* install all the prerequisites. follow these: 
  * https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/?view=aspnetcore-3.1#iis-configuration  
  * https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/?view=aspnetcore-3.1#install-the-net-core-hosting-bundle
*  


## Part 1: Create and build a website
* Create “ASP.NET Core Web App” project
* Check your csproj content
* Add “Newtonsoft.Json”
* Check your csproj again, what changed?
* Restore Nuget Packages
* Compile (rebuild) your project
* Which files and folders were created?
* Publish your application

## Part 2: Create website on your Microsoft machine
* Add IIS to your windows server
* Create a new IIS application pool
* Create website (use port 5100 and your new application pool)
* Copy your website to your windows server
* Browse to “http://localhost:5100/” from your microsoft machine
* Does it works? If not, make it work

**Make sure you get this result**
