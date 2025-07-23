# Clima - iOS Weather Application

## Project Overview

Clima is a sleek, user-friendly weather application for iOS that provides real-time weather data. Users can get the current weather for their location or search for the weather in any city around the world. This project was developed to demonstrate core iOS development skills, including working with APIs, handling user input, and creating a clean, modern user interface.

This project was built as part of a learning module from Cofoundery, which provided the initial concept and guidance. The final implementation, coding, and problem-solving were performed independently.

## Key Features

* **Live Weather Data:** Fetches current weather information from the [OpenWeatherMap API](https://openweathermap.org/api).
* **City Search:** Allows users to search for the weather in any city globally.
* **GPS Location:** Automatically gets the weather for the user's current location using CoreLocation.
* **Dynamic UI:** The user interface updates dynamically with a weather icon and temperature based on the fetched data.
* **Delegate-Based Networking:** Implements a clean, reusable networking layer using the delegate design pattern to handle API responses.

## Technical Skills Demonstrated

* **Languages & Frameworks:** Swift, UIKit, CoreLocation
* **Architecture:** Model-View-Controller (MVC)
* **Networking:** URLSession for making REST API calls, JSON parsing with `JSONDecoder`.
* **Concurrency:** Asynchronous network requests and completion handlers.
* **UI/UX:** Storyboard-based UI design with Auto Layout, handling user input with `UITextField`.
* **Design Patterns:** Delegate Pattern for robust communication between the `WeatherManager` and `WeatherViewController`.

## How It Works

1.  **User Input:** The user can either tap the location button or type a city name into the search field.
2.  **API Request:**
    * For GPS, `CoreLocation` fetches the device's coordinates.
    * The `WeatherManager` class constructs the appropriate URL for the OpenWeatherMap API with either the city name or coordinates.
3.  **Data Fetching:** `URLSession` creates a data task to perform an asynchronous GET request to the API.
4.  **Data Parsing:** Upon receiving a successful response, the JSON data is parsed into a `WeatherData` model using `JSONDecoder`.
5.  **UI Update:** The `WeatherManager` communicates the fetched weather data back to the `WeatherViewController` via a delegate method. The view controller then updates the UI elements (temperature label, city label, and condition image) on the main thread.

## How to Run This Project

1.  Clone the repository to your local machine.
2.  Open the `Clima.xcodeproj` file in Xcode.
3.  **Important:** To run the app, you must obtain a free API key from [OpenWeatherMap](https://openweathermap.org/appid).
4.  In the `WeatherManager.swift` file, replace the placeholder for the API key with your own key.
5.  Build and run the project on an iOS simulator or a physical device.
