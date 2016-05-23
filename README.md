# ASP .NET Core Sample App

A simple ASP.NET Core web application for the [ASP.NET Core buildpack](https://github.com/cloudfoundry-community/asp.net5-buildpack).

## Get the App Locally
1. Install ASP.NET Core by following [Get started with ASP.NET Core RC2](https://docs.asp.net/en/1.0.0-rc2/getting-started.html)
2. Get and build the code
```
git clone https://github.com/ritazh/aspnetcoreapp-cf
cd aspnetcoreapp-cf
dotnet restore
```

## Deploying the App to Cloud Foundry
```
cf push aspnetcoreapp -m 1g -b https://github.com/cloudfoundry-community/asp.net5-buildpack.git --no-start
cf enable-diego aspnetcoreapp
cf start aspnetcoreapp
```