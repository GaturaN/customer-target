**Customer Analysis and Targeting Application**

This Python application is designed to analyze customer data, identify key insights, and target specific customers within a certain radius of a reference location using the Google Maps API. The application is implemented in a Jupyter Notebook and leverages various Python libraries, including pandas, numpy, and matplotlib.

**Getting Started**

`1.` Install the required libraries:
+ pandas
+ numpy
+ matplotlib
+ googlemaps

`2.` Replace 'YOUR_API_KEY' in the code with your actual Google Maps API key.

`3.` Ensure you have the customer data in the Excel file format (Customer data.xlsx) with relevant columns such as 'Document Date', 'Customer/Vendor Name', 'Item Name', and 'Quantity'.

**Data Cleaning and Analysis**

 The application begins by loading the customer data into a pandas DataFrame, followed by performing data cleaning and analysis:

`1.` Identifying missing values: The application checks for missing values and drops the rows with missing cells to ensure a clean dataset.

`2.` Getting the days of the week with the most orders: The application extracts the day of the week from the 'Document Date' column, groups the data by day of the week, and calculates the total quantity of orders for each day. It then determines the day(s) with the most orders and visualizes the results in a bar chart.

`3.` Identifying the top 3 products per week: The application extracts the week number from the 'Document Date' column, groups the data by week number and product, and calculates the total quantity of each product sold per week. It then identifies the top 3 products for each week and presents the results in a DataFrame.

`4.` Finding the best performing customers: The application groups the data by 'Customer/Vendor Name' and counts the number of orders for each customer. It then calculates quartiles to determine the target customers falling within the 2nd and 4th quartiles.

**Targeting Customers Using Google Maps API**

The application uses the Google Maps API to locate the best performing customers and retrieve their contact information:

`1.` Retrieving location and contact details: The application uses the Google Maps API to retrieve the address, geolocation (latitude and longitude), phone number, website, and opening hours of the target customers.

`2.` Calculating distance to a reference location: The application calculates the haversine distance between the target customers' locations and a reference location (Unga House in Nairobi, Kenya). It filters the target customers within a 10 km radius of the reference location and saves the filtered data to a new Excel file.

**Important Note**
* Ensure you have a valid Google Maps API key and comply with Google's Terms of Service and usage policies when using the API.
* Be mindful of Google Maps API usage limits and potential billing implications based on the number of requests made.
* The application assumes that the customer data is stored in the 'Customer data.xlsx' file and contains the necessary columns for analysis. Modify the data file and column names accordingly if needed.
