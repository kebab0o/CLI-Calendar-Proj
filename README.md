Here's a README for your C# CLI Calendar application, mirroring the style and structure of the original Python version.

---

# CLI Calendar (C# Version)

CLI Calendar is a command-line interface (CLI) application for managing events, now implemented in C#. This application allows users to add, modify, delete, and list events, display a calendar for a specific month, and view events for today.

## Project Goals

The goal of this project is to provide a simple and efficient way to manage events directly from the command line. It is designed to be lightweight and easy to use, ideal for users who prefer using the terminal over graphical user interfaces.

## Features

- Add events with title, date, description.
- Modify existing events.
- Delete events.
- List events for a specific date.
- Display a calendar for a specific month or year.
- Show today's events.

## Technologies Used

- **.NET 8.0**: C# development framework.
- **Newtonsoft.Json**: For JSON serialization and deserialization of event data.
- **System.CommandLine**: For parsing command-line arguments.
- **Microsoft.Toolkit.Uwp.Notifications** (Windows only): For event notifications.

## Project Structure

```
.
├── CalendarDisplay.cs    
├── CLI.cs                 
├── CML.cs                 
├── Event.cs              
├── EventManager.cs        
├── EventStorage.cs         
├── Notification.cs         
├── Data/
│   ├── ongoingEvents.json  
│   └── finished.json       
└── README.md
```

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/kebab0o/cli-calendar-csharp.git
   cd cli-calendar-csharp
   ```

2. **Install .NET 6 SDK** if you haven't already.

3. **Install required dependencies**:

   Use NuGet to install the following packages:

   ```bash
   dotnet add package Newtonsoft.Json
   dotnet add package System.CommandLine
   dotnet add package Microsoft.Toolkit.Uwp.Notifications
   ```

4. **Run the application**:

   ```bash
   dotnet run
   ```

## Usage

To run specific commands, use `dotnet run` followed by the command. Here are examples for each main feature:

- **Add Event**:

  ```bash
  dotnet run add --title "Event Title" --date "2024-20-10" --description "Description"
  ```

- **Modify Event**:

  ```bash
  dotnet run modify --title "Event Title" --newDate "2024-20-10" --newDescription "Updated Description"
  ```

- **Delete Event**:

  ```bash
  dotnet run delete --title "Event Title"
  ```

- **List Events**:

  ```bash
  dotnet run list
  ```

- **Show Calendar**:

  ```bash
  dotnet run calendar --year 2024 --month 10
  ```

- **Show Today's Events**:

  ```bash
  dotnet run today
  ```

- **Exit Program**:

  Simply type `exit` when prompted to quit the application.

---

Enjoy using CLI Calendar!
