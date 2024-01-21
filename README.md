# .Net Unit Test Template

A minimal template for setting up a .Net Console App project with unit tests using [NUnit](https://nunit.org/) in VSCode.

References

- <https://code.visualstudio.com/docs/languages/csharp>
- <https://code.visualstudio.com/docs/csharp/get-started>
- <https://code.visualstudio.com/docs/csharp/testing>
- <https://docs.nunit.org/articles/nunit/getting-started/installation.html#im-using-visual-studio-code-as-my-development-tool>
- <https://docs.nunit.org/articles/nunit/running-tests/Index.html>

## Terminal Commands

Pre-requisites: Have the .Net SDK installed on your local machine.

Run [`/ConsoleApp/Program.cs`](./ConsoleApp/Program.cs)

```bash
dotnet run --project ConsoleApp
```

Run all unit tests

```bash
dotnet test
```

## Configuration

`ConsoleApp` and `TestProject` can be renamed to any other new name by renaming all the files and replacing all occurences of the original names to their new names. See [this repository](https://github.com/gjtiquia/advent-of-code-2023) for an example.

## Troubleshooting

If you have a different .Net SDK version, change the `<TargetFramework>` field in [AdventOfCode.csproj](./AdventOfCode/AdventOfCode.csproj) and [UnitTests.csproj](./UnitTests/UnitTests.csproj) to the corresponding version that you have.

## Setup Steps

The setup steps used to create this template.

### 1. Console App Setup

In root directory, using VSCode Command Pallete with C# Dev Kit installed: _.Net: New Project_ > _Console App_.

Name the project `ConsoleApp`.

In the `ConsoleApp` directory, Run the following to create a `.gitignore` file.

```bash
dotnet new gitignore
```

In the `ConsoleApp` directory, Run the following command to run the `Program.cs` file.

```bash
dotnet run
```

### 2. NUnit Setup

In root directory, using VSCode Command Pallete with C# Dev Kit installed: _.Net: New Project_ > _NUnit 3 Test Project_.

Name the project `TestProject`

In the `TestProject` directory, Run the following to create a `.gitignore` file.

```bash
dotnet new gitignore
```

In the root directory, run the following command to reference the main project `ConsoleApp` in the test project `TestProject`.

```bash
dotnet add TestProject/TestProject.csproj reference ConsoleApp/ConsoleApp.csproj
```
