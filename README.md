# README #

This README would normally document whatever steps are necessary to get your application up and running.

### What is this repository for? ###

* Quick summary
* Version
* [Learn Markdown](https://bitbucket.org/tutorials/markdowndemo)

### How do I get set up? ###

* Summary of set up
* Configuration
* Dependencies
* Database configuration
* How to run tests
* Deployment instructions

### Contribution guidelines ###

* Writing tests
* Code review
* Other guidelines

### Who do I talk to? ###

* Repo owner or admin
* Other community or team contact

### VS Code ###
* auto close tag
* auto rename tag
* bracket part colorizer 2
* C#
* C# Extensions
* sqlite
* prettier
* ES7 React/Reduc/GraphQL/React-Native snippets
* material icon theme
* NuGet Package Manager



### Tips and Tricks ###

.net —info

Create new webapi over cli
dotnet new webapi -n API

Create new class library over cli
dotnet new classlib -n Domain

add "Domain" project to solution with 
dotnet sln add Domain/

Add references between projects
Domain project is the center
Application needs dependency to Domain and Persistence

We go to the Application project and add ref to the Domain project
Cd application
dotnet add reference ../Domain

API needs a reference to our Application project

Persistence needs a reference to Domain

dotnet run -p API/ - set API as startup project and run
http://localhost:5000/api/values

Setup db with sqlite without a db server
opt.UseSqlite(Configuration.GetConnectionString("DefaultConnection"));

dotnet ef migrations add InitialCreate -p Persistence -s API

Add seed migration
dotnet ef migrations add SeedValues -p Persistence -s API/

It is recommended to make all db calls async

localhost:5000/api/values/1
