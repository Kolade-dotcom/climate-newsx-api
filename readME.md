# Climate News API

## Overview

The Climate News API is a Node.js-based application that fetches climate-related news articles from various sources and provides endpoints to access the data. It utilizes the `express`, `axios`, and `cheerio` libraries to retrieve and parse news articles from different news websites.

## API Endpoints

### Welcome Message

- **Endpoint**: `/`
- **HTTP Method**: GET
- **Response**: Displays a welcome message.
- **Example Response**:
  ```
  Welcome to My Climate News API
  ```

### Get All Climate News Articles

- **Endpoint**: `/newsX`
- **HTTP Method**: GET
- **Response**: Returns an array of climate-related news articles from various news sources.
- **Example Response**:
  ```
  [
    {
      "title": "Climate Crisis: London Must Become a World Leader on Climate Change Action",
      "url": "https://www.cityam.com/london-must-become-a-world-leader-on-climate-change-action/climate-crisis",
      "source": "cityam"
    },
    {
      "title": "Climate Change and Its Impact on the Environment",
      "url": "https://www.washingtonpost.com/climate-environment/climate-change-and-its-impact-on-the-environment/",
      "source": "washingtonpost"
    },
    // More articles...
  ]
  ```

### Get Climate News Articles from a Specific Source

- **Endpoint**: `/newsX/:newspaperId`
- **HTTP Method**: GET
- **Parameters**:
    - `newspaperId`: The identifier of the news source (e.g., `washingtonpost`, `cbc`, `nyt`, etc.).
- **Response**: Returns an array of climate-related news articles from the specified news source.
- **Example Response**:
  ```
  [
    {
      "title": "Climate Change and Its Impact on the Environment",
      "url": "https://www.washingtonpost.com/climate-environment/climate-change-and-its-impact-on-the-environment/",
      "source": "washingtonpost"
    },
    {
      "title": "Climate Change News: Latest Updates and Developments",
      "url": "https://www.cbc.ca/news/climate/climate-change-news-latest-updates-and-developments/",
      "source": "cbc"
    },
    // More articles...
  ]
  ```

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/Kolade-dotcom/climate-newsx-api.git
   cd climate-newsx-api
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Run the server:

   ```bash
   npm start
   ```

4. The server will start running on `http://localhost:8000`. You can access the API endpoints as described above.

## Notes

- This application fetches news articles from various websites, so the availability and content of the articles are subject to change based on the websites' data.
- The API endpoints use the HTTP methods (`GET`) as indicated above.

**Disclaimer**: This application is for educational purposes only and does not endorse or guarantee the accuracy of the information provided by external sources. The content and availability of the articles depend on the respective news websites.