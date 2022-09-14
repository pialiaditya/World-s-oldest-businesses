# World's-oldest-businesses

This project reinforces skills from Data Manipulation with pandas as well as Joining Data with pandas.
We use sorting, filtering and aggregation to find the oldest business in the world

We answer the following questions
TASK 1: Import the pandas library using its usual alias, pd. Load the businesses.csv file, located in the datasets folder, and save it as a DataFrame called businesses. Sort businesses by oldest to newest business, saving as sorted_business. Display the first few rows of sorted_businesses.

TASK 2: Let's join sorted_businesses with countries so we can look at data by continent. Load countries.csv from "datasets/countries.csv" and save it as a DataFrame called countries. Merge sorted_businesses with your new countries; save the merged DataFrame as businesses_countries. Filter businesses_countries to create a new DataFrame called north_america, which contains the oldest businesses for countries in North America only.

TASK 3: Lets find the oldest business on each continent Using businesses_countries as a starting point, create a continent DataFrame, which has a list of continents as its index and a single column showing the oldest (some might say minimum) year_founded. Note that continent must be a DataFrame and not a Series since .merge() cannot be used with a Series. Merge continent with businesses_countries to include data from the oldest business on each continent. Subset your new merged_continent to include just four columns: continent, country, business, and year_founded

TASK 4: For this task, we'll return to businesses and countries and use our .merge() skills to look for missing data.
Use .merge() to create a DataFrame called all_countries with all countries, regardless of whether they have business data.
Filter all_countries to include only countries without oldest businesses and save to a new DataFrame, missing_countries.
Create a pandas Series of the country names with missing oldest business data.
Display the series.

TASK 5: We want to vertically stack businesses and the information from new_businesses.csv together to create a more complete dataset.
Import new_businesses.csv as new_businesses.
Add the data in new_businesses to the existing businesses; save this complete dataset as all_businesses.
Use .merge() and filter the data as you did in the last task to identify countries with missing data in all_businesses; call this DataFrame new_missing_countries.
Group new_missing_countries by continent and display the count of missing countries in each continent; rename this column count_missing. A list of continents will be the index of this DataFrame.

TASK 6: Which industries do you think are best suited to last over the course of centuries?

Import the categories.csv data into categories and merge it with businesses to create businesses_categories.
Use businesses_categories to create count_business_cats, which lists all industry categories as its index and shows the count of oldest businesses in each of them.
Use businesses_categories to create years_business_cats which lists all industry categories as its index and shows the cumulative number of years businesses from the categories have been operating.
Rename the column in count_business_cats to be called count and rename the column in years_business_cats to be called total_years_in_business.

TASK 7: Let's find the oldest restaurants in the world.

Using .query(), filter businesses_categories so that we are only looking at CAT4 businesses ("Cafés, Restaurants & Bars") which were founded before the year 1800.
Sort your results to display the restaurants from oldest to newest.

TASK 8: Let's make a reference table showing the oldest business in each category of commerce by continent.

To begin, create a merged DataFrame called businesses_categories_countries that includes all businesses, category, and country information. Sort businesses_categories_countries from oldest to most recent year_founded. Manipulate businesses_categories_countries so that it shows a list of all continents, along with a list of all categories for each continent; then, show the year_founded for the oldest businesses in each continent-category pair. The continent-category pairs will display as the index of the DataFrame.


