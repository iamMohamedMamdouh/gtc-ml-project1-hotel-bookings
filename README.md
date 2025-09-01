# Hotel Booking Demand – Data Preprocessing
# Project Overview

### The goal of the project is to prepare and process hotel booking data to be suitable for building predictive models in the future.

### The project consists of three main phases: EDA, Data Cleaning, and Feature Engineering & Preprocessing.


File used: hotel_bookings.csv

Contains booking data for two hotels (City Hotel & Resort Hotel).

Columns include: booking dates, customer information, length of stay, number of people, payment methods, etc.

# Phase 1 – Exploratory Data Analysis (EDA)

Examine the general structure of the data (.info(), .describe()).

Analyze missing values ​​using tables and visualizations.

Detect outliers using boxplots and IQR.

Write a Data Quality Report to identify columns that need cleaning.

# Phase 2 – Data Cleaning

Address Missing Values:

company and agent → "None".

country → Mode or "Unknown".

children → Median/Mode.

Remove duplicates.

Process outliers (e.g., setting a cap on the adr value).

Convert data types (e.g., converting dates to datetime).

# Phase 3 – Feature Engineering & Preprocessing

Create new features:

total_guests = adults + children + babies.

total_nights = stays_in_weekend_nights + stays_in_week_nights.

is_family (family reservation).

Encoding for categorical variables:

One-Hot Encoding (for variables with low cardinality).

Grouping rare categories as "Other".

Remove columns with leaky information:

reservation_status and reservation_status_date.

Split the data into a Train/Test split (80/20).

Not Included (Out of Scope)

Build predictive models.

Hyperparameter tuning.

Model evaluation.

# Project Structure
### ├── hotel_bookings.csv
### ├── notebook.ipynb # Contains code and analytics
### └── README.md # Project description
