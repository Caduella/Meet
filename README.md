# Meet App
This is a serverless, progressive web application with React using a test-driven development technique.  The application uses the Google Calendar API to fetch upcoming events.

# Key Features
- Filter Events by City
- Show/Hide Event Details
- Specific Number of Events
- Use the App When Offline
- Add an App Shortcut to the Home Screen
- Display Charts Visualizing Event Details

# Technical Requirements
- The app is a React application.
- The app is built using the TDD technique.
- The app uses the Google Calendar API and OAuth2 authentication flow.
- The app uses serverless functions (AWS lambda) for the authorization server instead of using a traditional server.
- The app's code is hosted in a Git repository on GitHub.
- The app works on the latest versions of Chrome, Firefox, Safari, Edge, and Opera, as well as on IE11.
- The app displays well on all screen sizes (including mobile and tablet) widths of 1920px and 320px.
- The app passes Lighthouse's PWA checklist.
- The app works offline or in slow network conditions with the help of a service worker.
- Users may be able to install the app on desktop and add the app to their home screen on mobile.
- The app is deployed on GitHub Pages.
- The app implements an alert system using an OOP approach to show information to the user.
- The app makes use of data visualization.
- The app is covered by tests with a coverage rate >= 90%
- The app is monitored using an online performance monitoring tool.

# Project Features & Scenarios

Feature 1: Filter Events By City

- Scenario 1: When the user hasn’t searched for a city, show upcoming events from all cities
 As a user, I should be able to view upcoming events from all cities when I haven’t searched for a specific city, so that I can explore a wide range of events before deciding to narrow my search.

- Scenario 2: User should see a list of suggestions when they search for a city
As a user, I should see a list of city suggestions as I type in the city search box, so that I can quickly find and select the city I am interested in without typing the full name.

- Scenario 3: User can select a city from the suggested list
As a user, I should be able to select a city from the list of suggestions, so that I can conveniently filter events to only show those occurring in my selected city.

Feature 2: Show/Hide Event Details

- Scenario 1: An event element is collapsed by default
As a user, I should be able to see event elements collapsed by default, so that the interface remains uncluttered and easy to navigate.

- Scenario 2: User can expand an event to see details
As a user, I should be able to expand an event to see its details, so that I can learn more about the event I'm interested in.

- Scenario 3: User can collapse an event to hidee details
As a user, I should be able to collapse an expanded event to hide its details, so that I can minimize information overload and focus on other events.

Feature 3: Specify Number of Events

- Scenario 1: When user hasn't specified a number, 32 events are shown by default
As a user, I should see 32 events displayed by default when I haven't specified a number, so that I have a reasonable number of events to start exploring without feeling overwhelmed.

- Scenario 2: User can change the number of events displayed
As a user, I should be able to change the number of events displayed, so that I can view more or fewer events based on my preferences.

Feature 4: Use the App When Offline

- Scenario 1: Show cashed data when there is no internet connection.
As a user, I should be able to view cached data when there's no internet connection, so that I can still access event information offline.

- Scenario 2: Show error when user changes search setting (city, number of events).
As a user, I should be shown an error when I try to change search settings (like city or number of events) while offline, so that I understand why my search preferences cannot be updated without an internet connection.

Feature 5: Add an App Shortcut to the Home Screen

- Scenario 1: User can install the meet app as a shortcut on their device home screen.
As a user, I should be able to install the meet app as a shortcut on my device's home screen, so that I can quickly and easily access the app without navigating through my device's browser.

Feature 6: Display Charts Visualizing Event Details

- Scenario 1: Show a chart with the number of upcoming events in each city.
As a user, I should be able to see a chart showing the number of upcoming events in each city, so that I can visualize and understand the distribution of events geographically.

# Gherkin syntax
Feature 1: Filter Events By City

- Scenario: When user hasn’t searched for a city, show upcoming events from all cities

  Given The user is on the events app

  When The user hasn’t searched for any city

  Then Upcoming events from all cities show be shown

- Scenario: User should see a list of suggestions when they search for a city

  Given The user is on the events app

  When The user starts typing in the city search box

  Then A list of city suggestions based on the user's input should be displayed

- Scenario: User can select a city from the suggested list

  Given The user is on the events app and a list of city suggestions is displayed

  When The user selects a city from the suggestions

  Then Events from the selected city should be displayed

Feature 2: Show/Hide Event Details

- Scenario: An event element is collapsed by default

  Given The user is viewing the list of events

  When The events are initially displayed

  Then All events should be collapsed by default

- Scenario: User can expand an event to see details

  Given The user is viewing the list of events

  When The user clicks on an event

  Then The event to show its details should be expanded

- Scenario: User can collapse an event to hide details

  Given The user has expanded an event to see its details

  When The user clicks on the event again

  Then The event to hide its details should be collapsed

Feature 3: Specify Number of Events

- Scenario: When user hasn’t specified a number, 32 events are shown by default

  Given The user is on the events app

  When The user doesn't specify a number of events

  Then 32 events should be displayed by default

- Scenario: User can change the number of events displayed

  Given The user is on the events app

  When The user specifies a number of events to display

  Then The specified number of events should be shown

Feature 4: Use the App When Offline

- Scenario: Show cached data when there's no internet connection

  Given The user is using the events app

  When There is no internet connection

  Then The previously cached event data should be displayed

- Scenario: Show error when user changes search settings (city, number of events) while offline

  Given The user is using the events app offline

  When The user attempts to change search settings like city or number of events

  Then An error message indicating the inability to update search settings offline should be displayed

Feature 5: Add an App Shortcut to the Home Screen

- Scenario: User can install the meet app as a shortcut on their device home screen

  Given The user is on the events app

  When The user chooses to add the app to their home screen

  Then The meet app as a shortcut on the user's device home screen should be installed

Feature 6: Display Charts Visualizing Event Details

- Scenario: Show a chart with the number of upcoming events in each city

  Given The user is on the events app

  When The user views the chart of events

  Then A chart showing the number of upcoming events in each city should be displayed

# Serverless Function
- In the Meet App, serverless functions are utilized for handling various backend tasks such as user authentication, data processing, and interacting with Google Calendar API. Specifically, the Meet App can manage the OAuth2 authentication flow, which allows the app to access Google Calendar events without the need for a backend server to handle the authentication tokens. Serverless functions can be triggered on-demand to execute these operations, ensuring that the Meet App remains responsive and efficient. By employing serverless architecture, the app can benefit from reduced operational costs, as the infrastructure scales automatically with the number of requests, and attention can be focused-  more on the user-facing features rather than server maintenance.
