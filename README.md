## Project Overview
This project is a simple news website that fetches and displays news articles. It allows users to search for news by keywords and also provides pre-defined categories like "IPL," "Finance," and "Politics."

## Features
News Display: Fetches and displays news articles in a card format.
Search Functionality: Users can search for news using a search bar.
Category Navigation: Users can click on navigation links to view news related to specific categories.
Responsive Design: The website is designed to be responsive (though specific CSS for responsiveness is not detailed in the snippets).
Clickable News Cards: Each news card is clickable and opens the full article in a new tab.

## File Structure
index.html: The main HTML file that structures the webpage, including the navigation bar, search bar, and a container for news cards. It also includes a template for individual news cards.
style.css: Contains the CSS for styling the website, defining the layout, colors, and appearance of elements.
script.js: The JavaScript file that handles the core functionality:
Fetching news articles from an API.
Binding the fetched data to the HTML elements.
Handling user interactions like search and category selection.
Key Functionality Breakdown
script.js

## API Integration:
Uses a NEWSAPI_KEY (hardcoded in the snippet, should be managed securely in a real application).
Fetches data from https://newsapi.org/v2/everything?q=.
fetchNews(query): An asynchronous function that takes a search query, makes an API call, and then calls bindData with the results.
bindData(articles): Clears the existing news cards and then iterates through the fetched articles, cloning a news card template for each article and populating it with data using fillDataInCard.
fillDataInCard(cardClone, article): Takes a cloned news card template and an article object, then populates the image, title, description, source, and publication date. It also adds a click event listener to the card to open the article URL.
Navigation and Search Event Handling:
onNavItemClick(id): Handles clicks on navigation items, fetches news for the selected category, and updates the active state of the navigation item.
An event listener on the search button fetches news based on the text entered in the search input.
reload(): Reloads the current page.
index.html
Navigation Bar: Contains the company logo, navigation links (IPL, Finance, Politics), and a search bar.
Main Content Area: A div with the ID cards-container where news cards will be dynamically inserted by JavaScript.
News Card Template: A <template> element with the ID template-news-card defines the structure of a single news card, which is cloned and populated by JavaScript.
style.css
Styling: Defines styles for the overall layout, navigation, search bar, and news cards.
CSS Variables: Uses CSS variables for colors (--primary-text-color, --secondary-text-color, --accent-color, etc.) for easier theme management.
Layout: Utilizes flexbox (.flex) for layout and alignment.
Card Appearance: Styles the news cards with shadows, rounded corners, and hover effects.

## How to Run
Save the provided HTML, CSS, and JavaScript code into index.html, style.css, and script.js files respectively, in the same directory.
Ensure you have a valid NEWSAPI_KEY and replace the placeholder in script.js.
Open index.html in your web browser.

## Potential Improvements
API Key Management: Securely manage the API key (e.g., using environment variables).
Error Handling: Implement more robust error handling for API requests.
Pagination: For a large number of articles, implement pagination.
Loading Indicators: Add visual feedback while news articles are being fetched.
Accessibility: Improve accessibility by adding ARIA attributes and ensuring keyboard navigation.
More Categories: Add more news categories.

## Tech used-  Html, CSS, JavaScript
