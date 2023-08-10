# Tom's Weather Forecast App

This React application fetches weather data based on a user's input of a zip code and displays the current weather forecast. It utilizes the OpenWeatherMap API to retrieve weather information and presents it to the user in a user-friendly interface.

## Installation

1. Clone the repository or download the code.
2. Open your terminal and navigate to the project directory.
3. Run `npm install` to install the required dependencies.
4. Run `npm start` to start the development server.
5. Open your web browser and navigate to `http://localhost:3000` to use the app.

## Screenshot
<img width="794" alt="Screenshot 2023-08-10 at 12 32 00" src="https://github.com/tomtenniscourt/weather-forecast/assets/127535435/7838a242-9fdf-4480-bd75-6f2c347ad173">

### `Weather`

The core component of the application, responsible for managing the weather forecast retrieval and rendering.

- **State Initialization**: The component's initial state includes various properties related to weather data, such as `zipcode`, `temperature`, `high`, `low`, `description`, `city`, `error`, and `weather`.

- **handleChange**: This method is invoked when the user enters a zip code into the input field. It updates the `zipcode` property in the state based on the user's input.

- **handleSubmit**: When the user submits the form (clicks the "Get my forecast!" button), this method is called. It constructs a URL to fetch weather data from the OpenWeatherMap API using the provided zip code.

- **Fetch Weather Data**: The `fetch` API is used to retrieve weather data from the OpenWeatherMap API. The constructed URL includes the zip code and necessary parameters such as `units` for temperature units (imperial in this case) and an `appid` for API authentication.

- **Handle API Response**: The fetched JSON response is parsed. If the response indicates an error (status code `404`), an error message is displayed. Otherwise, the weather data is set in the state properties.

- **Rendering Weather Information**: The component conditionally renders weather information. If weather data is available, it displays the current temperature, high and low temperatures, and a description of the weather condition.

- **Displaying Icons**: The weather condition icon is fetched using the provided `iconCode` from the API response. An icon URL is constructed, and the icon is displayed using an `<img>` element.

### API Integration

The application integrates with the OpenWeatherMap API to retrieve weather data for a specified zip code.

- **API Key**: The API key is included in the `apiKey` variable. It is used for authentication when making requests to the API.

- **API Endpoint**: The base URL for the OpenWeatherMap API is stored in the `baseUrl` variable. The API endpoint for current weather data is constructed by appending the zip code and additional parameters such as `units`.

- **Fetching Data**: The `fetch` API is used to send a GET request to the constructed API endpoint. The response is received in JSON format.

- **Parsing Data**: The fetched JSON response is parsed to extract relevant weather information, such as temperature, high and low temperatures, and weather description.


## Contributing

Contributions are welcome! If you encounter any issues or have suggestions for improvement, please open an issue or submit a pull request.


