# ASP.NET Core Game Store API

This is a Game Store REST API project developed using ASP.NET Core. The project demonstrates how to build a complete Web API using the latest ASP.NET Core features.

## Project Features

- Data access using Entity Framework Core
- Complete CRUD operations implementation
- Data Transfer Objects (DTOs) for data transmission
- Route grouping implementation
- Data validation
- Dependency injection
- Asynchronous programming model

## Key Components

- `GamesEndpoints`: Handles CRUD operations for games
- `GenresEndpoints`: Handles genre queries
- `GameStoreContext`: Entity Framework Core database context
- Data Models: Includes Game and Genre entities

## Technologies Used

- ASP.NET Core
- Entity Framework Core
- SQLite Database
- Latest C# Features

## How to Run

1. Ensure .NET SDK is installed
2. Clone this repository
3. In the project root directory, run:
   ```
   dotnet run
   ```

## API Endpoints

- GET /games - Retrieve all games
- GET /games/{id} - Retrieve a specific game
- POST /games - Add a new game
- PUT /games/{id} - Update a game
- DELETE /games/{id} - Delete a game
- GET /genres - Retrieve all game genres

## Database Migration

Database migrations are automatically executed on application startup (`app.MigrateDbAsync()`).

## Configuration

The database connection string is configured in the application settings:

```csharp
var connString = builder.Configuration.GetConnectionString("GameStore");
```

## Project Structure

The project follows a clean architecture approach:

- Endpoints are organized using route groups
- Data models are separated from DTOs
- Mapping logic is isolated in extension methods
- Database context is configured with dependency injection

## Error Handling

The API implements comprehensive error handling:

- Validates input data
- Returns appropriate HTTP status codes
- Provides meaningful error messages

## Frontend Integration

The API is designed to be easily integrated with various frontend frameworks, providing:

- Consistent JSON responses
- CORS support if needed
- Well-documented endpoints
