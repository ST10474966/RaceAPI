# RaceAPI – Race Event Management System

# 1. Project Description

RaceAPI is an ASP.NET Core Web API developed to manage race events. The system allows users to manage categories, events, organisers, participants, routes, enrolments, results, and user accounts.

The API uses Entity Framework Core to communicate with a Microsoft SQL Server database. It also provides user registration and login functionality using BCrypt 

# 2. Technologies Used

- C#
- ASP.NET Core Web API
- .NET 8
- Entity Framework Core 8
- Microsoft SQL Server
- BCrypt.Net-Next
- Swagger / OpenAPI
- Git and GitHub

 3. Main Features

- Manage race categories.
- Create, view, update, and delete race events.
- Manage race organisers.
- Manage participant records.
- Manage race routes.
- Manage event enrolments.
- Record and view race results.
- Register user accounts.




## 4. Project Structure

```text
RaceAPI/
├── Controllers/
│   ├── CategoriesController.cs
│   ├── EventsController.cs
│   ├── OrganisersController.cs
│   ├── ParticipantsController.cs
│   ├── ResultsController.cs
│   ├── RoutesController.cs
│   ├── EnrolmentsController.cs
│   ├── UserAccountsController.cs
│   └── AuthController.cs
├── Data/
│   └── ApplicationDbContext.cs
├── Models/
│   ├── Category.cs
│   ├── Event.cs
│   ├── Organiser.cs
│   ├── Participant.cs
│   ├── Result.cs
│   ├── Route.cs
│   ├── Enrolment.cs
│   ├── UserAccount.cs
│   └── Auth
│       ├── LoginRequest.cs
│       └── RegisterRequest.cs
├── Program.cs
├── appsettings.json
└── 


## 5. Installation and Setup

### Requirements

- Visual Studio
- .NET 8 SDK
- Microsoft SQL Server or SQL Server LocalDB
- Git

### Steps

1. Clone or download this repository.
2. Open `RaceAPI.sln` in Visual Studio, if the solution file is included.
3. Check the database connection string in `appsettings.json`.
4. Restore the required NuGet packages.
5. Open the Package Manager Console.
6. Select `RaceAPI` as the default project.
7. Create the database migration:

   `Add-Migration InitialCreate

8. Apply the migration:

   `Update-Database

9. Build and run the project.
10. Open the Swagger URL displayed by Visual Studio to test the API.

# 6. API Endpoints

| Endpoint | Purpose |
|---|---|
| `/api/Categories` | Manage categories |
| `/api/Events` | Manage race events |
| `/api/Organisers` | Manage organisers |
| `/api/Participants` | Manage participants |
| `/api/Routes` | Manage race routes |
| `/api/Enrolments` | Manage enrolments |
| `/api/Results` | Manage race results |
| `/api/UserAccounts` | View user account information |
| `/api/Auth/register` | Register a user |
| `/api/Auth/login` | Log in a user |

The exact HTTP methods available depend on the controller implementation.

## 7. Authentication

The registration endpoint hashes passwords using BCrypt before storing them. The login endpoint verifies submitted passwords against the stored password hashes.

**Security note:** The current login implementation does not issue JWT tokens or establish a complete authenticated session. Protected endpoints and authorization policies must be configured before using the API in production.

## 8. Testing

The API can be tested through Swagger. Test the available GET, POST, PUT, and DELETE endpoints, where supported. Also test registration and login using valid and invalid 

 9. Version Control

GitHub is used to store the project source code and track development through meaningful commits. Each commit records a change to the project.



