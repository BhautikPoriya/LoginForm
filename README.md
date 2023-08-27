# LoginForm - EF Core Database First Approch

Login and Logout using Session and Database

Phase
1. Setup Session in ASP.NET Core App.
2. Implementing Database First Approach.
3. Login & Logout Task
 
-- Setup Session:-

Add below line before build in program.cs</br>
builder.Services.AddSession();

Add below line after build in program.cs</br>
app.UseSession(); 


-- Implementing DB First:-

1st Step:</br>
Install 3 Packages in your ASP.NET Core Application</br>
Microsoft.EntityFrameworkCore.SqlServer</br>
Microsoft.EntityFrameworkCore.Design </br>
Microsoft.EntityFrameworkCore.Tools</br>

2nd Step:</br>
Execute a command for Scaffold DbContext in package manager console.</br>

Scaffold-DbContext "Server=servername; database=databasename; trusted_connection=true" Mircosoft.EntityFrameworkCore.SqlServer -OutputDir Models

Above command will generate model class and DbContext class automatically.</br>

3ed Step:</br>
Move Connection String from DbContext class to appsetting.json file </br>

4th Step:</br>
Registering Connection String in Program.cs file
