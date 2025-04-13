# WeatherSphere
Weather App
A React-based weather application that fetches current weather and 5-day forecast data using the OpenWeatherMap API. Users can search by city name, zip code, or GPS coordinates (latitude,longitude). The app includes a geolocation feature to fetch weather for the user's current location.

# Features
## Search weather by:
City name (e.g., London, London,UK)
Zip code (e.g., 10001)
GPS coordinates (e.g., 40.7128,-74.0060)
Fetch current weather and 5-day forecast
Display daily forecast summaries (noon entries for each day)
Use browser geolocation to get weather for the user's current location
Responsive UI with error handling for invalid inputs or API failures
Backend proxy to securely handle OpenWeatherMap API requests
# Tech Stack
Frontend: React, Axios
Backend: Node.js, Express, Axios
API: OpenWeatherMap
Environment: Managed via .env for API keys and configuration
Prerequisites
Node.js (v14 or higher)
npm (v6 or higher)
OpenWeatherMap API key (sign up at OpenWeatherMap to get one)
# Setup
1. Clone the Repository
git clone https://github.com/your-username/weather-app.git
cd weather-app
2. Backend Setup
Navigate to the backend directory (if separate, e.g., ./backend):
cd backend

Install dependencies:
npm install

Create a .env file in the backend directory with the following:
OPENWEATHER_API_KEY=your_openweathermap_api_key
PORT=5000
Replace your_openweathermap_api_key with your actual OpenWeatherMap API key.
Start the backend server:
npm start
The backend will run on http://localhost:5000.

3. Frontend Setup
Navigate to the frontend directory (if separate, e.g., ./frontend):
cd frontend
Install dependencies:
npm install

Start the frontend development server:
npm start
The frontend will run on http://localhost:3000.

4. CORS Configuration
Ensure the backend allows CORS requests from the frontend. The backend includes CORS middleware (cors) to permit requests from http://localhost:3000.

Usage
Open the app in your browser at http://localhost:3000.
Enter a search query in the input field:
City: e.g., London, New York,US
Zip Code: e.g., 10001
Coordinates: e.g., 40.7128,-74.0060 (latitude,longitude)
Click Get Weather to fetch weather data.
Alternatively, click Use Current Location to fetch weather for your current location (requires browser geolocation permission).
View the current weather and 5-day forecast displayed on the page.
Coordinate Input Format
Enter latitude and longitude as latitude,longitude with no spaces. Examples:

New York City: 40.7128,-74.0060
London, UK: 51.5074,-0.1278
Sydney, Australia: -33.8688,151.2093
Rio de Janeiro, Brazil: -22.9068,-43.1729
Tokyo, Japan: 35.6762,139.6503
Notes:

Latitude: -90 to +90 (negative for south)
Longitude: -180 to +180 (negative for west)
Include at least one decimal place (e.g., 40.7,-74.0)

API Endpoints
The backend exposes two endpoints:

GET /api/weather/current: Fetches current weather data
Query params: lat, lon (for coordinates) or q (for city/zip)
GET /api/weather/forecast: Fetches 5-day forecast data
Query params: lat, lon (for coordinates) or q (for city/zip)
The backend forwards requests to OpenWeatherMap and returns the response to the frontend.

Error Handling
Invalid coordinates: "Invalid input format"
Location not found: "Location not found"
Geolocation denied: "Geolocation permission denied"
General API failure: "Failed to fetch weather data. Please try again."
Future Improvements
Add unit toggle (Celsius/Fahrenheit)
Enhance forecast display with more details (e.g., hourly data)
Implement caching for frequent queries
Add loading indicators during API requests
Support more input formats (e.g., city with state)

# Code
![Screenshot (77)](https://github.com/user-attachments/assets/178a96f3-438a-42df-9981-b0b32fe8e554)


# Frontend
![Screenshot (72)](https://github.com/user-attachments/assets/6dc72dd9-e8e0-4625-a0be-af4b1ffddc5f)



![Screenshot (73)](https://github.com/user-attachments/assets/a171df1a-948a-4b65-b9d2-4f7004c33419)


![Screenshot (74)](https://github.com/user-attachments/assets/7136467c-8f4e-499d-a074-ff00f861afd1)



# Backend
![Screenshot (76)](https://github.com/user-attachments/assets/90decb03-d88d-464b-8965-44e3145939b5)


# API
![Screenshot (75)](https://github.com/user-attachments/assets/37a79836-efe7-4cba-81d5-3051520bacd9)



# Demo Video
- Due to some reasons, voice is not recorded. But functionality is clearly explained. Kindly watch full video.
[Demo](https://drive.google.com/file/d/1ZI9rmcSKMWkmEbSBgbLS7bUFsUxHwFbX/view?usp=sharing)
