# Weather App

A lightweight, responsive weather application built with vanilla JavaScript that displays current weather conditions for any city worldwide.

## Features

- **Simple Search**: Enter any city name to get instant weather data
- **Comprehensive Weather Data**: View temperature, conditions, humidity, and wind speed
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Real-time Updates**: Fetches the latest weather information from OpenWeatherMap API
- **User-friendly Interface**: Clean design with smooth animations and visual feedback
- **Error Handling**: Clear error messages for invalid searches or connection issues

## Live Demo

[View the live demo](https://your-github-username.github.io/weather-app/) (Update with your actual link after deployment)

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- An API key from OpenWeatherMap (free tier available)

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/your-username/weather-app.git
   ```

2. Navigate to the project directory:
   ```
   cd weather-app
   ```

3. Open `index.html` in your text editor and replace `YOUR_API_KEY` with your OpenWeatherMap API key:
   ```javascript
   const apiKey = "YOUR_API_KEY"; // Replace with your actual API key
   ```

4. Open `index.html` in your browser to use the application.

### Getting an API Key

1. Register for a free account at [OpenWeatherMap](https://openweathermap.org/api)
2. After logging in, go to your API keys tab
3. Copy your default key or generate a new one
4. Note that new API keys may take a few hours to activate

## How It Works

The application uses a single HTML file that contains all necessary HTML, CSS, and JavaScript:

1. The user enters a city name and clicks "Search" or presses Enter
2. The app sends a request to the OpenWeatherMap API with the city name
3. While waiting for a response, a loading indicator is displayed
4. When data is received, the app parses the JSON response and updates the UI
5. If an error occurs (e.g., city not found), a helpful error message is shown

## Code Structure

- **HTML**: Defines the structure and content of the application
- **CSS**: Handles styling, animations, and responsive design
- **JavaScript**: Manages user interactions, API calls, and DOM updates

## Customization

### Changing Units

The app uses metric units by default (Celsius, meters per second). To switch to imperial units (Fahrenheit, miles per hour), change the `units` parameter in the API URL:

```javascript
const url = `${apiUrl}?q=${city}&units=imperial&appid=${apiKey}`;
```

Don't forget to update the display units in the HTML as well:

```javascript
tempElement.textContent = `${Math.round(temp)}°F`;
windElement.textContent = `${speed} mph`;
```

### Styling

The application uses a purple gradient background by default. To change this, modify the background property in the CSS:

```css
body {
    background: linear-gradient(135deg, #your-color-1 0%, #your-color-2 100%);
}
```

## Browser Support

The app works with all modern browsers that support ES6 JavaScript, Fetch API, and CSS3.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [OpenWeatherMap](https://openweathermap.org/) for providing the weather data API
- Inspiration from various weather apps and tutorials across the web
