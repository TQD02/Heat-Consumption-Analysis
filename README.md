# Heat-Consumption-Analysis

_**Project Goal:**_

The goal of this project is to analyze historical heating consumption in New York State to determine if a significant trend or pattern can be observed over time. This analysis will help evaluate whether energy use for heating has increased, decreased, or remained stable across the years 2013 to 2021.

_**Part 1: Web Scraping**_

We accessed data from the U.S. Energy Information Administration (EIA) using the following URL:
https://www.eia.gov/dnav/ng/hist/nga_epg0_vgth_sny_btucfm.htm

Using Python libraries like BeautifulSoup, requests, and lxml, we scraped the relevant HTML table containing monthly consumption data (in billion Btu) for each year from 2013 to 2021.

_**Part 2: Data Cleaning & Preparation**_

Each row corresponding to a year’s worth of monthly data was extracted and cleaned to remove HTML tags and unwanted characters (like \xa0, commas, and whitespace). The results were organized into a pandas DataFrame with:

Rows representing each month (Jan–Dec)

Columns for each year from 2013 to 2021

  Data cleaning steps included:

Removing HTML tags using regular expressions

Converting string values to numeric using a custom tidy() function

Structuring the data with clear column headers and consistent formatting

_**Part 3: Data Merging & Structuring**_
We divided the data into three chunks (2013–2015, 2016–2018, 2019–2021) and then merged them using pandas' .merge() on the "Year" (month) column to ensure a consistent time-based structure.
After merging, we obtained a final DataFrame of shape (12, 10), representing monthly heating consumption across 9 years.

_**Part 4: Analysis**_

Convert All Values to Numeric
Trend Visualization
