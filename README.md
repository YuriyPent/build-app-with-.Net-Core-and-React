# Complete guide to building an app with .Net Core and React
## Commands
* `dotnet --info` -  check dotnet version
* `mkdir Reactivities` - create folder
* `cd Reactivities` 
* `dotnet new sln` - create sln
* `dotnet new classlib -n Domain` - create classlib Domain
* `cd Domain`
* `cd ..`
* `dotnet new classlib -n Application` - create classlib Application
* `dotnet new classlib -n Persistence` - create classlib Persistence
* `dotnet new webapi -n API` - create classlib API
* `dotnet sln add Domain` - add project to sln
* `dotnet sln add Persistence` - add project to sln
* `dotnet sln add API` - add project to sln
* `dotnet sln list` - show sln projects
* `cd Application`
* `dotnet add reference ../Domain/`
* `dotnet add reference ../Persistence`
* `cd ..`
* `cd Reactivities`
* `cd API`
* `dotnet add reference ../Application/`
* `cd ..`
* `cd Persistence`
* `dotnet add reference ../Domain/`
* `cd..`
* `code .` - run vscode
* `doskey /history > C:\Users\user\Desktop\commands.txt`
* `dotnet run -p API/` - run app
* `dotnet ef migrations add InitialCreate -p Persistence/ -s API/` - migration
