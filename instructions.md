# Module 9
External APIs allow developers to access their data and functionality by making requests with specific parameters to a URL. Developers are often tasked with retrieving data from another application's API and using it in their context, frequently consuming this data via a server.
Your Challenge this week is to build a weather dashboard application that calls the OpenWeather API and renders data in the browser.

# Weather Dashboard
The application’s front end has already been created. It's your job to build the back end, connect the two, and then deploy the entire application to Render.
Use the 5-day weather forecast API
 to retrieve weather data for cities.
The base URL should look like the following:
https://api.openweathermap.org/data/2.5/forecast?lat={lat}&lon={lon}&appid={API key}


After registering for a new API key, you may need to wait up to 2 hours for that API key to activate.
For more information on how to work with the OpenWeather API, refer to the Full-Stack Blog on how to use API keys

# important
Make sure to download and unzip the starter code files and make your own repository with the starter code.
Before you start, download the starter code.

# User Story
AS A traveler
I WANT to see the weather outlook for multiple cities
SO THAT I can plan a trip accordingly

# Acceptance Criteria
GIVEN a weather dashboard with form inputs
WHEN I search for a city
THEN I am presented with current and future conditions for that city, and that city is added to the search history
WHEN I view current weather conditions for that city
THEN I am presented with the city name, the date, an icon representation of weather conditions, a description of the weather for the icon's `alt` tag, the temperature, the humidity, and the wind speed
WHEN I view future weather conditions for that city
THEN I am presented with a 5-day forecast that displays the date, an icon representation of weather conditions, the temperature, the wind speed, and the humidity
WHEN I click on a city in the search history
THEN I am again presented with current and future conditions for that city


# Getting Started
On the back end, the application should include a searchHistory.json file that will be used to store and retrieve cities using the fs module.
The following HTML route should be created:
GET * should return the index.html file.
The following API routes should be created:
GET /api/weather/history should read the searchHistory.json file and return all saved cities as JSON.
POST /api/weather should receive a city name to save on the request body, add it to the searchHistory.json file, and then return associated weather data to the client. You'll need to find a way to give each city name a unique id when it's saved (look into npm packages that could do this for you).
Refer to the Full-Stack Blog on deploying to Render and the Render documentation on setting environment variables.

# Hints
Using the 5-day weather forecast API, you'll notice that you'll need to pass in coordinates instead of just a city name. Using the OpenWeatherMap APIs, how could we retrieve geographical coordinates given a city name?
How could we make the OpenWeather API calls server-side, parse the data, and then send the parsed data client-side?

# Bonus
This application offers the DELETE functionality on the front end. As a bonus, try to add the DELETE route to the application using the following guideline:
DELETE /api/weather/history/:id should receive a route parameter that contains the id of a city name to delete. To delete a city, you'll need to read all the cities from the searchHistory.json file, remove the city with the given id property, and then rewrite the cities to the searchHistory.json file.

# Grading Requirements

# note
If a Challenge assignment submission is marked as “0”, it is considered incomplete and will not count towards your graduation requirements. Examples of incomplete submissions include the following:
A repository that has no code
A repository that includes a unique name but nothing else
A repository that includes only a README file but nothing else
A repository that only includes starter code
This Challenge is graded based on the following criteria:

# Technical Acceptance Criteria: 40%
Satisfies all of the preceding acceptance criteria plus the following:
Application uses the OpenWeather API to retrieve weather data.
Application back end must store cities that have a unique id in a JSON file.
Application must be deployed to Render.

# Deployment: 32%
Application deployed at live URL.
Application loads with no errors.
Application GitHub URL submitted.
GitHub repository that contains application code.

# Application Quality: 15%
Application user experience is intuitive and easy to navigate.
Application user interface style is clean and polished.
Application resembles the mock-up functionality provided in the Challenge instructions.

# Repository Quality: 13%
Repository has a unique name.
Repository follows best practices for file structure and naming conventions.
Repository follows best practices for class/id naming conventions, indentation, quality comments, etc.
Repository contains multiple descriptive commit messages.
Repository contains a quality README file with description, screenshot, and link to deployed application.

# Bonus
Fulfilling the following can add 10 points to your grade. Note that the highest grade you can achieve is still 100:
Application allows users to delete cities.

# How to Submit the Challenge
You are required to submit BOTH of the following for review:
The URL of the functional, deployed application.
The URL of the GitHub repository. Give the repository a unique name and include a README describing the project.

# note
You are allowed to miss up to two Challenge assignments and still earn your certificate. If you complete all Challenge assignments, your lowest two grades will be dropped. If you wish to skip this assignment, click Next, and move on to the next Module.
Comments are disabled for graded submissions in BootCamp Spot. If you have questions about your feedback, please notify your instructional staff or the Student Success Advisor. If you would like to resubmit your work for an improved grade, you can use the Resubmit Assignment button to upload new links. You may resubmit up to three times for a total of four submissions.

# important
It is your responsibility to include a note in the README section of your repo specifying code source and its location within your repo. This applies if you have worked with a peer on an assignment, used code in which you did not author or create sourced from a forum such as Stack Overflow, or you received code outside curriculum content from support staff such as an Instructor, TA, Tutor, or Learning Assistant. This will provide visibility to grading staff of your circumstance in order to avoid flagging your work as plagiarized.
If you are struggling with a Challenge or any aspect of the curriculum, please remember that there are student support services available for you:
Xpert LA Chat+ - chat with a Live Agent in the "Xpert Learning Assistant Chat+" section of Bootcampspot - Canvas.
Office hours facilitated by your instructional staff before and after each class session.
Tutoring Guidelines—schedule a session in the "Tutor Sessions" section of Bootcampspot - Canvas.
If the above resources are not applicable and you have a need, please reach out to a member of your instructional team, your Student Success Advisor, or submit a support ticket in the Student Support section of your BCS application.

