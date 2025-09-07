# CDC Wastewater Surveillance Dashboard

A real-time data visualization dashboard for monitoring COVID-19 wastewater surveillance data in your state. This application fetches live data from the CDC's National Wastewater Surveillance System (NWSS) and provides interactive visualizations to track viral activity levels through wastewater indicators.

## Usage

To use the dashboard, simply open the `dashboard.html` file in a modern web browser.

Click here to try it out:

[CovidWastewaterTracker](https://jlowder.github.io/CovidWastewaterTracker/dashboard.html)

**Note on Data Fetching:** This application fetches live data directly from the CDC's public API. Due to web browser security policies (CORS), direct API requests from a local file may be blocked. The application includes a fallback mechanism using public CORS proxies to mitigate this. If you still encounter issues, running the file from a local web server or using a browser extension to disable CORS for the session are alternative solutions.

## Features

- 📊 **Interactive Time Series Charts** - View COVID-19 wastewater viral activity levels over time
- 🌍 **Multi-Level Comparison** - Compare State/Territory, National, and Regional WVAL data
- 📅 **Flexible Date Periods** - Filter data by All Results, 1 Year, 6 Months, or 45 Days
- 🔄 **Real-Time Data Refresh** - Fetch the latest data from CDC's public API
- 📈 **Summary Statistics** - Current, average, and peak WVAL values
- 🥧 **Activity Level Distribution** - Pie chart showing distribution of activity categories
- 📋 **Raw Data Access** - Expandable table with complete dataset
- 🎨 **Color-Coded Categories** - Visual representation of activity levels (Very Low to Very High)

## Technology Stack

- **HTML:** The structure of the web page.
- **JavaScript:** For fetching data, interactivity, and chart generation.
- **Chart.js:** For creating the interactive charts.

## Data Source

This dashboard uses data from the CDC's National Wastewater Surveillance System (NWSS):
- **API Endpoint**: https://www.cdc.gov/wcms/vizdata/NCEZID_DIDRI/SC2/nwsssc2stateactivitylevelDL.csv
- **Update Frequency**: Data is fetched on initial page load and can be manually refreshed by clicking the "Refresh Data" button.

## WVAL Categories

The Wastewater Viral Activity Level (WVAL) is categorized as follows:

- 🟦 **Very High**: Highest viral activity detected (WVAL > 8)
- 🔷 **High**: Elevated viral activity (WVAL ≥ 5 and ≤ 8)
- 🔹 **Moderate**: Moderate viral activity (WVAL ≥ 3 and < 5)
- 🔸 **Low**: Low viral activity detected (WVAL ≥ 1 and < 3)
- ⬜ **Very Low**: Minimal viral activity (WVAL < 1)

## Development

The application is a single HTML file with embedded JavaScript and CSS. It has no external dependencies beyond Chart.js, which is loaded from a CDN. To handle potential CORS issues when fetching data from the CDC's API, the application cycles through a list of public CORS proxies if the direct request fails.
