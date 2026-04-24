# NAME: Dhruv Patil

# PRN: 25070123146

# Aim:

The aim of the experiment is to perform exploratory data analysis (EDA) on a COVID-19 dataset to visualize and understand the progression of the pandemic across different countries and Indian states.

## Theory:

The analysis utilizes Python for data manipulation and visualization. Key concepts include:

    Data Cleaning: Removing unnecessary columns (like serial numbers or metadata), converting string date formats to datetime objects, and filling missing values.

    Feature Engineering: Calculating the "Active" cases using the formula: Active = Confirmed - Recovered - Deaths.

    Data Aggregation: Grouping data by date and location (Country/Region and Province/State) to analyze trends over time and geographical distribution.

    Visualization: Using choropleth maps to represent spatial distribution of cases.

Key Commands Used:

The following commands and operations were used in the analysis:

Loading and inspecting data:

    pd.read_csv("/content/covid_19_data.csv")

    data.head()

    data.info()

   Data Preprocessing:

    data.drop(['SNo','Last Update'], axis=1): Drops irrelevant columns.

    data['ObservationDate'].astype('datetime64[ns]'): Converts the date column to a usable datetime format.

    data.fillna(0): Handles missing values by replacing them with zero.

  Calculations and Aggregation:

    data['Active'] = data['Confirmed'] - data['Recovered'] - data['Deaths']: Creates the Active cases column.

    data.groupby("Country/Region")[...].sum(): Aggregates statistics by country.

Visualization:

    px.choropleth(...): Creates interactive world and India maps to visualize case distributions.

## Conclusion: 

The experiment successfully processes and visualizes the COVID-19 dataset. By performing data cleaning and feature engineering, the analysis allows for a clear view of the spread of the virus. Key findings from the processed data included:

Global distribution of confirmed and recovered cases can be effectively visualized on world maps.

In India, Andhra Pradesh was identified as the state with the highest number of confirmed cases based on the provided dataset.

Temporal trends show a continuous rise in cumulative confirmed, death, and recovery figures over the duration of the dataset.
