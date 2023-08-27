# LoginForm

Login and Logout using Session and Database

Phase
1. Setup Session in ASP.NET Core App.
2. Implementing Database First Approach.
3. Login & Logout Task
 
-- Setup Session:-

Add below line before build in program.cs
builder.Services.AddSession();

Add below line after build in program.cs
app.UseSession(); 


-- Implementing DB First:-

1st Step:
Install 3 Packages in your ASP.NET Core Application
Microsoft.EntityFrameworkCore.SqlServer
Microsoft.EntityFrameworkCore.Design 
Microsoft.EntityFrameworkCore.Tools

2nd Step:
Execute a command for Scaffold DbContext in package manager console.

Scaffold-DbContext "Server=servername; database=databasename; trusted_connection=true" Mircosoft.EntityFrameworkCore.SqlServer -OutputDir Models

Above command will generate model class and DbContext class automatically.

3ed Step:
Move Connection String from DbContext class to appsetting.json file 

4th Step:
Registering Connection String in Program.cs file
