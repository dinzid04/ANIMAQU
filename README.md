This prompt is designed to guide the development of a website similar to Animaqu, an anime streaming platform. Below are the key components and instructions for recreating the website, based on the provided codebase.

### **Project Overview**

Animaqu is a web application for streaming anime with Indonesian subtitles. It is built using Node.js and Express, with Pug as the templating engine. The application fetches data from an external API and includes features such as browsing ongoing and completed anime, searching by genre, and watching episodes.

### **Key Features**

- **Home Page**: Displays a slider with featured anime, along with lists of ongoing and recently completed series.
- **Anime Listings**: Separate pages for ongoing and completed anime, with support for pagination.
- **Search Functionality**: Allows users to search for anime by keywords and filter results.
- **Genre Pages**: Provides a list of all available genres and allows users to browse anime by a specific genre.
- **Movie Listings**: A dedicated section for anime movies, with details and streaming links.
- **Episode Streaming**: An integrated video player for watching episodes directly on the site.
- **Dark Mode**: A toggle for switching between light and dark themes.
- **Cookie Consent**: A banner to inform users about cookie usage and obtain their consent.

### **Technical Specifications**

- **Backend**:
  - **Framework**: Node.js with Express.
  - **Templating**: Pug.
  - **Dependencies**: `axios` for API requests, `cheerio` for web scraping, `sqlite3` for database management, and `express-session` for user sessions.
- **Frontend**:
  - **Styling**: Tailwind CSS for a modern, responsive design.
  - **Video Player**: Plyr for a customizable and accessible video player.
- **API Integration**:
  - The application relies on an external API to fetch anime data. The base URL is configurable and falls back to a default if not specified.
  - The API service includes methods for fetching home page data, ongoing and completed anime, genres, and search results.

### **File Structure**

Recreate the project with the following directory structure:

```
/
|-- config/
|   |-- session.js
|-- models/
|   |-- database.js
|-- public/
|   |-- images/
|   |-- css/
|   |-- js/
|-- routes/
|   |-- index.js
|   |-- anime.js
|   |-- admin.js
|   |-- api.js
|-- services/
|   |-- animeApi.js
|-- views/
|   |-- index.pug
|   |-- layout.pug
|   |-- ongoing.pug
|   |-- complete.pug
|   |-- genres.pug
|   |-- movie-list.pug
|-- app.js
|-- package.json
```

### **Implementation Details**

1. **Setup the Express Server**:
   - Create the main application file (`app.js`) to configure the Express server, middleware, and routes.
   - Implement routes for each feature, such as the home page, anime listings, search, and genres.
2. **Create the API Service**:
   - Develop a service (`services/animeApi.js`) to handle all interactions with the external anime API.
   - Include methods for fetching different types of data (e.g., ongoing, completed, search results).
3. **Design the Views**:
   - Use Pug to create reusable templates, including a main layout (`layout.pug`) and individual pages for each feature.
   - Style the application with Tailwind CSS, ensuring a responsive and user-friendly design.
4. **Implement Key Features**:
   - **Home Page**: Fetch and display a slider with random ongoing anime, along with lists of ongoing and completed series.
   - **Anime Listings**: Create pages for ongoing and completed anime, with pagination to handle large datasets.
   - **Search**: Add a search bar that allows users to find anime by title.
   - **Video Player**: Integrate the Plyr video player on the episode streaming page.
   - **Dark Mode**: Add a toggle switch that allows users to switch between light and dark themes.

### **Data Models**

- **Anime**:
  - `title` (String): The title of the anime.
  - `slug` (String): A URL-friendly version of the title.
  - `poster` (String): The URL of the poster image.
  - `synopsis` (String): A brief summary of the anime.
  - `genres` (Array of Strings): The genres associated with the anime.
- **Episode**:
  - `title` (String): The title of the episode.
  - `slug` (String): A URL-friendly version of the episode title.
  - `stream_url` (String): The URL of the video stream.

By following these instructions, you can recreate the Animaqu website with all its key features and functionalities.