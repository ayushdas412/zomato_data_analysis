# Zomato Bangalore Restaurants — Exploratory Data Analysis

A Python-based Exploratory Data Analysis (EDA) project designed to load, clean, and visualize the Bangalore restaurants dataset (`address`, `name`, `online_order`, `book_table`, `rating`, `votes`, `location`, `cuisines`, `cost_per_person`, `type_of_restaurant`).

## Overview

This repository provides a structured workflow to inspect restaurant listings across Bangalore, handle unrated entries and missing values, and uncover insights around popular neighborhoods, dining formats, pricing, and customer ratings.

## Dataset Columns

| Column | Description |
| :--- | :--- |
| `address` | Full street address of the restaurant |
| `name` | Name of the restaurant |
| `online_order` | Whether online ordering is available (`Yes` / `No`) |
| `book_table` | Whether table booking is available (`Yes` / `No`) |
| `rating` | Customer rating out of 5 (`0` indicates unrated) |
| `votes` | Total number of customer votes |
| `location` | Neighborhood or locality in Bangalore |
| `cuisines` | Comma-separated list of cuisines offered |
| `cost_per_person` | Approximate dining cost per person (in INR) |
| `type_of_restaurant` | Dining category (e.g., `Delivery`, `Dine-out`, `Desserts`, `Cafes`, `Buffet`, `Drinks & nightlife`, `Pubs and bars`) |

## Analysis Workflow

1. **Setup & Data Loading**
   - Imports `pandas`, `numpy`, `matplotlib`, and `seaborn`.
   - Loads the CSV dataset and drops any redundant `Unnamed: 0` index column.
2. **Data Cleaning & Summary Statistics**
   - Converts `rating`, `votes`, and `cost_per_person` to numeric types.
   - Replaces `0` ratings with `NaN` so unrated restaurants do not skew rating averages.
   - Summarizes missing values and descriptive statistics.
3. **Top Locations & Restaurant Types**
   - Plots horizontal bar charts for the top 10 Bangalore locations by listing count and the distribution across restaurant types.
4. **Rating & Cost Per Person Distributions**
   - Visualizes histograms with KDE curves for cleaned ratings and per-person cost (INR).
5. **Online Ordering, Table Booking & Top-Rated Restaurants**
   - Calculates percentage availability for online ordering and table booking.
   - Filters for restaurants with at least 500 votes, removes duplicate branch entries, and lists the top 15 highest-rated restaurants.

## Prerequisites & Installation

Install the required Python libraries before running the notebook:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

## Usage

1. Place your CSV dataset (e.g., `bangalore_restaurants.csv`) in the same directory as the notebook (`zomato-v4.ipynb`), or update the `FILE_PATH` variable in the notebook to match your file path.
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open the notebook and run all cells sequentially.
