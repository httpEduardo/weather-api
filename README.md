# Weather Application

![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## Overview

A simple and efficient Python weather application that leverages the OpenWeatherMap API to provide real-time weather information for any city worldwide. This lightweight command-line tool features a modular architecture designed for easy maintenance and extensibility.

## Features

- 🌡️ **Real-time Weather Data**: Get current temperature readings in Celsius
- 💧 **Humidity Information**: Monitor humidity levels
- 🌤️ **Weather Descriptions**: Detailed weather condition descriptions
- 🏙️ **Global Coverage**: Search weather for any city worldwide
- 📦 **Modular Design**: Clean separation of concerns with dedicated modules

## Prerequisites

Before running this application, ensure you have the following:

- **Python 3.x** installed on your system
- **Internet connection** for API access
- **OpenWeatherMap API key** (free tier available)
- **requests library** for Python (HTTP requests)

## Installation

1. Clone this repository or download the project files:
   ```bash
   git clone https://github.com/httpEduardo/weather-api.git
   cd weather-api
   ```

2. Verify Python is installed:
   ```bash
   python --version
   # or
   python3 --version
   ```

3. Install required dependencies:
   ```bash
   pip install requests
   # or
   pip3 install requests
   ```

4. Obtain a free API key from [OpenWeatherMap](https://openweathermap.org/api):
   - Sign up for a free account at https://openweathermap.org/api
   - Navigate to API keys section
   - Generate a new API key
   - Copy the key for configuration

## Configuration

Before running the application, you need to configure your API key:

1. Open `weather_api.py` in your preferred text editor or IDE
2. Locate line 4 containing `'SUA_API_KEY'`
3. Replace `'SUA_API_KEY'` with your actual OpenWeatherMap API key:

   ```python
   api_key = 'your_actual_api_key_here'
   ```

**Important**: Keep your API key secure and never commit it to public repositories.

## Usage

To run the weather application:

1. Open a terminal or command prompt
2. Navigate to the project directory:
   ```bash
   cd /path/to/weather-api
   ```

3. Run the application:
   ```bash
   python weather_api.py
   # or
   python3 weather_api.py
   ```

4. Enter the city name when prompted:
   ```
   Enter city name: London
   ```

5. View the weather information displayed:
   ```
   Temperature: 15.3°C
   Humidity: 72%
   Description: scattered clouds
   ```

## Example Output

```
Enter city name: Tokyo
Temperature: 22.5°C
Humidity: 65%
Description: clear sky
```

## Project Structure

The application is organized into three main modules:

```
weather-api/
│
├── weather_api.py          # Main application entry point
│   └── Handles API requests, user input, and weather display
│
├── weather_processor.py    # Data processing module
│   └── Processes and formats weather data from API responses
│
├── main.py                 # Alternative data processing module
│   └── Contains process_weather_data function
│
└── README.md              # Project documentation
```

### Module Descriptions

- **`weather_api.py`**: The main application entry point. Contains the complete weather application with API communication, user input handling, inline data processing, and output display. This is the file you run to use the application. Note that it processes data directly rather than using the separate processing modules.

- **`weather_processor.py`**: Contains a reusable helper function `process_weather_data()` that can process and format raw weather data from API responses into a user-friendly string format. This module provides an alternative modular approach to data processing.

- **`main.py`**: Contains the same `process_weather_data()` function as `weather_processor.py`, providing an alternative module name for the data processing functionality.

## Troubleshooting

### Common Issues

**"City not found!" error**
- Verify the city name is spelled correctly
- Try using the full city name or include the country code (e.g., "London,UK")

**API key errors**
- Ensure you've replaced `'SUA_API_KEY'` in `weather_api.py` with your actual API key
- Verify your API key is active (new keys may take a few minutes to activate)
- Check that your API key hasn't exceeded the free tier limits

**Connection errors**
- Verify your internet connection is active
- Check if the OpenWeatherMap API is accessible from your location
- Ensure no firewall is blocking the connection

**Module import errors**
- Confirm the `requests` library is installed: `pip install requests`
- Ensure all three Python files are in the same directory

## License

This project is distributed under the MIT License. This means you are free to use, modify, and distribute this software, provided the original license notice is included.

---

**Note**: This application uses the OpenWeatherMap API free tier, which has rate limits. Please review the [API documentation](https://openweathermap.org/api) for current usage limits and terms of service.
