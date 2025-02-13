# Anchorage Single Family Home Web Scraper and Price Analysis

# Overview

The purpose of this web scraper is to collect residential property information from the Municipality of Anchorage website.   The web scraper was written in Python and uses the libraries Selenium for web scrapping and Openpyxl for collecting the data in Excel.

# Results

The chart below shows the range of prices for a single-family home in Anchorage for each region.

![image 5](/images/image5.png)

Using multivariate regression, the chart below shows the cost of an average single-family home in Anchorage.  Region 76 equates to Girdwood, which has the highest prices, and the region with the lowest single-family homes is East Anchorage.

![image 6](/images/image6.png)

# Web Scraper

# Demo

Below is a demo video of the web scraper and a brief explanation.

1) Opened MoA_Property_Information_empty.xlsx to show all cells are empty.

2) Ran the web scraper to collect data from two different houses.

3) Opened MoA_Property_Information_empty.xlsx again to show that information from the two houses were collected.

4) Opened MoA_Property_Information.xlsx to show the data collected for over 30,000 houses after running the web scraper.

![demo](/images/Property_Web_Scraper_Demo.gif)

# Links

[My Kaggle Notebook of Anchorage Single Family Home Anaylsis](https://www.kaggle.com/nathanoliver/anchorage-single-family-home-anaylsis)

[Anchorage Municipality Public Inquiry Website (site to be web scrapped)](https://www.muni.org/pw/public.html)

# Files

There are three main files included in the [repository](https://github.com/denaliyinuo/Web_Scraper_Property_Values).

- anchorage_property_value_web_scraper.py

  This is the Python file that runs the program.  The program only needs this file and the MoA_Property_Information_empty.xlsx file to run properly.

- MoA_Property_Information_empty.xlsx

  When the program runs, the program is currently written to copy and save the information into this excel file.

- MoA_Property_Information.xlsx

  This excel file is all the information I web scraped from the website, which includes over 30,000 data points.

# Anchorage Municipality Public Inquiry Home Page

Below is an image of the home page to search for any property in Anchorage.  There are several different search options for the user to find the property in question, such as street address, name, and description.  For this web scraper, I took advantage of the parcel number option. Since each property has an associated number, the program can cycle through all of the properties in the Anchorage area, while ensuring that no properties have been missed.

![image 1](/images/image1.jpeg)

# Web Scraper Steps
# Step 1

The web scraper enters the parcel number, as shown in the red box.  In order to start from the lowest numbered property, it is recommended to input 000-00-000-000.  The search page results will show the lowest numbered property.  After the parcel number has been entered, the program will press the search button.

![image 2](/images/image2.jpeg)

# Step 2

The search results present different properties, showing the parcel number, address, and owner's name or names.  The program will select the link in the first row, shown in the red box.  The program will also copy the parcel number in the second row, shown in the blue box.  This parcel number is copied because it will be saved and used in the succeeding property search.   

![image 3](/images/image3.jpeg)

# Step 3

All of the information shown in blue boxes is copied and stored in an Excel file.  The information copied includes property prices, address, house and lot sizes, and other pertinent information.  The New Search link shown in the red box is then clicked, which brings the browser back to the home page shown in step 1, allowing the program to continue collecting information.

![image 4](/images/image4.jpeg)

