# WeatherPy-and-VacationPy
WeatherPy and VactionPy, using ApiKey and GeoKey

# WeatherPy and VacationPy Data Analysis

## Overview
This project leverages Python, API calls, and data visualization tools to analyze global weather patterns and use that data to plan ideal vacation destinations. The analysis is split into two core components:
1. **WeatherPy:** Visualizes and models weather metrics across more than 500 random global cities relative to their distance from the equator.
2. **VacationPy:** Utilizes the weather dataset to filter for ideal travel conditions and maps nearby accommodations using geographic information systems.

## Key Features
*   **Global Weather Sampling:** Generates a random list of cities using latitude and longitude coordinates via the `citipy` library.
*   **API Ingestion:** Performs dynamic HTTP requests to pull live meteorological data and geographic points of interest.
*   **Linear Regression Analysis:** Separates cities into Northern and Southern Hemispheres to evaluate correlations between latitude and variables like maximum temperature, humidity, cloudiness, and wind speed.
*   **Geospatial Visualization:** Builds interactive map layers, utilizing heatmaps to show humidity density and interactive pins to show lodging information.

---

## Tech Stack & APIs
*   **Languages & Libraries:** Python, Pandas, NumPy, Matplotlib, SciPy, Requests, Hvplot
*   **OpenWeatherMap API:** Used in `WeatherPy` to fetch real-time weather metrics.
*   **Geoapify API:** Used in `VacationPy` to locate nearby hotels within a specific radius of filtered coordinates.

---

## Analysis & Visualizations

### WeatherPy Insights
Scatter plots are generated to analyze the relationship between latitude and major weather patterns. Linear regression lines help quantify how strongly latitude drives regional weather.

<Image src="image_agent_tag_10388689583610248390" alt="Scatter plot mapping global city longitude versus latitude to show geographic spread" caption="Global Distribution of Sampled Cities" />

### VacationPy Mapping
The dataset is filtered down to ideal vacation conditions (e.g., maximum temperature between 70°F and 80°F, low wind speed, and zero cloudiness). Interactive maps display the relative humidity of these regions alongside pinpoint markers identifying local lodging options.

<Image src="image_agent_tag_10388689583610245395" alt="Interactive map showing regional data layers and hotel information popups" caption="Vacation Interactive Map Interface" />

---

## Getting Started

### Prerequisites
Before running the notebooks, ensure the following keys are obtained:
*   An API key from [OpenWeatherMap](https://openweathermap.org/api)
*   An API key from [Geoapify](https://www.geoapify.com/)

### Project Structure
```text
├── WeatherPy/
│   ├── WeatherPy.ipynb      # Weather data aggregation and regression analysis
│   ├── VacationPy.ipynb     # Geospatial mapping and hotel filtering
│   ├── api_keys.py          # Local file holding API and Geo keys (Git ignored)
│   └── output_data/         # CSV datasets and saved PNG plot figures
└── README.md
