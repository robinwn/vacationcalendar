# Vacation Calendar for BC Government

A comprehensive vacation planning tool designed specifically for British Columbia Government employees. This application provides dynamic statutory holiday calculations, interactive vacation day planning, and automated flex day management - all running locally in your browser with no server required.

## Features

### 🎯 Core Functionality
- **Dynamic BC Statutory Holiday Calculation** - Automatically calculates all BC statutory holidays with proper weekend substitution rules
- **Interactive Vacation Planning** - Click-to-select vacation days with intelligent conflict detection
- **Automated Flex Day Generation** - Customizable flex day scheduling with holiday avoidance logic
- **Real-time Statistics** - Live tracking of working days, holidays, vacation days, and flex days
- **Smart Conflict Resolution** - Prevents vacation booking on holidays, weekends, and flex days

### 📱 User Experience
- **Responsive Design** - Works seamlessly on desktop and mobile devices
- **Local Data Storage** - All data stored locally in your browser with automatic saving
- **JSON Import/Export** - Backup, share, or transfer your vacation plans
- **Year Navigation** - Easy switching between years with persistent data
- **Interactive Modes** - Dedicated vacation and flex day editing modes

### 🏛️ BC Government Specific
- **Family Day** - Properly calculated (started in 2013)
- **Truth & Reconciliation Day** - Included for 2021 onwards
- **Victoria Day** - Monday on or before May 24th
- **BC Day** - First Monday in August
- **Weekend Substitution** - Holidays falling on weekends automatically moved to Monday

## Quick Start

### Installation
No installation required! Simply:
1. Download or clone this repository
2. Open [`calendar.html`](calendar.html) in any modern web browser
3. Start planning your vacation days

### Basic Usage

1. **View Calendar** - The calendar displays the current year with all BC statutory holidays pre-calculated
2. **Plan Vacation** - Click "Vacation Mode: OFF" to enable, then click weekdays to mark vacation days
3. **Configure Flex Days** - Use "Flex Settings" to set your start date and period, then "Generate Flex Days"
4. **Plan Vacation Ranges** - Use "Plan Vacation" for multi-day vacation planning
5. **Export Data** - Use "Export JSON" to backup your vacation plans

### Navigation
- **Previous/Next Year** - Navigate between years
- **Current Year** - Jump back to the current year
- **Mode Buttons** - Toggle between vacation and flex day editing modes

## Configuration

### Flex Day Settings
- **Start Date** - The base date from which all flex days are calculated
- **Period** - Number of days between flex days (e.g., 14 for bi-weekly)
- **Holiday Avoidance** - Flex days automatically move to the next working day if they fall on holidays

### Data Management
- **Local Storage** - Data automatically saved to browser localStorage
- **JSON Export** - Generate downloadable backup files
- **JSON Import** - Restore data from backup files
- **Clear Data** - Reset all vacation and flex day data

## Technical Details

### Requirements
- Modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- Local storage support

### Architecture
- **Single File Application** - Everything contained in one HTML file
- **No Server Required** - Runs completely in the browser
- **No External Dependencies** - Self-contained with embedded CSS and JavaScript
- **Local Data Only** - No data sent to external servers

### Holiday Calculation
The application uses precise algorithms to calculate BC statutory holidays:
- **Easter-based holidays** - Good Friday and Easter Monday calculated using astronomical algorithms
- **Fixed date holidays** - New Year's, Canada Day, Christmas, Boxing Day with weekend substitution
- **Relative holidays** - Family Day (3rd Monday in February), Victoria Day, BC Day, Labour Day, Thanksgiving

## Data Format

### JSON Export Structure
```json
{
  "metadata": {
    "exported_date": "2025-01-15",
    "calendar_year": 2025,
    "total_vacation_days": 15,
    "total_flex_days": 26
  },
  "flex_settings": {
    "startDate": "2025-01-03",
    "periodDays": 14
  },
  "vacation_days": {
    "2025-07-14": "Summer Vacation",
    "2025-07-15": "Summer Vacation"
  },
  "flex_days": {
    "2025-01-03": "Flex Day",
    "2025-01-17": "Flex Day"
  }
}
```

## Browser Compatibility

- Known to work in a modern Chrome

## License

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

See the [LICENSE](LICENSE) file for full details.

## Author

**Robin Windels**  
Email: robin.windels@gov.bc.ca  
Created: 2025  
Version: 1.0

## Contributing

This application is designed specifically for BC Government employees. For updates, documentation, and source code, visit the repository.

---

*💡 **Tip**: The application runs entirely in your browser and stores data locally. Your vacation plans are private and never sent to external servers.*
