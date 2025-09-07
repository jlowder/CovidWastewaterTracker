# CDC Wastewater Surveillance Dashboard

A real-time data visualization dashboard for monitoring COVID-19 wastewater surveillance data in your state. This application fetches live data from the CDC's National Wastewater Surveillance System (NWSS) and provides interactive visualizations to track viral activity levels through wastewater indicators.

## Features

- 📊 **Interactive Time Series Charts** - View COVID-19 wastewater viral activity levels over time
- 🌍 **Multi-Level Comparison** - Compare State/Territory, National, and Regional WVAL data
- 📅 **Flexible Date Periods** - Filter data by All Results, 1 Year, 6 Months, or 45 Days
- 🔄 **Real-Time Data Refresh** - Fetch the latest data from CDC's public API
- 📈 **Summary Statistics** - Current, average, and peak WVAL values
- 🥧 **Activity Level Distribution** - Pie chart showing distribution of activity categories
- 📋 **Raw Data Access** - Expandable table with complete dataset
- 🎨 **Color-Coded Categories** - Visual representation of activity levels (Very Low to Very High)

## Data Source

This dashboard uses data from the CDC's National Wastewater Surveillance System (NWSS):
- **API Endpoint**: https://www.cdc.gov/wcms/vizdata/NCEZID_DIDRI/SC2/nwsssc2stateactivitylevelDL.csv
- **Update Frequency**: Data refreshed when clicking "Refresh Data" button

## WVAL Categories

- 🟦 **Very High**: Highest viral activity detected (WVAL > 8)
- 🔷 **High**: Elevated viral activity (WVAL 5-8)
- 🔹 **Moderate**: Moderate viral activity (WVAL 3-5)
- 🔸 **Low**: Low viral activity detected (WVAL 1-3)
- ⬜ **Very Low**: Minimal viral activity (WVAL < 1)

