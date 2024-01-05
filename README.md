### Meet App - 

### Link: https://tcederberg.github.io/meet_app/

## Introduction

**Meet App** is a serverless Progressive Web Application (PWA) built with React. Utilizing a Test-Driven Development (TDD) approach, this app seamlessly integrates with the Google Calendar API to fetch and display upcoming events.

## Objective
Build a serverless, progressive web application (PWA) with React using a test-driven development (TDD) technique. The application integrates with the Google Calendar API to fetch upcoming events.


## Key Features
- Filter Events by City
- Show/Hide Event Details
- Specify Number of Events
- Offline Usage Capability
- Add App Shortcut to Home Screen
- Display Charts Visualizing Event Data


## Use of Serverless Function in the Meet App

- The Meet App can use serverless functions for event notifications, real-time data processing, user authentication, event recommendations, , and scalability. By leveraging serverless technology, the app can efficiently handle backend processes, provide personalized experiences, and scale according to user demand.


## user stories and features

FEATURE 1: FILTER EVENTS BY CITY

As a user, I should be able to filter events by city. So that I can see a list of events taking place in that city.

- **Scenario 1:** User opens the app and has searched a city.
- **Given** the main page with search option has been opened, 
    **when** the user entered a city, 
    **then** they should be shown upcoming events for that city.


- **Scenario 2:** User opens the app and hasn't searched a city.
- **Given** the main page with search option has been opened, 
    **when** the user opens the app, 
    **then** they should be shown a list of all events for all the cities available.


- **Scenario 3:** User can select a city from the suggested list.
- **Given** user was typing "Berlin" in the city textbox _AND_ the list of suggested cities is showing, 
    **when** the user selects a city (e.g., "Berlin, Germany") from the list, **then** their city should be changed to that city (i.e., "Berlin, Germany") _AND_ the user should receive a list of upcoming events in that city.

FEATURE 2: SHOW/HIDE AN EVENT'S DETAILS

As a user I should be able to show or hide event details, after I have selected a city I wanted to look up the events for.

- **Scenario 1:** An event element is collapsed by default
  - **Given** user has searched for events regardless to the chosen city or not,      **when** the user recieves the full list of events (specific for the city or all events), 
  **then** all events will colapse by default.

- **Scenario 2:** User can expand an event to see its details
  - **Given** the user gets a list of events, 
    **when** a user selects an event's details, 
    **then** the details will show up for that choosen event.

- **Scenario 3:** User can collapse an event to hide its details
  - **Given** the user sees the details of an event, 
    **when** the user presses a button to hide event's details, 
    **then** the details of that even will be hidden.

FEATURE 3: SPECIFY NUMBER OF EVENTS

As a user, I should be able to specify the number of displayed events, after I have selected the number of displayed events.

- **Scenario 1:** When user hasn't specified a number, 32 is the default number.
  - **Given** the user hasn't specified or filtered the number of events, 
    **when** the user sees the list of events 
    **then** the default number of displayed events will be 32.

- **Scenario 2:** User can change the number of events they want to see.
  - **Given** the user has events displayed, 
    **when** the user chooses to change the number of events displayed, 
    **then** the number of events displayed will update to the number the user selected.

FEATURE 4: USE THE APP WHEN OFFLINE

As a user, I should be able to get events information when offline, that was fetched while having internet connection.

- **Scenario 1:** Show cached data when there's no internet connection.
  - **Given** the user has no internet connection, 
    **when** the user is accessing the app, 
    **then** cached data, stored inside the app, will be provided to the user.

- **Scenario 2:** Show error when user changes the settings (city, time range).
  - **Given** the user has no internet connection, 
    **when** the user is trying to access new event information (change the city, etc.), 
    **then** the app will show an error.

FEATURE 5: ADD AN APP SHORTCUT TO THE HOME SCREEN

As a user I should be able to add a shortcut of the app to the home screen, so I can access the app quicker.

- **Scenario 1:** User can install the meet app as a shortcut on their device home screen.
  - **Given** the user wants to install the app, 
    **when** the user selects to install the app as a shortcut, 
    **then** a shortcut is created on users homescreen.

FEATURE 6: DISPLAY CHARTS VISUALIZING EVENT DETAILS

As a user, I would like to be able to see a chart showing the upcoming events in each city so that I know what events are organized in which city.

- **Scenario 1:** Show a chart with the number of upcoming events in each city.
  - **Given** the user is in the events detail page, 
    **when** the user clicks the button to see a chart of those events in all the cities as a comparison, 
    **then** a chart with the number of upcoming events for every city, will be shown to the user.


## Technical Stack

- **Frontend**: Developed using React, incorporating Progressive Web App (PWA) technologies for a responsive and offline-capable user experience.
- **Backend**: Serverless architecture leveraging AWS Lambda for scalable, maintenance-free backend solutions. Serverless functions are utilized to handle dynamic backend processes such as authentication, data processing, and integration with the Google Calendar API. This approach allows for efficient scaling, cost-effective operations (as costs are based on actual usage), and eliminates the need for dedicated server management, making the app more reliable and easier to maintain.
- **API Integration**: Utilizing the Google Calendar API with OAuth2 authentication for secure and reliable data fetching.
- **Testing**: Adhering to Test-Driven Development (TDD) principles with a target of at least 90% test coverage to ensure code reliability and quality.
- **Deployment**: The app is hosted on GitHub Pages and is designed to be compatible across major browsers, ensuring a seamless user experience on various devices.

## Project Requirements

- **React Application**: The app is built using React, following best practices and modern development standards.
- **Serverless Functions**: Implementation of serverless functions, preferably AWS Lambda, for handling backend processes, including authorization.
- **Deployment Strategy**: Deployment on GitHub Pages, emphasizing accessibility and performance across different browsers and devices.
- **PWA Compliance**: Adhering to Lighthouse's PWA checklist to guarantee a high-quality Progressive Web App experience.
- **Offline Functionality**: Ensuring robust offline functionality using service workers for a seamless user experience even without internet connectivity.
- **Data Visualization**: Integration of data visualization tools for effective representation of event data.
- **Testing and Performance**:

  - **Comprehensive Testing**: Embracing a thorough Test-Driven Development (TDD) approach, the application undergoes extensive testing. This includes:
    - **Unit Testing**: Ensuring individual components function correctly.
    - **Integration Testing**: Validating the interaction between various components.
    - **End-to-End Testing**: Testing the entire application workflow as experienced by the end user.
  - **Performance Optimization**: Performance assessments are conducted through tools such as Google Lighthouse to ensure optimal application speed and efficiency. Key focus areas include: - **Load Time**: Minimizing the time it takes for the app to become fully operational. - **Responsiveness**: Ensuring the app responds swiftly to user interactions regardless of the device or browser. - **Resource Efficiency**: Optimizing the use of resources to ensure a smooth, lag-free experience, especially in offline mode.