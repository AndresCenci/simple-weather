# Simple Weather

### TLDR
**weather-api** is the backend app with the services that query OpenWeatherMap.
**weather-app** is the frontend app that consumes the weather-api services.

**How to run the demo**
* *npm install* must be executed in each project, weather-api and weather-app.
* Configure the environment variable APPID_OPENWEATHERMAP with the appid obtained by registering at [openweathermap.org](https://openweathermap.org/), or add it to the weather-api project in the *config/index.js* file.
* Run *npm run dev* or *npm start* inside weather-api to run the server. It will run on port 8000, unless you have a PORT environment variable set on the OS.
* Execute *npm start* inside weather-app to run the app. It will run on port 3000, it will automatically open the browser during execution. If not, go to the browser and run *localhost:3000*.
* On the app screen are the instructions to consult for any other city than the one obtained by default by ipapi.


### Extended version
The project consists of two applications, a backend with api rest and a frontend that consumes its endpoints.

#### weather-api
It is a Node.js application that contains the following rest services that query openweathermap.org

**/location**

Returns the city location data according to ip-api.

**/current[/city]**

City is an optional parameter. Returns the city location data or the current location based on ip-api and the current weather status.

**/forecast[/city]**

City is an optional parameter. Returns the city location data or the current location based on ip-api and 5-day weather

**/find[/city][/country]**

City and Country are optional parameters. Returns the location data if city and country exist, and the 5-day weather. If only the city parameter is sent it will return values if there is not more than one city with that name. If it does not find them, nothing returns.

The following dependencies were used:
* [cors](https://www.npmjs.com/package/cors)
* [dotenv](https://www.npmjs.com/package/dotenv)
* [express](https://www.npmjs.com/package/express)
* [ipapi.co](https://www.npmjs.com/package/ipapi.co)
* [node-fetch](https://www.npmjs.com/package/node-fetch)

The following development dependencies were used:
* [eslint](https://www.npmjs.com/package/eslint)
* [eslint-config-prettier](https://www.npmjs.com/package/eslint-config-prettier)
* [eslint-plugin-mocha](https://www.npmjs.com/package/eslint-plugin-mocha)
* [eslint-plugin-prettier](https://www.npmjs.com/package/eslint-plugin-prettier)
* [husky](https://www.npmjs.com/package/husky)
* [lint-staged](https://www.npmjs.com/package/lint-staged)
* [mocha](https://www.npmjs.com/package/mocha)
* [nodemon](https://www.npmjs.com/package/nodemon)
* [prettier](https://www.npmjs.com/package/prettier)
* [supertest](https://www.npmjs.com/package/supertest)

**How to run weather-api**
* *npm install* must be executed inside weather-api.
* Configure the environment variable APPID_OPENWEATHERMAP with the appid obtained by registering at [openweathermap.org](https://openweathermap.org/), or add it to the weather-api project in the *config/index.js* file.
* Execute *npm run dev* or *npm start* inside weather-api to run the server. It will run on port 8000, unless you have a PORT environment variable set on the OS.
* To run the tests you must execute *npm test*.


#### weather-app
It is a React project generated with create-react-app and was performed only to view the results of the backend.
Only two poorly designed components were generated on a single screen to see results and test functionality. No tests were generated for this project either.

**How to run weather-app**
* *npm install* must be executed in each project, weather-api and weather-app.
* Configure the environment variable APPID_OPENWEATHERMAP with the appid obtained by registering at [openweathermap.org](https://openweathermap.org/), or add it to the weather-api project in the *config/index.js* file.
* Execute *npm run dev* or *npm start* inside weather-api to run the server. It will run on port 8000, unless you have a PORT environment variable set on the OS.
* Execute *npm start* inside weather-app to run the app. It will run on port 3000, it will automatically open the browser during execution. If not, go to the browser and run localhost: 3000.
* On the app screen are the instructions to consult for any other city than the one obtained by default by ipapi.


## Enjoy!
