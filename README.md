Overview
This repository contains a comprehensive SQL database focused on global fuel price trends from 2020 to early 2024. The dataset includes weekly records for various countries and regions, capturing prices for petrol, diesel, and LPG in USD per liter, alongside Brent crude oil prices and tax percentages.

The project is designed to facilitate deep-dive analysis into how fuel costs fluctuate based on income levels, subsidy levels, and global oil market changes.

Database Structure
The core of this project is the fuel_analysis database, which consists of a primary data table and several analytical views:

1. Primary Table: fuel_data
This table stores the raw historical data with the following schema:

date: The recording date (YYYY-MM-DD).

country: Name of the country.

region: Geographic region (e.g., North America).

income_level: Economic classification (e.g., High).

subsidy_level: Level of government fuel subsidies (e.g., Low).

petrol_usd_liter: Price of petrol per liter in USD.

diesel_usd_liter: Price of diesel per liter in USD.

lpg_usd_liter: Price of LPG per liter in USD.

brent_crude_usd: Global Brent crude oil price.

tax_percentage: Applied tax percentage.

2. Analytical Views
To simplify reporting, the database includes several pre-defined views:

basic_statistics: Provides aggregate minimum, maximum, and average prices for all fuel types and Brent crude oil.

country_wise_analysis: Breaks down average fuel and crude oil prices by country.

year_wise_analysis: Conducts a year-over-year comparison of average petrol, diesel, LPG, and Brent crude prices.

Key Features
Multi-Fuel Support: Tracks Petrol, Diesel, and LPG prices simultaneously.

Economic Context: Includes data on income and subsidy levels to help analyze price disparities between different economies.

Market Correlation: Allows for direct comparison between consumer fuel prices and Brent crude oil market rates.

Getting Started
Ensure you have MySQL 8.0+ installed.

Clone this repository.

Import the database using the provided SQL dump:

Bash
mysql -u your_username -p < global_fuel_data.sql
Example Analysis
You can easily query the views for instant insights:

SQL
-- View average petrol prices by year
SELECT year, avg_petrol_price FROM year_wise_analysis;

-- Compare fuel prices by country
SELECT country, avg_diesel_price FROM country_wise_analysis;
Data Source
The data contained in this repository covers a historical period including the significant market shifts of 2020 through early 2024.
