# web-scrapping
This Python code is intended to create a simple web crawler using the BeautifulSoup library to extract links from a web page. 
# execution of code
type or copy and paste the code in google collab or any py editor
# code explaination
first we start withe import function and these are the following functions we are gonna import
os: this function imports or provides module providing operating system functionalities 
requests: it is a which is library which is imported for making HTTP requests to websites.
BeautifulSoup:It is alsp an library for parsing HTML content.

now after import we start with the initialization here we are going to give or intialise the url which is empty for now
url: An empty list ['']. It should contain the starting URL or any URl of that page to crawl from, but in this code it's empty and needs to be filled with any of the URl for eg you can take the URL of the wikipedia page

now after initialising we come into another function called vizitate 
This function helps to visit a website and extract links from it.
It opens a file named "visited.txt" in write mode and writes the site URL into it. However, the file is opened and closed within the same function call, potentially overwriting its content if this function is called multiple times.
It uses requests.get to fetch the HTML content of the site URL and then parses it using BeautifulSoup.
The HTTP headers of the site URL are printed to the console.
It searches for all anchor (<a>) tags in the HTML content and examines each one: wkt that anchor tag is a tag which contains links and is usually used to link any pages or sites
For each anchor tag, it checks if it contains an href attribute,href stands for hyper reference 

and at last the url of the page or site is printed and it crawls to that website or page


Execution:
It calls the vizitate() function with the first URL (assuming there's a URL in url[0]). This is meant to start the crawling process.
After executing vizitate(), it prints the url list which now contains the extracted links.

This code attempts to extract links from the provided URL(s) but has some issues, such as potential overwriting of the "visited.txt" file and using a global url list in a way that might not work as intended for a comprehensive web crawling task. Additionally, it doesn't handle recursive crawling or keep track of visited URLs to prevent duplicates.
