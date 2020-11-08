# todoAppTuroASP.netCore

following the tutorial found here : 

https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-3.1&tabs=visual-studio-code

1./to create the app in terminal do : 

dotnet new webapi -o TodoApi
cd TodoApi
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameworkCore.InMemory
code -r ../TodoApi

2./ accept the  prompt you get in vsc
click yes

3./ test app wit ctrl F5

4./ create your first models :
 TodoItem
 TodoContext

5./ Register database context
 
 copy paste the startup.cs

6./ scaffold a controller CLI : 

dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design
dotnet add package Microsoft.EntityFrameworkCore.Design
dotnet tool install --global dotnet-aspnet-codegenerator
dotnet tool update -g Dotnet-aspnet-codegenerator
dotnet aspnet-codegenerator controller -name TodoItemsController -async -api -m TodoItem -dc TodoContext -outDir Controllers

7./ Change the code for Post in TodoItemsController

8./ change security in postman 

settings => disable SSL certificate verification

9./ test POST and GET in postman

10./ change the route 

change the route to take  Todoitems  in stead of [controller]

11./ test PUT method

12./ examine and test DELETE method

13./ prevent overposting by using a subset of a model (DTO)




FINAL STEP 

REACTIVATE SSL IN POSTMAN
