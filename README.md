# Resolute 🎯

An AI-coded New Year's Resolution Tracker built with .NET 10.0

## Overview

Resolute is a command-line application designed to help you track and maintain your New Year's resolutions throughout the year. With features like customizable reminders, progress check-ins, and detailed statistics, Resolute keeps you accountable and motivated to achieve your goals.

### Key Features

- **Resolution Management**: Create, view, edit, and manage your resolutions with detailed descriptions and categories
- **Smart Reminders**: Set up interval-based or specific date reminders to stay on track
- **Progress Tracking**: Regular check-ins to monitor your progress with status indicators (On Track, Struggling, Completed)
- **Statistics & Reports**: View detailed statistics about your resolutions, including completion rates and category breakdown
- **Persistent Storage**: All data is stored locally in JSON format

## Installation

### Prerequisites

- [.NET 10.0 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) or later

### Building from Source

1. Clone the repository:

   ```bash
   git clone https://github.com/ardalis/Resolute.git
   cd Resolute
   ```

2. Build the project:

   ```bash
   dotnet build
   ```

3. Run the application:

   ```bash
   dotnet run --project src/Resolute.Cli/Resolute.Cli.csproj
   ```

### Running Tests

```bash
dotnet test
```

## Usage

### Main Menu

When you start Resolute, you'll see the main menu with the following options:

1. **View All Resolutions** - Browse all your resolutions with filters and details
2. **Add New Resolution** - Create a new resolution with reminders
3. **Check In on Resolution** - Log progress on your resolutions
4. **View Upcoming Reminders** - See which resolutions need attention
5. **Statistics & Reports** - View analytics about your progress
6. **Exit** - Close the application

### Creating a Resolution

1. Select **Add New Resolution** from the main menu
2. Enter a title (e.g., "Exercise 3 times per week")
3. Provide a detailed description
4. Choose a category (Health, Career, Personal, Finance, Education, Relationships, Other)
5. Optionally set a target completion date
6. Configure reminder settings:
   - **Interval-based**: Get reminded every N days
   - **Specific dates**: Set exact dates for reminders
   - **Both**: Combine interval and specific date reminders

### Checking In

1. Select **Check In on Resolution** from the main menu
2. Choose which resolution to check in on
3. Select your status:
   - **On Track**: Making good progress
   - **Struggling**: Encountering difficulties
   - **Completed**: Achieved this resolution!
4. Add optional notes about your progress

### Viewing Statistics

The Statistics & Reports screen provides:

- Total number of resolutions
- Completion rate percentage
- Breakdown by category
- Active vs. completed resolutions
- Recent check-in activity

## Data Storage

Resolutions are stored in a `resolutions.json` file in the application directory. The file is automatically created on first run and updated as you make changes.

### Data Structure

Each resolution includes:

- Unique identifier (GUID)
- Title and description
- Category classification
- Creation and target dates
- Completion date (when applicable)
- Reminder settings (interval-based, specific dates, or both)
- Check-in history with dates, status, and notes

## Project Structure

```
Resolute/
├── src/
│   └── Resolute.Cli/
│       ├── Models/           # Data models (Resolution, CheckIn, etc.)
│       ├── Services/         # Business logic (ResolutionManager, ReminderService, etc.)
│       ├── UI/              # Console UI screens
│       └── Program.cs       # Application entry point
├── tests/
│   └── Resolute.UnitTests/
│       └── Models/          # Model tests
├── Directory.Build.props    # Common build properties
├── Directory.Packages.props # Central package management
└── global.json             # SDK version specification
```

## Technology Stack

- **.NET 10.0** - Target framework
- **C# 13** - Programming language
- **xUnit** - Testing framework
- **TimeWarp.Nuru** - Enhanced console UI framework
- **System.Text.Json** - JSON serialization

## Contributing

This is an AI-coded demonstration project. Feel free to fork and enhance it for your own use!

## License

See [LICENSE](LICENSE) file for details.

## Author

Created by [Steve "ardalis" Smith](https://github.com/ardalis) with AI assistance.
