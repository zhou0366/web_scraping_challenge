# web_scraping_challenge

## Part 1: Scrape Titles and Preview Text from Mars News

In this part, we are scraping the following web page: https://static.bc-edx.com/data/web/mars_news/index.html

We begin by following importing, opening the browser, opening the web page, and creating a BeautifulSoup object as done in previous module 11 exercises.

To extract all text elements, we are looking for the class name "list_text" on the web page. These all contain classes "list_text", "list_date", "content_title", "article_teaser_body" which care used in later steps.

To create a list of articles, we want to get the article titles and article summaries. To do this, we are looping through each article's container collected previously and creating a list which will retrieve web page items with class "content_title" for the title and "article_teaser_body" for the summary. These will then be added to the main articles list. The final result will be a list of all article titles and summaries output at the end of the jupyter notebook.

## Part 2: Scrape and Analyze Mars Weather Data

In this part, we are scraping the following web page: https://static.bc-edx.com/data/web/mars_facts/temperature.html

We begin by following importing, opening the browser, opening the web page, and creating a BeautifulSoup object as done in previous module 11 exercises.

To retrieve all rows of data items, we are looking for the class name "data-row". When storing this in a list, we append the list with all items with each 'td' containers in the data rows collected from the website. We add this data into a dataframe and label the columns to correspond with the data item names on the web page. As all items in the dataframe are objects, we will need to convert them to proper variable types by first casting them as type string and then as types according to requirements laid out in the assignment page.

Now that the data has been gathered, we are can do analysis for the following questions:

1. How many months exist on Mars?

By using nunique count in the months column, we can determine that there are 12 unique months in the mars data dataframe.

2. How many Martian (and not Earth) days worth of data exist in the scraped dataset?

By using nunique count in the sol column, we can determine that there are 1867 days of data in the dataframe.

3. What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:

By grouping by months and taking the mean of temperature data, we can see the following average minimum temperatures:

By sorting the months's averages, we can see that the third month has the lowest temperature and the eigth month has the highest.

4. Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:

By plotting the average perssures by month, we can see that the lowest pressure average occurs on the sixth month and the highest occures on the ninth month.

5. About how many terrestrial (Earth) days exist in a Martian year? To answer this question:

When we plot all data entries by minimum temperature vs number of terrestrial days, we can see that the minimum temperature fluctuates somewhat regularly once every 700 terrestial days.
