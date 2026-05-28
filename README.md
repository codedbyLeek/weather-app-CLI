# Weather CLI

A simple Python command-line tool that fetches the current weather for any city using the free [wttr.in](https://wttr.in) service.

## Features

- Look up current weather by city name
- Displays temperature (°F), weather condition, and humidity
- No API key required — uses the free wttr.in JSON endpoint

## Requirements

- Python 3.6+
- [`requests`](https://pypi.org/project/requests/) library

Install the dependency with:

```bash
pip install requests
```

## Usage

Run the script from your terminal:

```bash
python weather.py
```

You'll be prompted to enter a city name:

```
Enter a city name: Atlanta
You want the weather for: Atlanta
Temperature: 72°F
Condition: Partly cloudy
Humidity: 58%
```

City names with spaces work too (e.g., `New York`, `San Francisco`).

## How It Works

The script sends a GET request to `https://wttr.in/<city>?format=j1`, which returns weather data as JSON. It then pulls out the current temperature, weather description, and humidity from the response.

## Error Handling

If the request fails (bad city name, no internet connection, unexpected response format, etc.), the script prints:

```
Something went wrong! Please check your city name and try again.
```

## Possible Improvements

A few things you could add later:

- Support for Celsius via a command-line flag
- Show additional fields like wind speed, feels-like temperature, or the multi-day forecast
- More specific error messages (network error vs. city not found vs. parsing error)
- Accept the city as a command-line argument instead of interactive input

## License

Free to use and modify.
