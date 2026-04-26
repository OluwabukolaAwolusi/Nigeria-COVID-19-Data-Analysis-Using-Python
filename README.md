[![Alt text](covid.jfif)]

Introduction 

The COVID-19 pandemic has severely impacted Nigeria, affecting its economy, healthcare system, and population. The early part of the COVID-19 crisis ushered in Nigeria deepest recession since the 1980s, with services and industry hit especially hard. The COVID-19 pandemic and aftermath have had a huge effect on Nigeria’s socioeconomic growth, affecting many parts of the country’s economy and society. One of the biggest problems has been the disruption of the economy, which has caused people to lose their jobs and see big differences in their incomes. Due to lockdowns, many companies, especially small and medium-sized ones, had to close or cut back on their hours, which hurt people’s ability to make a living and made poverty worse. This analysis aims to provide insights into the spread of COVID-19 in Nigeria, identifying high-risk states, and assessing the impact of lockdown phases on confirmed cases.

# Nigeria-COVID-19-Data-Analysis-Using-Python
Data Scientist Microdegree Capstone Project


## Data description
This project uses the covid 19 dataset from the [ustacky] https://github.com/Ustacky-dev/Nigeria-COVID-19-Data-Analysis-Using-Python repository 


## Project File
The project in this repository resides in "Capstone project(2).ipynb" file.

## Dependencies:
To run this project, install and import the following dependencies:
NumPy
Pandas
Seaborn
Matplotlib


## Data Wrangling
This section covers data acquisition, cleaning, and preparation steps performed before analysis.

### Data Collection & Loading
- **NCDC data**: Loaded from CSV using `pd.read_csv()`
- **COVID-19 case data**: Confirmed, death, and recovered cases sourced from the [Johns Hopkins CSSE repository](https://github.com/CSSEGISandData/COVID-19)
- **External datasets**: COVID-19 vulnerability index, budget data, and real GDP data imported and consolidated into a DataFrame
- **Initial inspection**: Used `.head()` and `.info()` to preview data structure and verify data types

### Data Cleaning & Transformation
- Filtered global datasets to isolate Nigeria's data by indexing on `Country/Region`
- Restructured Nigeria's confirmed, death, and recovered cases into a unified DataFrame using lists and dictionaries
- Cleaned numeric columns by removing commas with `.str.replace(',','')` and converting to appropriate numeric types
- Standardized date formats and handled missing values

## Analysis

### Top 10 States by Confirmed Cases
- States ranked using `.sort_values(ascending=False)` on confirmed cases
- Lagos State recorded the highest number with 25,000+ laboratory-confirmed cases
- Results visualized using a horizontal bar chart with `matplotlib`

### Daily Infection Rate
- Daily new cases calculated using `.diff()` on cumulative confirmed cases
- Peak infection rate occurred on `2020-02-12`
- Trend visualized using a time series line plot
![alt text](<daily infection rate.png>)
### Relationship Between External Dataset and NCDC COVID-19 Dataset
- External vulnerability data merged with NCDC data on `state` using `pd.merge()`
- Relationship between confirmed cases and Overall CCVI Index visualized using a dual-axis plot with `ax1.twinx()`

### Regression Analysis
- Used `sns.regplot()` to examine correlation between population density and confirmed cases
- Strong positive correlation found between confirmed cases and deaths: `r = 0.9258`
- Linear relationships visualized with regression plots

### Further Analysis
- Acute IHR capacity scores plotted by state using `plt.plot()` to assess health emergency preparedness
- Health system performance metrics visualized by state with `plt.plot()` to evaluate healthcare access and infrastructure

**Effect of the Pandemic on the Economy**

- Real GDP value pre-COVID-19 versus Real GDP in 2020 (COVID-19 period, Q2 2020)
- Data was plotted using a bar chart with a figure size set to (10,6) for clearer view
![alt text](<Screenshot 2024-09-30 163551.png>)

**Budget Analysis**

- Barh chart was used to visualize states with the highest revised and initial budget
- Top ten states by health systems and revised budget were plotted


**Analysis of Different Phases**

- Lockdown phases were assigned using pd.cut() function
- Total confirmed cases for each phase were calculated using df.groupby() function
![alt text](<covid lockdphases.png>)

  **FUTURE WORK**
  Conduct a comparative analysis with other African countries,Develop predictive models to forecast COVID-19 cases, hospitalizations, and deaths.Investigate the long-term effects of COVID-19 on healthcare systems, economy, and society.
