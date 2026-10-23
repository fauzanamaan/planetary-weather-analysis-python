# Planetary Weather Analysis

pandas and Plotly analysis of weather readings from a planetary rover, used to estimate the length of the planet's year and identify it as Mars.

**Notebook:** [M6_Planetary_Weather_Data_Analysis.ipynb](M6_Planetary_Weather_Data_Analysis.ipynb)

This is a milestone project from the Global Career Accelerator program. The scenario and data come from the program. It is not work done for NASA.

## Context

The scenario casts the analysis as a NASA internship. The dataset holds daily weather readings from a rover on a planet whose name is not given. The task is to inspect and clean the data, find seasonal patterns, and work out which planet it is.

## Tools and skills

- Python, pandas, Plotly Express, Jupyter
- Inspecting data: `shape`, `info`, `describe`, null counts
- Dropping columns that hold no usable data
- `groupby` with averages
- Bar charts and time-series line charts

## Approach

1. Inspected the data: 1,894 rows and 10 columns, data types, missing values and summary statistics.
2. Dropped `wind_speed` (no values at all) and `atmo_opacity` (every reading is "Sunny" apart from three `--` entries).
3. Averaged minimum temperature and pressure by planetary month and charted both.
4. Charted daily pressure and daily minimum temperature over time.
5. Estimated the length of a year from the distance between peaks, then matched it to a planet.

## Key findings

- **Wind speed was never recorded**, and minimum temperature, maximum temperature and pressure are missing on 27 days.
- **Month 3 is the coldest month** (average minimum -83.3 °C) and **Month 8 the warmest** (-68.4 °C).
- **Peaks in the daily charts repeat about every 675 Earth days**, so a year on this planet is roughly 1.85 Earth years.
- **That year length matches Mars.**

The optional LevelUp extension at the end of the notebook (working out how many Earth days fall in each planetary month) was not completed.

## How to run

The data file is not included (see [datasets/README.md](datasets/README.md)). The notebook keeps its saved outputs, so it can be read on GitHub without running anything.

To run it yourself:

1. Place `planet_weather.csv` in `datasets/`.
2. Open `M6_Planetary_Weather_Data_Analysis.ipynb` in Jupyter and run the cells from the top.

Requirements: Python 3 (the notebook was saved with Python 3.10.6), pandas, plotly and Jupyter. Package versions were not recorded.

## Repo structure

```
planetary-weather-analysis-python/
├── M6_Planetary_Weather_Data_Analysis.ipynb   analysis notebook with saved outputs
└── datasets/
    └── README.md                              which data file goes here
```
