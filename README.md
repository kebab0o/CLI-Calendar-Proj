# Command-Line Calendar Project

The Command-Line Calendar is a CLI application designed for event and task management, available in Python, C#, and JavaScript versions. Users can manage events by adding, modifying, deleting, or listing tasks within the command line. Each version leverages the strengths of its respective language to provide a unique and efficient approach to interacting with the calendar.

## Project Goals

The goal of this project is to provide a simple, lightweight, and efficient way to manage events directly from the command line, without needing a graphical user interface.

## General Features

- **Calendar Display**: Show current or specified month/year.
- **Task and Event Management**:
  - Add, modify, delete, and list tasks or events.
  - Mark tasks as finished.
  - Set notifications (Python and C# versions).
- **Data Persistence**: Events are stored in JSON files for easy retrieval and modification.

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/finalnirepo/cli-calendar.git
   cd cli-calendar
   ```

## Language-Specific Implementations

Each version has slight variations in functionality and setup. See details below for the Python, C#, and JavaScript versions.

### Python Version

CLI Calendar (Python) is a command-line interface for managing events with support for notifications on Windows.

#### Setup

1. Ensure **Python** is installed.
2. Install dependencies:

   ```bash
   pip install win11toast
   ```

#### Usage Examples

- **Add Event**: `python cli_calendar.py add "Event Title" "2024-11-15" -d "Description" -t "09:00" -n "2024-11-15-07:00"`
- **Finish Event**: `python cli_calendar.py finish "Event Title" "2024-11-15"`
- **Delete Event**: `python cli_calendar.py delete "Event Title" "2024-11-15"`
- **Modify Event**: `python cli_calendar.py modify "Event Title" "2024-11-15" -d "New Description" -t "10:00"`
- **Show Calendar**: `python cli_calendar.py show -y 2024 -m 11`

#### Project Structure

```
.
├── cli_calendar.py
├── cli_utils.py
├── notification_utils.py
├── data/
│   ├── events.json
│   └── finished.json
└── README.md
```

### C# Version

CLI Calendar (C#) uses .NET for cross-platform compatibility, offering event notifications on Windows.

#### Setup

1. Ensure **.NET 8.0** SDK is installed.
2. Install dependencies with NuGet:

   ```bash
   dotnet add package Newtonsoft.Json
   dotnet add package System.CommandLine
   dotnet add package Microsoft.Toolkit.Uwp.Notifications
   ```

3. Run the application:

   ```bash
   dotnet run
   ```

#### Usage Examples

- **Add Event**: `dotnet run add --title "Event Title" --date "2024-11-15" --description "Description"`
- **Modify Event**: `dotnet run modify --title "Event Title" --newDate "2024-11-16"`
- **Delete Event**: `dotnet run delete --title "Event Title"`
- **List Events**: `dotnet run list`
- **Show Calendar**: `dotnet run calendar --year 2024 --month 11`

#### Project Structure

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

### JavaScript Version

CLI Calendar (JavaScript) is a Node.js-based implementation that focuses on task management and calendar views with no external dependencies.

#### Setup

This version uses built-in Node.js libraries. To run it:

1. Ensure **Node.js** is installed.
2. Run the application:

   ```bash
   node calendar.js <command>
   ```

#### Usage Examples

- **Show Current Month**: `node calendar.js show`
- **Show Specific Month**: `node calendar.js show -m 2024 11`
- **Add Task**: `node calendar.js add 2024 11 15 "My Task"`
- **Delete Task**: `node calendar.js delete 2024 11 15 "My Task"`

#### Project Structure

```
.
├── calendar.js
├── data/
│   ├── events.json
└── README.md
```

## Dependencies

### Python

- **argparse**: Command-line argument parsing.
- **json**: Data storage.
- **datetime**: Date and time manipulation.
- **calendar**: Displaying calendars.
- **win11toast** (Windows only): Notifications.

### C#

- **.NET 8.0 SDK**: Development framework for C#.
- **Newtonsoft.Json**: JSON serialization and deserialization.
- **System.CommandLine**: Command-line argument parsing.
- **Microsoft.Toolkit.Uwp.Notifications** (Windows only): Notifications.

### JavaScript

- **fs**: For reading and writing to the JSON file where data is stored.
- **path**: Cross-platform file path management.
- **process**: Handles command-line arguments.

---

Enjoy using the Command-Line Calendar!
