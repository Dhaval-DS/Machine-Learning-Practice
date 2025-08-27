Web Scraping Project: Quotes to Scrape
This project demonstrates web scraping using Python to extract data from the "Quotes to Scrape" website. The script gathers quotes, author names, and their associated tags from the first 10 pages of the site.

Data Source
The data was scraped from 

Quotes to Scrape, a website designed for web scraping practice.

Methodology
The scraping process follows these steps:

Sends an HTTP 

GET request to each of the first 10 pages of the website.

Parses the HTML content of each page using 

BeautifulSoup.

Locates and extracts the quote, author, and tags from the relevant HTML elements.

Stores the extracted data in a pandas DataFrame.

Concatenates the data from all pages into a single DataFrame and exports it to a CSV file.

Technologies Used 💻
Python


Requests: For making HTTP requests.


BeautifulSoup4: For parsing HTML and extracting data.


Pandas: For data manipulation and exporting to CSV.


Jupyter Notebook: As the development environment.

Output
The final output is a CSV file named 

quotes.csv containing 100 quotes with the following columns:


Name of Author: The name of the person who said the quote.


Quote: The full text of the quote.


Tags: A list of tags associated with the quote.
