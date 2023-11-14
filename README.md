# web-scrapping
This Python code is intended to create a simple web crawler using the BeautifulSoup library to extract links from a web page. Let's break it down into steps:
# execution of code
type or copy and paste the code in google collab or any py editor
# code explaination
Imports:
os: Module providing operating system functionalities 
requests: Library for making HTTP requests to websites.
BeautifulSoup: Library for parsing HTML content.

Initialization:
url: An empty list ['']. It should contain the starting URL(s) to crawl from, but in this code, it's empty and needs to be filled with the desired URL(s).

Function vizitate(site):
This function aims to visit a website (site) and extract links from it.
It opens a file named "visited.txt" in write mode ("w+") and writes the site URL into it. However, the file is opened and closed within the same function call, potentially overwriting its content if this function is called multiple times.
It uses requests.get(site) to fetch the HTML content of the site URL and then parses it using BeautifulSoup.
The HTTP headers of the site URL are printed to the console.
It searches for all anchor (<a>) tags in the HTML content and examines each one:
For each anchor tag, it checks if it contains an href attribute (which contains the URL).
If the URL starts with a slash ('/') and doesn't contain '.pdf' (to avoid PDF files), it appends the URL to the url list. Note that url is a global list that starts as [''] and is being modified by this function.

Execution:
It calls the vizitate() function with the first URL (assuming there's a URL in url[0]). This is meant to start the crawling process.
After executing vizitate(), it prints the url list which now contains the extracted links.

This code attempts to extract links from the provided URL(s) but has some issues, such as potential overwriting of the "visited.txt" file and using a global url list in a way that might not work as intended for a comprehensive web crawling task. Additionally, it doesn't handle recursive crawling or keep track of visited URLs to prevent duplicates.
