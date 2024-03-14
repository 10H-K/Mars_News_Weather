# Scraping And Previewing Mars News Articles

## Overview ##

The goal of this portion of the project is to scrape titles and preview text from Mars news articles.

## Process ##

A) Visiting Mars News Website Through Automated Browsing, Inspecting Elements to Scrape:
  1. Importation of dependencies (Splinter And BeautifulSoup)
  2. Using automated browsing to visit the Mars news site
  3. Inspecting the Mars news site to identify which elements to scrape

B) Scraping Mars News Website:
  1. Creating a Beautiful Soup object and using it to parse the website HTML
  2. Extracting all the list text elements for each article
  3. Printing the list text elements for each article

C) Storage Of Results:
  1. Creating empty list to store the dictionaries
  2. Looping through all the list text elements:
     - Extracting each article title/preview
     - Storing the title/preview as pairs in dictionary
     - Adding each created article dictionary to list 'titles_previews'
  4. Printing the 'titles_previews' list to confirm success
  5. Quitting the browser

---

# Scrape And Analyze Mars Weather Data

## Overview ##

The goal of this portion of the project is to scrape and analyze Mars weather data, which exists in an HTML table.

## Process ##

A) Visiting Mars Temperature Data Website Through Automated Browsing, Inspecting Elements to Scrape:
  1. Importation of dependencies (Matplotlib, Pandas, Splinter, and BeautifulSoup)
  2. Using automated browsing to visit the Mars temperature data website
  3. Inspecting the Mars temperature data site to identify which elements to scrape

B) Scraping Mars Temperature Data Website:
  1. Creation of Beautiful Soup object and using it to parse the website HTML
  2. Extracting all rows of temperature data from the HTML table

C) Storage Of Results:
  1. Creation of empty list to store the Mars temperature data
  2. Looping through the scraped data to create a list of rows of data:
     - Finding all table cells in the row
     - Extracting text from each cell and creating a row
     - Appending the row to the list 'mars_temperature_data'
  3. Printing the 'mars_temperature_data' list containing all rows created from the scraped data
  4. Creating Pandas DataFrame by using list of rows and list of column names
  5. Confirming DataFrame created successfully

D) Preparing Data For Analysis:
  1. Examining data type of each column
  2. Changing data types for subsequent data analysis
  3. Confirming data type changes were successful by examining data types again

E) Analyzing The Data Through Questions:
  1. How Many Months Are There On Mars?
     - Calculating number of unique months in 'month' column of Mars temperature DataFrame
     - Printing the result
  2. How Many Martian Days' Worth Of Data Are There?
     - Calculating total number of Martian days by counting length of 'sol' column in Mars temperature DataFrame
     - Printing the result
  3. What Is The Average Low Temperature By Month?
     - Grouping Mars temperature DataFrame by 'month' column, computing mean of 'min_temp' column
     - Displaying the result
     - Creating plot for average low temperature by month
        - Setting plot labels and title
        - Showing plot

      ![output](https://github.com/10H-K/Web_Scraping/assets/152930492/b2cffc23-7eb0-40b7-828f-2374c0fb6369)

     - Identifying the coldest and hottest months in Curiosity's location through plotting
        - Setting plot labels and title
        - Showing plot

      ![output](https://github.com/10H-K/Web_Scraping/assets/152930492/69d99418-79ef-4291-a1d9-0823c46a853c)

  3. What Is The Average Pressure By Martian Month?
     - Grouping Mars temperature DataFrame by 'month' column, computing mean of 'pressure' column
     - Displaying the result
     - Creating plot for average pressure by month
        - Setting plot labels and title
        - Showing plot

      ![output](https://github.com/10H-K/Web_Scraping/assets/152930492/c9c5ac25-0728-4ed3-bdc4-cae47987d770)

  4. How Many Terrestrial (Earth) Days Are There In A Martian Year?
     - Filtering Mars temperature DataFrame to include only rows where Solar Longitude is either 0 or 359
     - Sorting filtered DataFrame by 'terrestrial_date' column
     - Grouping sorted data by Solar Longitude and Terrestrial date, counting occurrences
     - Displaying resulting series
     - Defining two dates as strings, corresponding to Solar Longitude 0 and 359, respectively
     - Converting the date strings to Pandas datetime objects
     - Calculating the difference
     - Printing the result
     - Creating plot for minimum temperature against number of Martian days (sol)
        - Setting plot labels and title
        - Showing plot

      ![output](https://github.com/10H-K/Web_Scraping/assets/152930492/ea494470-a98d-4df1-97a1-e53ead300a4d)

F) Saving Data:
  1. Exporting the data to a csv
  2. Quitting the browser

