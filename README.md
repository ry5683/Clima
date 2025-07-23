# 🌦️ Clima - iOS Weather Application

## 📝 Project Overview

Clima is a sleek, user-friendly weather application for iOS that provides real-time weather data. I developed this project to solidify and demonstrate my proficiency in core iOS development skills, including API integration, asynchronous programming, and building clean, responsive user interfaces with UIKit.

This project was built upon a concept from a Cofoundery learning module. I independently wrote all the code, implemented the final architecture, and handled all problem-solving to bring the concept to life.

## ✨ Key Features

* **🛰️ Live Weather Data:** Fetches current weather information from the OpenWeatherMap API.
* **🏙️ City Search:** Allows users to search for the weather in any city globally.
* **📍 GPS Location:** Automatically gets the weather for the user's current location using CoreLocation.
* **🎨 Dynamic UI:** The user interface updates dynamically with a weather icon and temperature based on the fetched data.
* **🤝 Delegate-Based Networking:** Implements a clean, reusable networking layer using the delegate design pattern for robust API communication.

## 🛠️ Core Technologies & Concepts

* **UI & Frameworks:** UIKit, CoreLocation, Auto Layout, Storyboards
* **Language:** Swift
* **Architecture & Design Patterns:** Model-View-Controller (MVC), Delegate Pattern
* **Networking & Data:** URLSession for REST API calls, JSON parsing with `JSONDecoder`, Asynchronous Programming

## ⚙️ How It Works

1.  **User Input:** The user can either tap the location button or type a city name into the search field.
2.  **API Request:** `WeatherManager` constructs the appropriate URL for the OpenWeatherMap API with either the city name or coordinates.
3.  **Data Fetching:** `URLSession` creates a data task to perform an asynchronous GET request to the API.
4.  **Data Parsing:** Upon receiving a successful response, the JSON data is parsed into a `WeatherData` model.
5.  **UI Update:** The `WeatherManager` communicates the fetched data back to the `WeatherViewController` via a delegate method, which then updates the UI on the main thread.

## 🚀 How to Run This Project

1.  Clone the repository to your local machine.
2.  Open the `Clima.xcodeproj` file in Xcode.
3.  **Important:** To run the app, you must obtain a free API key from [OpenWeatherMap](https://openweathermap.org/appid).
4.  In `WeatherManager.swift`, find the `let weatherURL` constant and replace the API key placeholder with your actual key.
5.  Build and run the project on an iOS simulator or a physical device.

