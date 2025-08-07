# Integrated-project-Access-to-drinking-water

<img width="259" height="195" alt="water-supply" src="https://github.com/user-attachments/assets/e56d53cb-5f6a-49ba-bad9-aa6cf86db2a7" />

In this project I exhibit my **Spreadsheet** skills using **Google Sheets** and I was able to perform all data `import,` `retrieve,` `manipulation,` `cleaning,` and `visualization` of the dataset.

Understanding the data,  we’ll investigate access to safe and affordable drinking water.

[You can access the main project solutions Google spreadsheet here](https://docs.google.com/spreadsheets/d/1VKogBApZeoFOVw0v_qDp6wEy-GAEuo3m0rX0wJ0HdGA/edit?gid=1722416536#gid=1722416536)


# Becoming familiar with the dataset

We’ll take a look at the WHO/UNICEF JMP (Joint Monitoring Programme for Water Supply, Sanitation, and Hygiene) Estimates on the use of water dataset for (2000-2020).


- ``name``
The country or area name.

- `income_group`
The country’s classification according to income group.

- `pop_n`
The national population size estimate, in thousands.

- `pop_u` 
The urban population share estimate in percentage points (%).

- `_wat_bas_n_` 
The estimated national share of people with at least basic service (%)*.

- `_wat_lim_n_` 
The estimated national share of people with limited service (%).

- `_wat_unimp_n_` 
The estimated national share of people with unimproved service (%).

- `_wat_sur_n_` 
The estimated national share of people with surface service (%).
 
- `_wat_bas_r_` 
The estimated rural share of people with at least basic service (%).

- `_wat_lim_r_` 
The estimated rural share of people with limited service (%).

- `_wat_unimp_r_` 
The estimated rural share of people with unimproved service (%).

- `_wat_sur_r_` 
The estimated rural share of people with surface service (%).

- `_wat_bas_u_` 
The estimated urban share of people with at least basic service (%).

- `_wat_lim_u_` 
The estimated urban share of people with limited service (%).

- `_wat_unimp_u_` 
The estimated urban share of people with unimproved service (%).

- `_wat_sur_u_` 
The estimated urban share of people with surface service (%).

We have a total of 16 features (or columns) in our dataset, 12 of which are service-level percentage shares.

## Process of Investigations that was consider on the Dataset:

1. **Investigating year representation**
   
   In order to understand what our dataset represents, we need to investigate when and how often data were collected.
   
   -  During which years was this data recorded?
     
      To observe which years are represented for which countries, we sort both by name and year.
      
   -  What is the average number of years between data collections per country?
     
      Calculate the average difference in years for data entries per country.

2. **Investigating Annual Rates of Change (ARC)**

   We want to see if access to services is improving or declining across national, urban, and rural areas.
   
   The United Nations (UN) uses Annual Rates of Change (ARC) to see whether the proportion of access to drinking water is declining or improving.

   - What is the ARC for the national, rural, and urban areas per country?
  
     Calculate ARC per country, i.e. only calculate the ARC between two years of the same country name.
  
   - What is the average of the different ARCs for all countries?
  
     Calculate the average, minimum, and maximum for each of the ARC values for access to the basic service level for each of the three population groups.

3. **Investigatingaccess by area**

   Now, we want to investigate whether countries have made significant enough effort to improve this in the years leading up to 2020.

   - What does the change in access to basic water look like for different areas?
  
     Calculate the number of countries per area that have full access and Annual Rates of change equal to zero, smaller than zero, and greater than zero.
  
   -  How does the ARC differ between rural and urban populations?
  
      Calculate the difference between the Annual Rates of change between rural and urban populations per country.

4. **Investigating access by region**

   The UN often uses classification by region as a way to group various countries and investigate a region’s progress in the SDGs.

   We want to investigate whether more or less progress has been made in increasing access to basic water services in specific regions across the world.

   - How does ARC compare across different regions?
  
     Our original dataset didn’t include region information, so we’ll have to amend our dataset to investigate access by region.

     Import the Regions.csv into a new sheet.  Add a new column to the original dataset called region, and use any LOOKUP function to add the region based on the country name.
  
   - What is the influence of national population size on the ARC?

     Visualize access by region to investigate the relationship between the national and rural Annual Rates of change, as well as population size and region.
 
     Create a visualization that represents the national ARC versus the rural ARC, as well as the region and national population size.

# Visualization


<img width="600" height="371" alt="AVERAGE of ARC_n and AVERAGE of ARC_r" src="https://github.com/user-attachments/assets/d4432d70-41b0-48ac-8965-55c2b4a68190" />

Average of ARC_national, Average of ARC_rural and the Regions using Bar charts

<img width="600" height="371" alt="AVERAGE of pop_n vs  Region" src="https://github.com/user-attachments/assets/a12f28c5-2d50-4bd0-b440-c55b6ac47b3c" />

Average of ARC_national and the Regions using Histogram charts

<img width="600" height="371" alt="Histogram of year" src="https://github.com/user-attachments/assets/8f99b23a-0d00-4f5d-b37f-1275a9e388cb" />

Improvement of years from 2000 - 2022 Histogram chart

<img width="600" height="371" alt="ARC_n and ARC_r" src="https://github.com/user-attachments/assets/77cd4de6-65c3-4235-b421-c9b293c71ab2" />

AVerage ARC_national and Average ARC_rural using Line chart

<img width="600" height="371" alt="Histogram of ARC_diff" src="https://github.com/user-attachments/assets/09ccf5be-7d3a-4dc9-8a22-26493a99357e" />

Difference between ARC for all national_pop for countries Histogram chart

# Summary

1. **Becoming familiar with the dataset**

   Original 16 features in the column but as we progress with the analysis more columns where formed.

2. **Investigating year representation**

   New column formed `(y_diff).` A summary of the dataset year and year difference, including the median, minimum, and maximum.

    A histogram of the year column.

3. **Investigating Annual Rates of Change (ARC)**

   New columns formed `(ARC_n, ARC_r, ARC_u).`  The median, minimum, and maximum of each of the three newly created ARC columns based on the national, rural, and urban change in access.

4. **Investigating access by area**

   New columns formed `(wat_bas_n (rounded), wat_bas_r (rounded), wat_bas_u (rounded), ARC_n_full, ARC_r_full, ARC_u_full, ARC_diff).` The number of countries that have no ARC value, full access, `ARC < 0, and ARC > 0` for each of the three newly created ARC columns.
 
  A histogram of the difference in ARC values for rural versus urban areas.

5. ** Investigating access by region**

   New Dataset imported `(Region).` A summary per region that at least includes the number of countries per region, the average ARC on a national level, and the average ARC values in rural and urban areas.

   A visualization (of choice) that represents the national `ARC, rural ARC,` region, and population size.

# Conclusion

Through my Data investigations I was able to analyze, and discover the following insights from our dataset:

- The average-differences of countries that have good and poor drinking-access-to-water-supply, sanitation, and hygiene

- The Annual Rate of Change (ARC) of each nations improvement to water-supply, sanitation and hygiene per year

- The countries with full access to water-supply

- The countries with low rate of water-supply, sanitation and hygiene.


