This project consists mainly of my notes and remarks for a .NET API tutorial that was on my playlist. It was intended to cover the basics and help me create a solid foundational understanding of the principles that dictate how .NET APIs work.

**Link to Tutorial:** https://www.youtube.com/watch?v=87oOF9Ve-KA

## Running this project
1. `dotnet run`
2. Access `http://localhost:5004/swagger/index.html` on your browser for the Open API interface

---

## Tutorial Notes

- Versioning APIs is very important because breaking changes need to be signalled.
- APIs are important because they're a bridge between user interfaces and an application's data
- What makes a controller (not sure what is convention vs. actually required)
  - "Controller" in the class name
  - File in the `Controllers` directory
  - `[ApiController]` annotation over class
  - Inheritance from `ControllerBase`
- The REST standard itself is poorly understood so it's difficult to create something 100% RESTful
  - From a high level, REST is all about keeping minimal endpoints and the difference in behavior comes from how you interact with them (using a GET vs a POST)
  - Bottom line: Predictability is key
- .NET APIs can be Controller-Based or Minimal
  - Controller
    - `dotnet new webapi`
    - Endpoints correspond to controller classes, which live in the `Controllers` directory
    - More complex, scale better
    - Great for APIs with lots of controllers
  - Minimal
    - `dotnet new web`
    - Endpoints are in the `Program.cs` file, using commands such as `MapGet`
    - Scale poorly, simpler
    - Good for microservices that have 2 or 3 endpoints
  - From an end user's perspective, both feel identical
- C# project types reference: https://www.csharpprojects.com