# Complete guide to building an app with .Net Core and React

## Walking Skeleton Part 1 - API
`dotnet --info` -  check dotnet version
`mkdir Reactivities` - create folder
`cd Reactivities` 
`dotnet new sln` - create sln
`dotnet new classlib -n Domain` - create classlib Domain
`cd Domain`
At the 'Reactivities' level run the following command:
`cd ..`
`dotnet new classlib -n Application` - create classlib Application
`dotnet new classlib -n Persistence` - create classlib Persistence
`dotnet new webapi -n API` - create classlib API
`dotnet sln add Domain` - add project to sln
`dotnet sln add Persistence` - add project to sln
`dotnet sln add API` - add project to sln
`dotnet sln list` - show sln projects
`cd Application`
`dotnet add reference ../Domain/`
`dotnet add reference ../Persistence`
`cd ..`
`cd Reactivities`
`cd API`
`dotnet add reference ../Application/`
`cd ..`
`cd Persistence`
`dotnet add reference ../Domain/`
`cd..`
`code .` - run vscode
`doskey /history > C:\Users\user\Desktop\commands.txt`
`dotnet run -p API/` - run app
`dotnet ef migrations add InitialCreate -p Persistence/ -s API/` - migration
 `dotnet watch run`
 Run command `SqlLite open database` open reactivities.db
 `dotnet ef migrations add SeedValues -p Persistence/ -s API/`

 ## Walking Skeleton Part 2 - Client
 `npx create-react-app client-app --use-npm --typescript` - create-react-app
`cd client-app/`
`npm start`