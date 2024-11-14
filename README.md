---

# Command-Line Calendar Project

The Command-Line Calendar is a CLI application designed for event and task management, available in Python, C# and JavaScript versions. Users can manage events by adding, modifying, deleting, or listing tasks within the command line. Each version offers a unique approach to interacting with the calendar, leveraging the strengths of each programming language.

## Project Goals

The goal of this project is to provide a simple, lightweight, and efficient way to manage events directly from the command line, without needing a graphical user interface.

## General Features

- Display calendar for current or specified month/year.
- Task and Event Management:
  - Add, modify, delete, and list tasks or events.
  - Mark tasks as finished.
  - Set notifications.
- Data Persistence:
  - Stores events in JSON files for easy data retrieval and modification.

## Installation

1. **Clone the Repository**:

   ```bash
	git clone https://github.com/finalnirepo/cli-calendar.git
	cd cli-calendar
   ```

## Language-Specific

### Python 

CLI Calendar (Python) is a command-line interface for managing events with support for notifications on Windows.

#### Features

- Add events with title, date, description, time, and notification.
- Modify existing events.
- Delete events.
- Mark events as finished.
- List events for a specific date.
- Show a calendar for a specific month or year.

#### Setup

1. Ensure you have **Python** installed.
2. Install required dependencies:

   ```bash
   pip install win11toast
   ```

#### Usage Examples

- **Add Event**:

  ```sh
  python cli_calendar.py add "Event Title" "2024-11-15" -d "Description" -t "09:00" -n "2024-11-15-07:00"
  ```

- **Finish Event**:

  ```sh
  python cli_calendar.py finish "Event Title" "2024-11-15"
  ```

- **Delete Event**:

  ```sh
  python cli_calendar.py delete "Event Title" "2024-11-15"
  ```

- **Modify Event**:

  ```sh
  python cli_calendar.py modify "Event Title" "2024-11-15" -d "New Description" -t "10:00" -n "2024-11-15-08:00"
  ```

- **Show Calendar**:

  ```sh
  python cli_calendar.py show -y 2024 -m 11
  ```

### C# Version

CLI Calendar (C#) provides similar functionality to the Python version, using the .NET environment for cross-platform compatibility.

#### Features

- Add, modify, delete and list events.
- Display a calendar for a specific month or year.
- Show today’s events.

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

### JavaScript Version

CLI Calendar (JavaScript) is a Node.js based implementation which is focusing on task management and calendar views with no external dependencies.

#### Features

- Display the current or specified month/year calendar.
- Add, edit, or delete tasks by date and name.
- View all tasks for today or a specified day.

#### Setup

This version uses built-in Node.js libraries. To run it:

1. Ensure you have **Node.js** installed.
2. Run the application:

   ```bash
   node calendar.js <command>
   ```

#### Usage Examples

- **Show Current Month**:

  ```bash
  node calendar.js show
  ```

- **Show Specific Month**:

  ```bash
  node calendar.js show -m 2024 11
  ```

- **Add Task**:

  ```bash
  node calendar.js add 2024 11 15 "My Task"
  ```

- **Delete Task**:

  ```bash
  node calendar.js delete 2024 11 15 "My Task"
  ```

## Dependencies

### Python

- **argparse**: For command-line argument parsing.
- **json**: For data storage.
- **datetime**: For date and time manipulation.
- **calendar**: For displaying calendars.
- **win11toast** (Windows only): For notifications.

### C#

- **.NET 8.0 SDK**: Development framework for C#.
- **Newtonsoft.Json**: For JSON serialization and deserialization.
- **System.CommandLine**: For command-line argument parsing.
- **Microsoft.Toolkit.Uwp.Notifications** (Windows only): For notifications.

### JavaScript

- **fs**: For reading and writing to the JSON file where data is stored.
- **path**: Manages file paths across different OSes.
- **process**: Handles command-line arguments.

---

Enjoy using the Command-Line Calendar!
