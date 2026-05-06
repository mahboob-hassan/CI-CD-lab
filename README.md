# 🧪 Swagger API Test Automation with CI/CD Pipeline

A sample API test automation project built with **C#**, **HttpClient**, and **NUnit**, targeting a **Swagger-documented REST API**. Includes a fully configured **GitHub Actions CI/CD pipeline** that runs tests automatically on every push and pull request.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| C# / .NET 8 | Programming language and runtime |
| HttpClient | Sending HTTP requests to REST APIs |
| Newtonsoft.Json | JSON serialization and deserialization |
| NUnit | Test framework for writing and running tests |
| NUnit3TestAdapter | Running NUnit tests via dotnet CLI |
| Swagger / OpenAPI | API documentation and contract reference |
| GitHub Actions | CI/CD pipeline automation |

---

## ✅ What's Covered

- REST API testing using Swagger/OpenAPI spec as a reference
- CRUD operation tests — GET, POST, PUT, DELETE
- JSON request and response handling with Newtonsoft.Json
- Status code, header, and response body validation
- Strongly typed model classes mapped from API responses
- Automated test execution via GitHub Actions on every push and PR
- Test results published after each pipeline run

---

## ⚙️ Prerequisites

- .NET 8 SDK installed
- Git installed
- An IDE — Visual Studio or JetBrains Rider recommended

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/your-username/your-repo-name.git

# Navigate to the project
cd your-repo-name

# Restore dependencies
dotnet restore

# Run all tests
dotnet test
```

---

## 🔄 CI/CD Pipeline

The project uses **GitHub Actions** for continuous integration. Tests run automatically on:

- Every `push` to the `main` branch
- Every `pull request` targeting `main`

Pipeline steps:
1. Checkout code
2. Set up .NET 8
3. Restore NuGet packages
4. Build the project
5. Run tests with `dotnet test`
6. Publish test results

Pipeline config is located at `.github/workflows/ci.yml`

---

## 📁 Project Structure

```
SwaggerApiTests/
├── Models/                  # C# model classes mapped from API responses
├── Helpers/                 # HttpClient setup, base URL config, utilities
├── Tests/                   # Test classes organized by endpoint/feature
├── SwaggerApiTests.csproj   # Project file with NuGet dependencies
.github/
└── workflows/
    └── ci.yml               # GitHub Actions pipeline
```

---

## 📦 Key NuGet Packages

```xml
<PackageReference Include="Newtonsoft.Json" Version="13.0.3" />
<PackageReference Include="NUnit" Version="3.14.0" />
<PackageReference Include="NUnit3TestAdapter" Version="4.5.0" />
<PackageReference Include="Microsoft.NET.Test.Sdk" Version="17.9.0" />
```

---

## 📊 Reports

After running tests, results are available in the terminal output. For HTML reports, install:

```bash
dotnet add package ExtentReports
```
