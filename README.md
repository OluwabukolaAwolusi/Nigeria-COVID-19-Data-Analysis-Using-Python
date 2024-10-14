
# Nigeria-COVID-19-Data-Analysis-Using-Python
Data Scientist Microdegree Capstone Project

**Data Collection**

- NCDC data was collected using pd.read()
- Confirmed cases, death cases, and recovered cases were collected from the John Hopkins repository
- External data such as COVID-19 external data, budget, and real GDP data were collected and saved to a DataFrame
- Basic information was obtained using .head() and .info() to check data types


**Data Cleaning and Preparation**

- Global confirmed, recovered, and death COVID-19 cases dataset was indexed to locate Nigeria's data
- Data was passed into a list and dictionary to create a new table containing COVID-19 death, confirmed, and recovered cases for Nigeria
- Numerical data types were cleaned by removing commas using .replace(',','') and converting to appropriate data types


**Analysis**


**Top 10 States by Confirmed Cases**

- Determined using .sort_values() with Lagos state accounting for the top state
- Visualized using a bar chart with Lagos state having over 25,000 laboratory-confirmed COVID-19 cases


**Daily Infection Rate**

- Plotted using .diff() function to determine the date with the highest infection rate
- Date with the highest infection rate occurred on 2020-02-12 00:00:00


**Relationship Between External Dataset and NCDC COVID-19 Dataset**

- Determined using pd.merge() method on the state column
- Relationship between confirmed cases and Overall CCVI Index was plotted using axis1.plot() and axis2=axis1.twinx()


**Regression Plot**

- Determined using sns.regplot() between population density and confirmed cases
- Regression between number of deaths and confirmed cases was high, with a correlation of 0.9258264780306408


**Further Analysis**

- Acute IHR was plotted against states using plt.plot() method
- Health system by states was plotted using plt.plot() method to determine access to healthcare and healthcare performance


**Effect of the Pandemic on the Economy**

- Real GDP value pre-COVID-19 versus Real GDP in 2020 (COVID-19 period, Q2 2020)
- Data was plotted using a bar chart with a figure size set to (10,6) for clearer view


**Budget Analysis**

- Barh chart was used to visualize states with the highest revised and initial budget
- Top ten states by health systems and revised budget were plotted


**Analysis of Different Phases**

- Lockdown phases were assigned using pd.cut() function
- Total confirmed cases for each phase were calculated using df.groupby() function

  **FUTURE WORK**
  Conduct a comparative analysis with other African countries,Develop predictive models to forecast COVID-19 cases, hospitalizations, and deaths.Investigate the long-term effects of COVID-19 on healthcare systems, economy, and society.
