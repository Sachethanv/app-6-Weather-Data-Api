# Weather Data API

A Flask-based REST API application that provides access to historical weather station data. This web service allows users to query weather information by station, date, and year through a clean and intuitive API interface.

## Overview

This project demonstrates how to build a RESTful API using Flask and Pandas to serve weather data from CSV files. The application includes a web interface displaying available weather stations and provides multiple API endpoints for flexible data retrieval.

## Features

- **Home Page**: Interactive HTML table displaying all available weather stations
- **Station-Date Query**: Retrieve specific weather data for a station on a particular date
- **All Station Data**: Get complete historical data for a specific weather station
- **Yearly Data**: Access all weather data for a station within a specific year
- **REST API**: Clean URL structure following RESTful principles
- **JSON Responses**: All API endpoints return data in JSON format for easy integration

## API Endpoints

### 1. Home Page
```
GET /
```
Displays an HTML page with a table of all available weather stations.

### 2. Get Weather Data by Station and Date
```
GET /api/v1/<station>/<date>
```
**Parameters:**
- `station`: Station ID (e.g., 10)
- `date`: Date in YYYYMMDD format (e.g., 19881025)

**Example:**
```
GET /api/v1/10/19881025
```

### 3. Get All Data for a Station
```
GET /api/v1/<station>
```
**Parameters:**
- `station`: Station ID

**Example:**
```
GET /api/v1/10
```

### 4. Get Yearly Data for a Station
```
GET /api/v1/yearly/<station>/<year>
```
**Parameters:**
- `station`: Station ID
- `year`: Year (4 digits)

**Example:**
```
GET /api/v1/yearly/10/1988
```

## Technology Stack

- **Flask**: Web framework for building the API
- **Pandas**: Data manipulation and CSV file handling
- **Python**: Core programming language
- **HTML**: Frontend for displaying station information

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Sachethanv/app-6-Weather-Data-Api.git
cd app-6-Weather-Data-Api
```

2. Install required dependencies:
```bash
pip install flask pandas
```

3. Ensure your weather data CSV files are in the correct directory structure

## Usage

1. Start the Flask application:
```bash
python main.py
```

2. Access the application:
- Open your browser and navigate to `http://localhost:5000/`
- Use the API endpoints as documented above

## Project Structure

```
app-6-Weather-Data-Api/
├── main.py           # Flask application with API routes
├── home.html         # Frontend HTML template
└── README.md         # Project documentation
```

## Data Format

The application expects weather data in CSV format with the following structure:
- Station data files named according to station IDs
- Date column in YYYYMMDD format
- Weather measurements in subsequent columns

## Use Cases

- Weather data analysis and visualization
- Historical weather pattern research
- Integration with weather forecasting applications
- Educational projects for learning REST API development
- Data science and climate studies

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests to improve the application.

## License

This project is open source and available for educational and research purposes.

## Author

Sachethanv

## Acknowledgments

- Flask documentation and community
- Pandas library for efficient data handling
