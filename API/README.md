dotnet --info
mkdir Reactivities
cd Reactivities
dotnet new sln
dotnet new classlib -n Domain
cd Domain
cd ..
dotnet new classlib -n Application
dotnet new classlib -n Persistence
dotnet new webapi -n API
dotnet sln add Domain
dotnet sln add Persistence
dotnet sln add API
dotnet sln list
cd Application
dotnet add reference ../Domain/
dotnet add reference ../Persistence
cd ..
cd Reactivities
cd API
dotnet add reference ../Application/
cd ..
cd Persistence
dotnet add reference ../Domain/
cd..
code .
doskey /history > C:\Users\user\Desktop\commands.txt
