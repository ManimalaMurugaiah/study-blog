# .NET Notes

## What is .NET?
.NET is a framework by Microsoft for building apps.

## Topics I Will Add
- C#  
- ASP.NET Core  
- Web API  
- Entity Framework

# SOLID Principles in .NET Core
S.O.L.I.D are five principles of object-oriented design to create maintainable and scalable software:
-	S – Single Responsibility Principle: One class should have one responsibility.
-	O – Open/Closed Principle: Classes should be open for extension, but closed for modification.
-	L – Liskov Substitution Principle: Derived classes must be substitutable for their base classes.
-	I – Interface Segregation Principle: No client should be forced to depend on interfaces it doesn't use.
-	D – Dependency Inversion Principle: High-level modules should not depend on low-level modules. Use abstractions (interfaces).

2. Types of Classes in .NET Core
-	Static Class
-	Abstract Class
- Sealed Class
-	Partial Class
-	Generic Class
-	Record Class (C# 9+)
-	Normal Class (Concrete)
-------------------
3. How to Write a Web API in .NET Core
Steps:
1.	Create a project:
bash
CopyEdit
dotnet new webapi -n MyApiApp
2.	Define a controller:
csharp
CopyEdit
[ApiController]
[Route("api/[controller]")]
public class ProductsController : ControllerBase
{
    [HttpGet]
    public IEnumerable<string> Get() => new[] { "Product1", "Product2" };
}
3.	Configure routing and services in Startup.cs or Program.cs (.NET 6+):
csharp
CopyEdit
builder.Services.AddControllers();
app.MapControllers();

4. What is a Generic Class and Usage
Generic Class:
A class that works with any data type.
csharp
CopyEdit
public class Repository<T>
{
    public void Add(T item) { /* ... */ }
}
Usage:
csharp
CopyEdit
var intRepo = new Repository<int>();
var stringRepo = new Repository<string>();
------------------
5. Difference Between .NET Core and .NET Framework
Feature    	   .NET Core	   .NET Framework
Platform	     Cross-platform 	Windows only
Performance	   High	            Moderate
Deployment	   Side-by-side	    Global only
API Support	   Lightweight,       modular	Full API
Modern App
Support	       Yes (Microservices, Cloud)	Legacy apps
--------------------------


