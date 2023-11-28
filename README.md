# .Net Unit Test Template

A minimal template for setting up a .Net project with unit tests using [NUnit](https://nunit.org/) in VSCode.

References

- <https://code.visualstudio.com/docs/languages/csharp>
- <https://code.visualstudio.com/docs/csharp/get-started>
- <https://code.visualstudio.com/docs/csharp/testing>
- <https://docs.nunit.org/articles/nunit/getting-started/installation.html#im-using-visual-studio-code-as-my-development-tool>
- <https://docs.nunit.org/articles/nunit/running-tests/Index.html>

## Setup Steps

### 1. Console App Setup

In root directory, using VSCode Command Pallete with C# Dev Kit installed: ".Net: new Project" > "Console App".

Name the project "ConsoleApp"

Using the terminal, `cd ConsoleApp` to go into the ConsoleApp directory.

Run `dotnet new gitignore` to create a .gitignore file.

Run `dotnet run` to run the `Program.cs` file.

### 2. NUnit Setup

In root directory, using VSCode Command Pallete with C# Dev Kit installed: ".Net: new Project" > "NUnit 3 Test Project".

Name the project "TestProject"

Using the terminal, `cd TestProject` to go into the TestProject directory.

Run `dotnet new gitignore` to create a .gitignore file.

In the root directory, run `dotnet add TestProject/TestProject.csproj reference ConsoleApp/ConsoleApp.csproj` to reference the main project in the test project.
