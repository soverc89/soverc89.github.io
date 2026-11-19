[Back to Portfolio](./)

Contact Andrew Taylor for implementation details.

Senior Project: Hunting Stand Weather Manager
===================

-   **Class:** Senior Project
-   **Grade:** TBD
-   **Language(s):** Python, HTML, CSS, JavaScript, SQL
-   **Source Code Repository:** [soverc89/CSU-Senior-Project-aTaylor](https://github.com/soverc89/CSU-Senior-Project-aTaylor)

## Project description
The Hunting Stand Weather Manager is a web application that helps hunters organize properties and stand locations, compare current wind conditions, and identify favorable stands. It combines an interactive map with a ranked dashboard displaying favorability percentages, colors, and compass indicators.

### Statement of Purpose
Choosing a hunting stand requires comparing wind direction with the stand's orientation to understand where the hunter's scent will travel. This project simplifies that process by retrieving local wind observations and presenting stand rankings in an accessible desktop and mobile interface.

### Project Language(s), Software, and Hardware
The application uses Python with Flask, Flask-SQLAlchemy, Flask-Login, and Requests. SQLite stores user, property, and stand records. HTML, CSS, JavaScript, Pure.css, and Leaflet provide the interface and satellite/street maps. Development uses a standard laptop, and the application is accessed through a desktop or mobile web browser.

### Project Requirements
The acceptance criteria included that:

1. Users can create, edit, and delete properties and stands, including stand coordinates and facing directions.
2. Users can manage stands through an interactive map and use device geolocation to populate coordinates.
3. The system retrieves National Weather Service wind data and ranks stands using color-coded favorability percentages.
4. User accounts require authentication, hashed passwords, and access restrictions protecting each user's data.
5. The application stores records in a relational database and caches weather data to reduce repeated API calls.

### Project Implementation Description & Explanation
The application follows Flask's application factory pattern, with separate modules for routing, database models, weather retrieval, and map data. Each user owns properties containing stands. Weather observations are fetched for the property's coordinates, converted from wind-source direction to wind-travel direction, and cached for one hour. The grader compares that direction with each stand's facing to produce a 0–100% favorability score.

Users can place and move stand pins, select their current location, and aim a stand with a draggable compass control. A temporary wind override previews different rankings without changing cached weather. Automated tests cover grading, database relationships, mocked weather responses, input validation, and security controls.

[Back to Portfolio](./)
