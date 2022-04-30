# sfpd_incident_analysis
A Tableau dashboard on San Francisco crimes

## Project Overview
The purpose of this project was to create a Tableau dashboard on San Francisco crimes as documented by the SFPD. The dashboard is filtered to exclude 2022 to account for data in years only with complete months. Data inspection and cleaning was done using Python. 

### Resources
- [SFPD Incident Report](https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-2018-to-Present/wg3w-h783)
- Software: Tableau, Jupyter Notebook
- Language: Python
- [Data inspection and cleaning](https://github.com/samanthajpv/sfpd_incident_analysis/blob/main/data_inspection.ipynb)
- [Link to Tableau Dashboard](https://public.tableau.com/app/profile/samantha.villanueva/viz/SFPDIncidentReport-CrimeDashboard/Dashboard1)

## Data Inspection and Cleaning

- Columns not needed were removed and some datetime transformations were applied.
- 'Incident Category' was cleaned by standardizing similar categories. Those with null values were filled in based on the 'Incident Description' column since the subcategory also shows null.
- Note that geographic location is not available for all rows. Those with no geolocation were not removed to show how many incident reports do not have location information in the 'Neighborhood' section of the dashboard.

## Visualizations

- **Neighborhood**, **Police District**, & **Crime Map**: All three visualizations show that most crimes happen downtown San Francisco. It can be confirmed by the number of crimes committed and the density as seen in the map.
- **Incident Category**: 'Larceny Theft' is the most common crime with almost a third of all the reported crimes. It's followed by 'Other Miscellaneous' which is comprised of a lot of different crimes labeled as 'Other' in the subcategory.
- **Yearly Incident Count**: shows the count and percentage increase/decrease of crime from 2018 to 2021.
- **Monthly Incident Count**: shows month to month comaprison of crime rate regardless of the year.
- **Day and Hour of Incident** - shows crime rate occurrence regardless of the month and year. A lot would think that crimes happen late at night but the dahboard reveals that most crimes happen midday and late in the afternoon.  

## Improvement
 - Further refine the "Other Miscellaneous' incident cateogry to more specific labels
 - create a tableau story to show a deeper dive into each visualization
 - add filter in the dashboard to exclude rows with null information
 - make a year to year comparison of crime rate

