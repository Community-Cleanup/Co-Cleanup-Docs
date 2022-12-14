<img src="./doc/../docs/logo/logo-icon.svg" alt="User Story Tasks Delegation" width="300"/>

### Chris Hullman & Mick Caffery <!-- omit in toc -->
### MERN full-stack app <!-- omit in toc -->
### Coder Academy <!-- omit in toc -->
### T3A2 (Part A) Assignment <!-- omit in toc -->
#### Due Date: 23rd Nov 2022 <!-- omit in toc -->

---

## Table of Contents <!-- omit in toc -->
- [Links](#links)
  - [Live Production Site:](#live-production-site)
  - [Documentation Link:](#documentation-link)
  - [Server App Repository:](#server-app-repository)
  - [Client App Repository:](#client-app-repository)
- [Overview](#overview)
  - [Purpose](#purpose)
  - [Functionality \& Features](#functionality--features)
  - [Target Audience](#target-audience)
  - [Tech Stack](#tech-stack)
- [Libraries](#libraries)
  - [Client Libraries](#client-libraries)
  - [Server Libraries](#server-libraries)
- [Screenshots](#screenshots)
- [Dataflow Diagrams](#dataflow-diagrams)
    - [Note about the below diagrams](#note-about-the-below-diagrams)
    - [Dataflow Diagrams Legend](#dataflow-diagrams-legend)
    - [Diagram 1 - Client or Server App Production Deployment](#diagram-1---client-or-server-app-production-deployment)
    - [Diagram 2 - Sign-Up then Automatic Sign-In](#diagram-2---sign-up-then-automatic-sign-in)
    - [Diagram 3 - Logout](#diagram-3---logout)
    - [Diagram 4 - Co Cleanup 'Events' API Resource](#diagram-4---co-cleanup-events-api-resource)
    - [Diagram 5 - Co Cleanup 'Comments' API Resource](#diagram-5---co-cleanup-comments-api-resource)
    - [Diagram 6 (Part 1) - Administrator User Role - Find Any User](#diagram-6-part-1---administrator-user-role---find-any-user)
    - [Diagram 6 (Part 2) - Administrator User Role - Disable/Reenable Found User](#diagram-6-part-2---administrator-user-role---disablereenable-found-user)
    - [Diagram 7 - External 'Map' API Forward Geocoding](#diagram-7---external-map-api-forward-geocoding)
    - [Diagram 8 - External 'Map' API Rendering on Client App](#diagram-8---external-map-api-rendering-on-client-app)
- [Application Architecture Diagram](#application-architecture-diagram)
- [User Stories](#user-stories)
  - [User Stories - Board Link:](#user-stories---board-link)
  - [User Stories - About:](#user-stories---about)
  - [Revision 1:](#revision-1)
  - [Revision 2:](#revision-2)
  - [Revision 3:](#revision-3)
  - [Revision 4:](#revision-4)
- [Wireframes](#wireframes)
  - [Figma](#figma)
  - [Landing Page](#landing-page)
  - [Sign Up Page](#sign-up-page)
  - [Sign-In Page](#sign-in-page)
  - [Events Search Page](#events-search-page)
  - [Event Page](#event-page)
  - [Create \& Update Event Page](#create--update-event-page)
  - [User Dashboard](#user-dashboard)
  - [Admin Dashboard](#admin-dashboard)
- [Project Management](#project-management)
  - [Overview](#overview-1)
  - [Timeframe](#timeframe)
  - [Kanban Board](#kanban-board)
  - [Trello Implementation Board Link:](#trello-implementation-board-link)
  - [Scrum Sprints \& Ceremonies](#scrum-sprints--ceremonies)
    - [*Planning Meetings*](#planning-meetings)
    - [*Daily Standups*](#daily-standups)
    - [*Sprint Reviews*](#sprint-reviews)
  - [Task Delegation](#task-delegation)
    - [Overview](#overview-2)
    - [Kanban Tickets](#kanban-tickets)
    - [Sprint Planning](#sprint-planning)
    - [Strengths \& Weaknesses](#strengths--weaknesses)
  - [Pair Programming](#pair-programming)
  - [Source Control](#source-control)
- [Sprint 1](#sprint-1)
  - [Planning meeting 1](#planning-meeting-1)
  - [Planning meeting 2](#planning-meeting-2)
  - [Sprint Review](#sprint-review)
- [Sprint 2](#sprint-2)
  - [Planning meeting](#planning-meeting)
  - [Sprint Review](#sprint-review-1)
- [Sprint 3](#sprint-3)
  - [Planning meeting](#planning-meeting-1)
  - [Sprint Review](#sprint-review-2)
- [Sprint 4](#sprint-4)
  - [Planning meeting](#planning-meeting-2)
  - [Sprint Review](#sprint-review-3)
- [Sprint 5](#sprint-5)
  - [Planning meeting](#planning-meeting-3)
  - [Sprint Review](#sprint-review-4)
- [User Testing](#user-testing)
  - [Testing Process](#testing-process)
  - [User Testers](#user-testers)
  - [Testable Modules](#testable-modules)
    - [Functional Testing:](#functional-testing)
    - [Non-Functional Testing:](#non-functional-testing)
  - [Development Testing Environment](#development-testing-environment)
  - [Production Testing Environment](#production-testing-environment)
  - [Test Schedule](#test-schedule)
  - [Completed Test Cases](#completed-test-cases)
    - [Completed Test Cases - Development](#completed-test-cases---development)
    - [Completed Test Cases - Production](#completed-test-cases---production)
  - [Production Client Feedback](#production-client-feedback)

## Links

### Live Production Site:

[**https://cocleanup.social**](https://cocleanup.social/)

### Documentation Link:

[**https://github.com/Community-Cleanup/Co-Cleanup-Docs**](https://github.com/Community-Cleanup/Co-Cleanup-Docs)

### Server App Repository:

[**https://github.com/Community-Cleanup/Co-Cleanup-Server**](https://github.com/Community-Cleanup/Co-Cleanup-Server)

### Client App Repository:

[**https://github.com/Community-Cleanup/Co-Cleanup-Client**](https://github.com/Community-Cleanup/Co-Cleanup-Client)

## Overview

### Purpose

After a natural disaster strikes, communities are often left with the enormous clean-up effort required to restore people's homes, businesses and community areas. During these times government, council and emergency services resources are often stretched thin. Co Cleanup, short for Community Clean-up, aims to help communities better coordinate the clean-up process after a natural disaster, or any time that community members would like to coordinate group action for the betterment of their community. Clean-up tasks may involve the removal of debris, non-hazardous waste, and/or minor repairs, removal or replacements of small objects such as plants, furniture or garbage.

It should be noted that this platform is not to replace the coordination of emergency services in critical disaster recovery contexts or when the personal safety of any individual is at risk due to any given disaster situation.

**Co Cleanup has been designed and built by Chris Hullman and Mick Caffery as their final cap-stone project for Coder Academy???s Full Stack Development Bootcamp, 2022.**

### Functionality & Features

The functionality & features are described below for unregistered visitors, registered users and administrators. 

**Visitors**

- Can view the landing page to understand Co Cleanup's purpose and why it might be useful
- Can search and view all clean-up events (locations displayed on a map)
- Can view all details about clean-up events
- Are able to sign up to become a registered user
- Vital safety information displayed as paramount to all users attending a clean-up event, with reminders to leave critical emergency recovery situations to trained safety and recovery professionals (e.g. SES)

**Registered Users**

- Secure sign-up & sign-in with a robust cloud authentication platform (Firebase)
- Can create clean-up events
- Functionality to upload and display photos to an event the user has created.
  - **Due to the time constraints of the project, it was decided that the photo upload feature would not be included in Part B MVP scope.**
- Can register to participate in a clean-up event
- Can add comments to a clean-up event that you are registered for or have created

**Administrators**

- Assure the safety of registered users with the functionality of role-based access control (RBAC).
- Can search for and view all users
- Can deactivate or remove any users and events if any inappropriate content is shown.

### Target Audience

Co Cleanup is aimed at community members, organisations, emergency services or councils to help inform and coordinate clean-up efforts post-natural disaster. Willing volunteers can use this app to know the time and locations of coordinated clean-ups and where help is most needed.

### Tech Stack

**Front-end:** HTML5, CSS3, JavaScript, React.js, Axios

**Back-end:** Node, ExpressJS, Mongoose, MongoDB, Firebase Authentication

**Authentication:** Firebase Authentication

**Deployment (Server):** Heroku 

**Deployment (Database):** MongoDB Cloud Services

**Deployment (Front-End):** Netlify

**APIs** Mapbox maps & geocoding

**Testing:**  Jest

**Source Control:** Git & Github

**Project Management:** Trello & TeamGantt

**UI Design:** Figma

## Libraries

Co Cleanup is built on the full MERN stack (MongoDB, Express, React, Node).

A complete list of client and server libraries are listed below, along with a description of how they were implemented in the app. Node Package Manager (npm) was used as the package manager to install and update each of the libraries.

### Client Libraries

| n.o | Name | Version | Use | Docs |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| 1 | react | 18.2.0 | User Interface Components | [Link](https://www.npmjs.com/package/react) |
| 2 | react-dom | 18.2.0 | React Virtual DOM | [Link](https://www.npmjs.com/package/react-dom) |
| 3 | react-scripts | 5.0.1 | create-react-app Scripts | [Link](https://www.npmjs.com/package/react-scripts) |
| 4 | react-router-dom | 6.4.3 | React Client Routing | [Link](https://www.npmjs.com/package/react-router-dom) |
| 5 | axios | 1.1.3 | HTTP Client | [Link](https://www.npmjs.com/package/axios) |
| 6 | firebase | 9.13.0 | Authentication | [Link](https://www.npmjs.com/package/firebase) |
| 7 | styled-components | 5.3.6 | CSS-in-JS Components | [Link](https://www.npmjs.com/package/styled-components) |
| 8 | react-loader-spinner | 5.3.4 | SVG Loading Animation | [Link](https://www.npmjs.com/package/react-loader-spinner) |
| 9 | mapbox-gl | 2.10.0 | Maps | [Link](https://www.npmjs.com/package/mapbox-gl) |
| 10 | @mapbox/mapbox-gl-geocoder | 5.0.1 | Address Geocoding | [Link](https://www.npmjs.com/package/@mapbox/mapbox-gl-geocoder) |
| 11 | @testing-library/react | 13.4.0 | React DOM Testing Utilities | [Link](https://www.npmjs.com/package/@testing-library/react) |
| 12 | @testing-library/jest-dom | 5.16.5 | React Jest Testing | [Link](https://www.npmjs.com/package/@testing-library/jest-dom) |
| 13 | @testing-library/user-event | 13.5.0 | User Event Testing | [Link](https://www.npmjs.com/package/@testing-library/user-event) |
| 14 | web-vitals | 2.1.4 | Web Vitals Metrics | [Link](https://www.npmjs.com/package/web-vitals) |

- **1: react** - This package alone provides the high-level necessary functionality to define React components, included by default with Create React App, and is used by Co Cleanup in close alignment with the below package, react-dom.
- **2: react-dom** - This is used for React rendering for the web, and included with Create React App, and is used by Co Cleanup to allow React renderers to access the DOM.
- **3: react-scripts** - React scripts provide the code base from Create React App to handle the easy build and execution pipeline for the React app. With its listing in `package.json` scripts, Co Cleanup developers can execute these scripts every time by executing the React app with the command `npm start` (or `yarn start`), and building the production release with `npm build`.
- **4: react-router-dom** - React Router is a necessary use by Co Cleanup client app to simulate URL-based HTTP routing on the client, despite it being a Single Page Application (SPA). Co Cleanup's implementation of this includes automatic client-side navigation, and automatic redirection on any unhandled, 404 Not Found, page/component routes.
- **5: axios** - Axios, as a promise-based HTTP client for the browser in our case, is the primary library used by the client app to handle all HTTP requests, and the subsequent responses (successful or not), to our server API route end-points as RESTful operations. Axios provides easy-to-implement functions for handling the CRUD requests as HTTP verbs, and for including any body data or headers in each request.
- **6: firebase** - The Firebase JavaScript SDK, not to be confused with the Firebase Admin SDK described in the following section, implements the client-side libraries to interact with Firebase. Co Cleanup's implementation of this on the client app imports the Firebase Authentication services needed to both securely create a new user account on Firebase via email and password (i.e. sign up), and to sign in the user with authentication and validation, which if successful, generates a unique ID token (JWT). Co Cleanup client app uses this token for session persistence and to send as request headers to the Co Cleanup server app for processing by the Firebase Admin SDK (described in the following section).
- **7: styled-components** is a React specific CSS-in-JS styling package that allows for an HTML element to be styled with custom CSS and imported into JSX components. In our project, we utilised this package by doing all of our CSS stylings within styled-components. We broke our components into elements like buttons, input fields, etc. Then we made utility divs that applied margin, widths, padding, flex, grid, etc. 
- **8: react-loader-spinner** provided a simple React SVG spinner component that displayed during async await operations so that the user understood that the page was loading.
- **9: mapbox-gl** is a JavaScript library for interactive, customizable vector maps on the web provided by Mapbox. We used this library to display maps and location data as layers on each map. 
- **10: @mapbox/mapbox-gl-geocoder** is a geocoder control for mapbox-gl-js using the Mapbox Geocoding API. We used geocoding in our Event Forms to get addresses and the coordinates for each address. The Mapbox Geocoder with mapbox styling was built for vanilla JS projects, however we converted it to be used in a React component.
- **11: @testing-library/react** - React Testing Library (RTL) is a light-weight solution for testing React components. We installed this package as we were planning to implement detailed front-end testing. Due to time constraints and our current skills, we were not able to fully utilise RTL and will be an area for our team members to improve on after the completion of this assignment. 
- **12: @testing-library/jest-dom** is a part of the RTL library and allows for Jest to be used to write tests about the state of a DOM. 
- **13: @testing-library/user-event** is a part of the RTL library and simulates real events that would occur in a browser as a user interacts with it.
- **14: web-vitals** comes included with create-react-app projects. Taken from the web-vitals docs. web-vitals library is a tiny (~1.5K, brotli'd), a modular library for measuring all the Web Vitals metrics on real users, in a way that accurately matches how they're measured by Chrome and reported to other Google tools. We did not utilise this package, however, did not uninstall it (due to its size) in case we wanted to use it for future use.

### Server Libraries

| n.o | Name | Version | Use | Docs |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| 1 | express | 4.18.2 | RESTful API Framework | [Link](https://www.npmjs.com/package/express) |
| 2 | cors | 2.8.5 | CORS Middleware | [Link](https://www.npmjs.com/package/cors) |
| 3 | helmet | 6.0.0 | HTTP Headers | [Link](https://www.npmjs.com/package/helmet) |
| 4 | mongoose | 6.7.0 | MongoDB Object Modelling | [Link](https://www.npmjs.com/package/mongoose) |
| 5 | firebase-admin | 11.2.0 | Authentication | [Link](https://www.npmjs.com/package/firebase-admin) |
| 6 | dotenv | 16.0.3 | Environment Variable Storage | [Link](https://www.npmjs.com/package/dotenv) |

- **1: express** - Express is used as a minimal and flexible Node.js web application framework. It is used by Co Cleanup to establish and maintain a HTTP server that listens to HTTP requests and request methods from the client, and to handle HTTP API routes/end-points, middleware, and sending of HTTP responses to the client. Co Cleanup uses Express' application-level middleware, router-level middleware, and built-in middleware where appropriate. Express has also been configured to only accept incoming requests as JSON objects, and to respond with only JSON objects.
- **2: cors** - cors is used as Express middleware to enable CORS (Cross-origin resource sharing) for the Co Cleanup client-side app URL. It has been configured on the server to automatically apply CORS to all routes.
- **3: helmet** - Helmet is used as Express middleware as an extra security solution that sets various HTTP headers. Co Cleanup's implementation of helmet uses all default headers and their values, except that the Content-Security-Policy (CSP) header is configured with a specific directive to aid in mitigating XSS attacks.
- **4: mongoose** - Due to the NoSQL, schemaless nature of MongoDB, Mongoose is implemented in the Co Cleanup application to provide a schema-based solution, which the server app uses mostly for validation and type casting of values in MongoDB document storage. Its Object Data Modeling (ODM) library also provides easy-to-use methods for querying documents in MongoDB within our app's various middleware and other functions.
- **5: firebase-admin** - The Firebase Admin SDK is implemented and instantiated on Co Cleanup's server app, where only the Admin Auth API services are utilised. Specifically, the identity verification services that the Firebase Authentication API provides. When required, mostly on protected middleware routes, the Admin SDK verifies and decodes the Firebase ID token that is sent in from the client's request header to extract the token's claims (e.g. the email address), which is used to verify against the relevant MongoDB documents. Note that there is no implementation or use of any *custom* user claims by Co Cleanup.
- **6: dotenv** - Dotenv allows for the contents of private/secret `.env` files (contents as key/value pairs) to be automatically read and loaded as global environment variables (specifically, Node's `process.env` property) for use throughout both the server app and client app's lifecycle. Co Cleanup uses this specifically to hold the private credentials and connection details for Co Cleanup's Firebase and MongoDB accounts for app connection, authentication and authorisation. Note that the production, cloud deployment instances of the server app and client app have their own independent copy of these environment variables.

## Screenshots

## Dataflow Diagrams

**Update 23/11/2022 - Unfortunately, no change has been made to any of the below Dataflow Diagrams and their description since the Part A assessment submission due to time constraints. The current implementation of Co Cleanup has some slight modifications to the dataflows described.**

#### Note about the below diagrams

Besides the 'Legend' diagram below, all subsequent Dataflow Diagrams have their processes (circle shapes) numbered.

The numbered lists below each Dataflow Diagram indicate the sequence, in ascending order, of data flow for each process. Note however that many processes are performed asynchronously, or sometimes not at all for any given live process transaction - e.g. in the case of error responses.

#### Dataflow Diagrams Legend

![Data Flow Diagram - Legend](./docs/diagrams/data-flow-legend.png)

#### Diagram 1 - Client or Server App Production Deployment

![Data Flow Diagram - Diagram 1 - Client or Server App Production Deployment](./docs/diagrams/data-flow-diagram1.png)

1. One or more developers on a local development machine will push (or pull request) the latest code base to the central main/master branch of a version control/source code repository.
2. With repository and client or server app cloud 'Platform as a Service' (PaaS) authorised to link together, the initial version of the code base will automatically be sent to the PaaS system.
3. Polls will be sent to and/or from the repository and the PaaS system to monitor for codebase changes, and if a new change is detected, automatically re-push the new code onto the PaaS system (i.e. Continuous Deployment).
4. The client or server app PaaS system will request from a Certificate Authority (CA) for a new or renewed TSL/SSL certificate.
5. The signed certificate will be sent back to the client or server app PaaS system to enable HTTPS on the deployed client or server app.
6. For the client app, the public access keys to the cloud authentication services systems will be sent.
7. The cloud authentication services systems will return an authentication ID token to store in a cookie on the client app PaaS system.

#### Diagram 2 - Sign-Up then Automatic Sign-In

![Data Flow Diagram - Diagram 2 - Sign-Up then Automatic Sign-In](./docs/diagrams/data-flow-diagram2.png)

1. From a sign-up form on the client app, the user's username, email and password as user input will be added to the client app.
2. With the client-app-side validated username, email and password it will be sent as a POST request to the cloud authentication services. Included in the request will be a flag to bypass any email verification requirements for the sign-up.
3. With the cloud authentication services attempt at validating the email and password on its systems, if this is a *sign up*, attempt to save the user's email and secured password on its systems, alternatively for *sign in* attempt to retrieve the existing user from its systems. The auth services will respond back with an object to the client, depending on whether it was successful or not.
4. From process #3, one of three error responses may occur: "Weak Password", "Invalid Email", or "Operation Not Allowed". Or only "User Not Found" error if this is a *sign in* request only.
5. Alternatively, if successful user creation on the auth system services, return a response object with the ID token (JWT) with token metadata such as expiry time.
6. Clear any existing cookies stored on the end user's web browser.
7. Store a copy of the ID token on a cookie on the end-user's web browser.
8. Send a POST request to the server API app with the ID token for validation against the "admin" side of the cloud authentication services.
9. From process #8, an error response of "Connection Refused" may occur if there's a network error, for example.
10. Send a POST request with the ID token to the admin cloud authentication services to validate it.
11. If the ID token is deemed still valid, decode the user's claims from the payload to retrieve the user's details (email, username, etc.) in plain text.
12. With the decoded claims, as an object, and as a query filter, send a database query to the NoSQL database to create a new user (for *sign up*) on the database, or fetch the user (for *sign in*) from the database.
13. Respond with any connection/network errors to the database that may have occurred.
14. If the database query was successful retrieve the user's details from the database as a document as per NoSQL database design, which the server API app will handle and store as an object.
15. A promise from the client app for the user's details from the database should be resolved and the user's decoded details stored in *state* on the client app.

*Note that for any future requests to protected endpoints that require sign-in or other authorisation (e.g. user administrator role requirements), the token stored in the cookie from process #7 will be used to send back to the server API to repeat the above same token decoding and database query processes.*

#### Diagram 3 - Logout

![Data Flow Diagram - Diagram 3 - Logout](./docs/diagrams/data-flow-diagram3.png)

If the signed-in end-user clicks the logout button, the following three processes will occur:
1. The signed-in end-user fires/clicks the logout button on a webpage which will trigger a handler on the client app to request a logout.
2. Functions will be executed to delete the cookie on the end-user's web browser.
3. Functions will be executed to clear out the user *state* on the client app.

Alternatively, if a listener/observer on the client app detects from the cloud authentication services that the user's token has been changed or is no longer valid on the cloud auth services, process #5 will occur to trigger the same processes as processes #2 and #3, above.

#### Diagram 4 - Co Cleanup 'Events' API Resource

![Data Flow Diagram - Diagram 4 - Co Cleanup 'Events' API Resource](./docs/diagrams/data-flow-diagram4.png)

1. The end-user triggers an action on their webpage to see all created events.
2. Or, the end-user triggers an event on their webpage to see only their own created events.
3. Or, the end-user triggers an event on their webpage to see a particular event by requesting the unique ID (UID) of the event.
The client app will then either send one of the following relevant CRUD requests (from #4 to #9) to the server API app:
4. Send a GET request for all existing events.
5. Send a GET request for the user's own created events.
6. Send a GET request to get a particular event by its UID.
7. Send a POST request to create a new event with the event details (title, address, description, etc.) as an object - only if the user is signed in.
8. Send a PUT request to edit an event with the updated details as an object - only if the user is signed in, and it's their own event or the user is an administrator.
9. Send a DELETE request to delete an event - only if the user is signed in, and it's their own event or the user is an administrator.
10. The server API app may respond with one of the following two errors: "Connection Refused", or later on, a database query error back to the client app as an object.
11. Query the database depending on the above CRUD operation chosen.
12. If the CRUD event requires authorisation permission and the server API app has approved this, e.g. the user is signed in, and whether or not the user is an administrator, conduct one of the following three CRUD processes against the database:
13. Query the database to create a new event.
14. Query the database to edit an event.
15. Query the database to delete an event.
16. If there is a database error, the server API app will retrieve a response that the database connection/network has failed as an object.
17. If the query operation was successful, respond with an object with details of the selected, or updated event. If the event was deleted, respond with the correct status code.
18. If the POST, PUT or DELETE CRUD operation was unauthorised, respond with a status code 401 error object.
19. The server API will respond to the client app with a validated model instance of the event(s) object including the status code/message.

#### Diagram 5 - Co Cleanup 'Comments' API Resource

![Data Flow Diagram - Diagram 5 - Co Cleanup 'Comments' API Resource](./docs/diagrams/data-flow-diagram5.png)

1. The end-user triggers an action on their webpage to see all comments by an event UID.
The client app will then either send one of the following relevant CRUD requests (from #2 to #4) to the server API app:
2. Send a GET request for all existing comments on an event.
3. Send a POST request for a new comment on an event with an object containing the comment description -  only if the user is signed in and they are attending the event.
4. Send a DELETE request to delete a comment - only if the user is signed in, and it's their own comment or the user is an administrator.
5. The server API app may respond with one of the following two errors: "Connection Refused", or later on, a database query error back to the client app as an object.
6. Query the database for comment(s) depending on the above CRUD operation chosen.
7. If the CRUD event requires authorisation permission and the server API app has approved this, e.g. the user is signed in, and whether or not the user is an administrator, conduct one of the following two CRUD processes against the database:
8. Query the database to create a new comment for an event.
9. Query the database to delete a comment on an event.
10. If there is a database error, the server API app will retrieve a response that the database connection/network has failed as an object.
11. If the query operation was successful, respond with an object with details of the selected comment. If the event was deleted, respond with the correct status code.
12. If the POST or DELETE CRUD operation was unauthorised, respond with a status code 401 error object.
13. The server API will respond to the client app with a validated model instance of the comment(s) object including the status code/message.

#### Diagram 6 (Part 1) - Administrator User Role - Find Any User

![Data Flow Diagram - Diagram 6-1 - Administrator User Role - Find Any User](./docs/diagrams/data-flow-diagram6-1.png)

1. The administrator end-user searches for any user by their username on their administrator-only webpage on the client app.
2. A GET request with the requested user's username as a query string/param is sent to the server API app.
3. The server API app may respond with one of the following two errors: "Connection Refused", or later on, a database query error back to the client app as an object.
4. Query the database with the requested user's username and find their database entry by their UID.
5. If there is a database error, the server API app will retrieve a response that the database connection/network has failed as an object.
6. If the query operation was successful, respond with an object with details of the selected user.
7. The promise on the client app should resolve successfully with the user's details from the server API app.

#### Diagram 6 (Part 2) - Administrator User Role - Disable/Reenable Found User

![Data Flow Diagram - Diagram 6-2 - Administrator User Role - Disable/Reenable Found User](./docs/diagrams/data-flow-diagram6-2.png)

1. The administrator end-user, with their found user, triggers a form action or button to enable or disable a user's account.
2. A PUT request with the found user's details with the enable/disable boolean is sent to the server API.
3. The server API app may respond with one of the following two errors: "Connection Refused", or later on, a database query error back to the client app as an object.
4. Query the database with the requested user's UID and find their database entry by their UID and update their database document with the enabled/disabled boolean.
5. If there is a database error, the server API app will retrieve a response that the database connection/network has failed as an object.
6. If the query operation was successful, respond with an object with details of the selected and now updated user.
7. The promise on the client app should resolve successfully with the now updated user's details from the server API app.

#### Diagram 7 - External 'Map' API Forward Geocoding

![Data Flow Diagram - Diagram 7 - External 'Map' API Forward Geocoding](./docs/diagrams/data-flow-diagram7.png)

1. The server API app sends a GET request of an object including the URL of the Geocoding API endpoint, and the query string/params of the access token for the API and the address of the location to forward geocode.
2. The server API app may respond with one of the following two errors: "Connection Refused", or an invalid access key/token error, as an object to the server API app.
3. If successful, the server API app will receive a resolved promise that the Geocoding API will respond with an object containing the latitude and longitude coordinates of the address if found.

#### Diagram 8 - External 'Map' API Rendering on Client App

![Data Flow Diagram - Diagram 8 - External 'Map' API Rendering on Client App](./docs/diagrams/data-flow-diagram8.png)

1. The client app sends a GET request of an object including the URL of the Maps API endpoint, and the query string/params of the access token for the API.
2. The client app may respond with one of the following two errors: "Connection Refused", or an invalid access key/token error, as an object to the client API app.
3. If successful, the client API app will receive a resolved promise that the Maps API will respond with the object with the map details that the pre-installed client-side SDK of the maps service can utilise to render the map graphics on the client app display.

## Application Architecture Diagram

![Application Architecture Diagram](./docs/diagrams/architecture.png)

**Legend**

1. The client (front end) represents the technologies that users interact with directly. The main components are React (components), Axios (XHR), and deployed on Netlify
2. React is an open-source front-end JavaScript library for building user interfaces with UI components. The diagram shows the main front-end React components that make up the application. Each of these components uses Axios to make XHR requests and the event pages use the Mapbox API for geocoding.  
3. Axios is a promise-based XMLHttpRequests (XHR) client that is used to make requests to the backend. These requests send and receive JSON data. An example is sending data from the ???Create Event??? form to a backend REST API endpoint. The React front-end components also receive JSON data via Axios to update state and access the data. 
4. The front end is built, deployed and hosted by Netlify, which also allows for automated deployments direct from GitHub. 
5. The server (back end) represents all of the technologies that process incoming requests from the client and generate the response. The server uses Node.js as an environment runtime, ExpressJS to create the REST API, Mongoose for database modelling, Firebase for user authentication and MongoDB as a cloud-hosted NoSQL database. 
6. Node.js is the environment runtime that executes JavaScript code outside of a web browser. 
7. ExpressJS is a backend framework that is used to build RESTful APIs. ExpressJS has been used to create all the backend API endpoints for CRUD operations for different database collections. 
8. Mongoose is used to create database models using schemas. These schemas represent how data will be stored in each database collection. Mongoose is responsible for creating and reading documents from the MongoDB database. 
9. The Node.js backend is built, deployed and hosted by Heroku. Heroku also allows for automated deployments direct from GitHub. 
10. Firebase Authentication provides a front and back-end authentication service, via node.js software development kits (SDK). These kits handle the authentication for the application. Firebase stores user details on a Firebase database. 
11. MongoDB is a NoSQL cloud-hosted database. With the use of Mongoose, data is modelled and stored within collections. 
12. The Mapbox Maps API is used to display Mapbox-created maps that can be used as a base layer for location data to be overlaid. The Mapbox Geocoding API converts location text into geographic coordinates. Geocoding is used when a user creates an event, then the location can be plotted on the base layer map. 

## User Stories

**Update 23/11/2022 - To keep track of which of our Git commits correspond to which User Story card number, it was opted that for Git commits for both the server app and client app code, all commits that related to a specific User Story card would begin with the sentence "US# - ...." followed by the rest of the commit message (the # being replaced with the number of the User Story card).**

### User Stories - Board Link: 

[**https://trello.com/b/kBMQdaEN/user-stories-co-cleanup**](https://trello.com/b/kBMQdaEN/user-stories-co-cleanup)

### User Stories - About: 

The Co Cleanup app User Stories Trello board has an **INFORMATION** list (first board column) with cards that explain the approach, formatting and syntax to reading and editing the board and its User Stories. Below are direct links to the information cards (for each card, please read the card title, and the card description, if there is one):

- Structure of a User Story text - [https://trello.com/c/ikJvrfnR](https://trello.com/c/ikJvrfnR)
- Who are the personas? - [https://trello.com/c/uO42CR5e](https://trello.com/c/uO42CR5e)
- About RED labelled cards - [https://trello.com/c/FrhWO1ks](https://trello.com/c/FrhWO1ks)
- About ORANGE labelled cards - [https://trello.com/c/DpYXKgNt](https://trello.com/c/DpYXKgNt)
- How to delete/discard cards - [https://trello.com/c/3QqTMrCv](https://trello.com/c/3QqTMrCv)
- How to edit cards - [https://trello.com/c/zDDxwutQ](https://trello.com/c/zDDxwutQ)

### Revision 1:

This is the original draft User Stories version from Week 1 of the sprint, with the planned articulated User Stories categorised into persona needs and "must haves" vs "would like to have" features of the app.

![User Stories - Revision 1](./docs/trello-screenshots/user-stories-revision1.png)

### Revision 2:

In this revision from Week 2 of the sprint, the following changes were made:
- It was discussed and clarified that our target audience would like to see, as read-only, all existing cleaning events that are scheduled without needing to be signed in to the app.
- For clarity, when the user first signs up in the app, they can specify a nickname as their username, hence we discarded the user story card relating to concerns of privacy of the user's full, real name.

![User Stories - Revision 1](./docs/trello-screenshots/user-stories-revision2.png)

### Revision 3:

In this revision from Week 2 of the sprint, the following changes were made:
- The functionality for a user to upload and attach one or more photos to an event when creating their own event will be an optional (i.e. "would like to") requirement outside of the scope of the MVP and will be implemented if the timeframe allows.
- A user story card was added for the optional user want for a feature to be able to instant message/chat with other attendees of cleanup events.

![User Stories - Revision 3](./docs/trello-screenshots/user-stories-revision3.png)

### Revision 4:

In this final revision before the production release, the following change was made:
- Discarded User Story #23 as this was an accidental mistake as it was already a *MUST* requirement in User Story #21.

![User Stories - Revision 4](./docs/trello-screenshots/user-stories-revision4.png)

## Wireframes

### Figma

Our team used Figma to create our wireframes, allowing us to easily collaborate and share ideas. Our Figma wireframe project can be viewed at the below link. **Following Agile principles, we adjusted our wireframes as we gained feedback through the development process and user testing.** The revisions of our wireframes can be viewed on the different pages of the Figma project. 

[Figma Wireframes](https://www.figma.com/file/7jp9yPtxe7STeHsvZgwpen/Community-Cleanup-Wireframes?node-id=20%3A716&t=DgzonqlR0Dj8Op92-1)

### Landing Page

The landing page will be the page that visitors see when they navigate to the root URL. It is designed so that users can quickly learn what the app is for and why it might be useful for them. Details about this page include:

1. The search bar can be used by visitors who are not logged in to view events. When the search bar is focused, the landing page will navigate to the events search page. The about and volunteer links will navigate to information about how the site work and how users can volunteer at events. The create event link will navigate to the create event form, but only if the user is signed in. If the user is not signed in, then this form will navigate to the sign-up page.
2. The log-in and sign-up links will not be displayed if a user is signed in, instead a user account icon link will be displayed.
3. The landing page component will consist of a Co Cleanup title, a blurb about Co Cleanup, hero image and links to sign up and view events. 
4. The footer will have links to the about and contact pages, along with copyright text. 

![Landing Page Wireframe](./docs/wireframes/landing-page.png)

### Sign Up Page

The sign-up page is a minimal design that makes it clear to the user what is needed to sign up.

5. By signing up the users agree to the Terms of Service, Privacy Policy, and Cookie Policy. Colouring and underlining will show the user that these headings are also clickable links so that they can read the associated terms and policies.

![Sign Up Page Wireframe](./docs/wireframes/sign-up.png)

### Sign-In Page

The sign-in page is another minimal design and will use similar components for the sign-up page.

6. There will be a link to the sign-up page, in case the user has not created an account previously. 

![Sign In Page Wireframe](./docs/wireframes/sign-in.png)

### Events Search Page

7. The events search page is designed so that users can easily see which clean-up events have been organised and where they are located. As users search for either event names or locations, the list of events will be filtered, and associated markers displayed on the map.

![Home Events Page Wireframe](./docs/wireframes/home-search.png)

### Event Page

The event page is designed to clearly show all details about the upcoming event.

8. A register button so that signed-in users can register for an event. If the users are not registered, then this button will navigate them to the sign-in page. 
9. Is a feature for users to be able to leave comments about the event, so that event organisers can reply with further information. 

![Event Page Wireframe](./docs/wireframes/event.png)

### Create & Update Event Page

The create event page is designed so that users can easily create and update events. 

10. Signed-in users can navigate to this page from the create event button in the navbar. If they would like to update an event they can navigate to the update event page by a link in their user dashboard under the heading ???My Events???, which lists the events they have organised. 

![Create Event Page Wireframe](./docs/wireframes/create-event.png)

### User Dashboard

The user dashboard is designed so that users can easily see all details relating to them.

11. The details section will show their username and email which can be updated.
12. The ???Attending??? section will show all events that they have registered for. These events can be clicked and the user is navigated to the event page.
13. The ???My Events??? section will show a list of all the events that the user has created. They can choose to update or delete the event. 

![User Dashboard Page Wireframe](./docs/wireframes/user-dashboard.png)

### Admin Dashboard

The admin dashboard is designed so that administrators of Co Cleanup can manage users and events.

14. Admin can select if they will search for users or events. Once they have found the user or event, they can deactivate the user or event. 

![Admin Dashboard Page Wireframe](./docs/wireframes/admin-dashboard.png)

## Project Management

### Overview

In the beginning, we discussed how we should effectively manage the project, the tools we should use, and how to delegate tasks effectively. We aimed to incorporate different tools and methods from Agile Project Management frameworks like Scrum and Kanban that would suit our team size, project scope and timeframe. 

### Timeframe

We were given a timeframe of five weeks to complete both Part A and Part B of the assignment, starting on Wednesday 19th of October 2022 until the final due date of Wednesday 23rd of November 2022. The contact hours throughout the Bootcamp were Monday to Wednesday, 9 am to 5 pm. We chose to keep this as the core contact hours for the project. Due to team members' work commitments and job search efforts, we decided that any additional hours from Thursday to Sunday would be planned ahead.

### Kanban Board

We decided to use Trello to manage our Kanban board as we both had experience with this product. We used the Kanban board to create a backlog of tasks or user stories that would be required to move the project forward. Then move each item into an ???in progress??? section while being worked on and assign the task to the team member who will complete it. Finally, move the item to the ???done??? section once complete. As a team, we both took responsibility for organising the backlog, delegating the tasks and communicating to each which items were being updated or completed.

### Trello Implementation Board Link: 

[**https://trello.com/b/jLaQiEnG/implementation-board-co-cleanup**](https://trello.com/b/jLaQiEnG/implementation-board-co-cleanup)

### Scrum Sprints & Ceremonies

We decided to break the 5-week period into five sprints based on the Scrum framework. We would use these sprints to plan and build our product in a series of five iterations, which would help break down the final product into manageable pieces of work. We predict that this approach will help us ship our work sooner and more frequently, whilst giving us the opportunity to adapt and change as we receive feedback from user testing. 

#### *Planning Meetings*

We decided that each sprint would start each Monday and begin with the planning ceremony (meeting). During each planning meeting, we discussed what we would like to achieve during the sprint and the value that goal would bring to the project. We then moved items from the product backlog that was necessary to complete the sprint and delegated how we would complete these items. Finally, each of the items moved from the backlog was broken down into an increment that would be achievable to be completed in one day.

Based on this approach, each planning meeting addressed the following three questions:

**What is the main sprint goal and the value that would bring to the project?**

**Which items can be moved from the backlog to achieve this goal and who will work on them?**

**How should we break down the chosen items into daily increments?**

To help with tracking the tasks in each week's sprint we used a Gantt chart. The Gantt chart we used was a Trello power-up created by TeamGantt, making it easy to move tasks from the backlog into each sprint and delegate them. 

#### *Daily Standups*

The purpose of our team's morning standup (during core days) was to discuss the progress towards the sprint goal and adapt the backlog as necessary. We adjusted any delegation as necessary to help us both complete our tasks. As we were a small team of just two, on top of our morning stand-up we were in frequent communication throughout the day discussing any challenges or re-evaluating the daily plan. 

#### *Sprint Reviews*

The purpose of our sprint reviews is to review what was accomplished during the Sprint, adjust the product backlog, and determine future adaptations to the project. 

### Task Delegation

#### Overview

We aimed to be purposeful and considerate in how we delegated tasks. We wanted to both share the workload equally while taking into account our interests, strengths, and weaknesses. We discussed the delegation of tasks during our planning meetings and recorded task delegation in both Kanban task, user story cards and in our sprint planning Gantt chart. We then re-evaluated our assigned tasks each day during our stand-ups.  

#### Kanban Tickets

As shown in the below example of a Kanban user story card, each card was marked with the names of the team members who will work on the tasks within that card. The card was given an overall difficulty ranking to equally divide the difficult tasks. The example below shows the card difficulty ranked medium. 

![User Story Card Task Delegation](./docs/trello-screenshots/delegation-card.png)

Each user story card was then given the required tasks and sub-tasks to complete that User Story. Each subtask was delegated to a team member, or both of us if we preferred to use pair programming to complete that task. Assigned tasks reflected who would do the bulk of the work to complete each task. Communication was always free-flowing and we both helped each other whenever required with our assigned tasks. 

<img src="./docs/trello-screenshots/delegation-task.png" alt="User Story Tasks Delegation" width="500"/>

#### Sprint Planning

We then used the User Story Task delegation to plan our sprints and clearly identify on the sprint Gantt chart who will be completing each task. As shown below, the User Story number is recorded with each task and the names of those who will complete each task can be viewed in the assigned column. The User Story number is also recorded with each associated git commit and pull request. 

**The colour of the Gantt chart taskbars were designated *purple* for tasks we both worked on, *dark blue* for Chris, and *light blue* for Mick.** 

![User Story Tasks Delegation](./docs/trello-screenshots/delegation-sprint.png)

#### Strengths & Weaknesses

When delegating tasks we took into consideration the strengths and weaknesses of our team members, but also what areas we were both interested in learning and improving at. Above all we both wanted to improve in both our front-end and back-end skills and teach each other as much as possible so that we both finished this assignment as confident MERN full-stack developers. 

We both were equal in skills regarding both client and server-side development. However, we both had areas of the project that we were keen to explore and naturally we delegated tasks according to these interests. 

An example being Chris was interested in learning more about Authentication & Authorisation, particularly in relation to using Firebase, and naturally, Chris was delegated to do the bulk of these tasks and then demonstrate to Mick what he had learnt. 

Another example was Mick was interested in learning more about the Mapbox API and implementing mapping and geocoding. Hence, Mick was delegated the bulk of these tasks and in return was able to teach Chris about Mapbox. 

### Pair Programming

We wanted to incorporate pair programming into our workflow as a way to share knowledge, write better code and problem-solve together. We chose to use pair programming as a way to get started on our server and client code bases, and when each of us encountered any difficult work items. The main tool we used to pair program was VS Code Live Share. We discovered this was a great tool where we could collaborate and write code in unison live on the one project. While pair programming in VS Code Live Share we used Discord to provide video, voice and chat. 

### Source Control

We decided that the 'Git Feature Branch Workflow' would be the best for our team size and project requirements. Both of us would work on separate feature branches and push our branches to the central repository, then merge our changes into the main codebase using a pull request. This meant that the main codebase would never contain broken code and allow for continuous integration of the deployed back-end and front-end.

## Sprint 1

### Planning meeting 1

We kicked off the project with an initial planning meeting. This is where we discussed potential ideas and submitted our chosen idea for approval. We then discussed how we would like to manage the project and which tools and methods would suit. We then talked about the initial tasks that we both would work on. 

The Kanban board below was created after this initial planning meeting and reflects these initial tasks and backlog. We decided that we should place an emphasis on revising the MERN masterclass presented by our class instructors on the previous two days, as the concepts covered were crucial to our team performing well on this assignment.

![Week 1 Day 1 Trello Screenshot](./docs/trello-screenshots/day1-implement.png)

Due to the first day of the project starting on Wednesday, and the core contact hours for the project being Monday to Wednesday we decided that we would hold another planning meeting on the following Monday. 

### Planning meeting 2

**The topics discussed were:**

**What is the main sprint goal and the value it would bring to the project?**

- The main sprint goal this week was to have a basic Express server deployed to Heroku with CRUD functionality for ???users??? and ???events???, with data being stored on MongoDB cloud. On top of this, we would create a React Front end deployed to Netlify with a simple form to create an event. 
- A secondary goal was to have all of our initial users' stories documented
- These goals would bring value to our project by following the principles of CI/CD and the mantra ???deploy often and deploy early???. Due to the flexibility of Express and the MongoDB data structure we aimed to build a working ???core server??? that was deployed that we could build upon as we worked through each user story.

**Which items can be moved from the backlog to achieve this goal?**

- Items moved from the backlog included:
  - Setting up Express Back-end and deploy
  - Document user stories
  - Scaffold React front-end and deploy
  - Build basic forms for Register & Sign In
  - Build a basic form for Registering for an Event

**How should we break down the chosen items into daily increments?**

  - Monday would be spent developing User stories and documentation
  - Tuesday would be spent Setting up Express Back-end and deploy
  - Wednesday would be spent setting up React front-end, deployment and basic forms

### Sprint Review

The screenshots below show the implementation board at the end of sprint 1. We achieved the majority of what we planned for the sprint, however, did not start any development of the front end. The Gantt chart shows which items were worked on each day of the sprint. 

As this was the first sprint for the assignment we learnt a lot about time management and what is achievable in a single sprint. We also came up against parts of the development process that were more difficult than expected. 

During this sprint, a difficult task was understanding how to set up Firebase Authentication on the frontend. We decided that we should adjust our backlog and devote time to researching and understanding how best to implement Firebase authentication into our project. 

There were no major adaptations to the project. However, in review, we were able to adjust which tasks should be given priority in order to meet the assignment requirement of submitting the Part A documentation by the end of sprint two. 

![Sprint 1 Review Implementation Board](./docs/trello-screenshots/sprint1-implement.png)

![Sprint 1 Gantt Chart](./docs/trello-screenshots/sprint1-gantt.png)

## Sprint 2

### Planning meeting

**The topics discussed were:**

**What is the main sprint goal and the value that would bring to the project?**

- The main sprint goal this week was to research and understand Firebase Authentication. Our next main goal was to finish all the required wireframes, diagrams, and Readme documentation required for the Part A submission. 
- The value these goals would bring to the project would be that through a better understanding of authentication, we would be able to design and draw more accurate data flow diagrams, which is a requirement for Part A. The goal of finalising the Readme documentation ahead of time, will also allow us to review and make any changes before the Part A due date, and also enable us to continue working on Part B of the assignment. 

**Which items can be moved from the backlog to achieve this goal?**

- Items moved from the backlog included:
  - Research Firebase Authentication
  - Data Flow Diagram Increment 2
  - Architecture Diagram Increment 2
  - Finalise Wireframes
  - Finalise Part A Readme

**How should we break down the chosen items into daily increments?**

- Following on from our previous sprint, the dataflow diagram and architecture diagram have already been broken down into daily increments, with the first increments being completed in sprint 1. The remainder of the tasks have been planned to take less than one day.

### Sprint Review

The screenshots below show the implementation board at the end of sprint 2. The Gantt chart shows which items were worked on each day of the sprint. We successfully completed all of the major items and completed the Part A Submission ahead of time. 

There were no major adaptations to the project. The end of sprint 2 marks the end of our planning phase for the project. 

![Sprint 2 Review Implementation Board](./docs/trello-screenshots/sprint2-implement.png)

![Sprint 2 Gantt Chart](./docs/trello-screenshots/sprint2-gantt.png)


## Sprint 3

### Planning meeting

**The topics discussed were:**

**What is the main sprint goal and the value that would bring to the project?**

- The main sprint goal this week was to start working through the most important user stories and complete the associated tasks and subtasks. Some of the main features we focused on were authentication, sign up/in forms, landing page, and create & view events. 
- The value these goals would bring to the project would be that we would have working features that we can start show users and complete user tests on. These goals would also mean that we would be making good progress in completing part B of the assignment on time. 

**Which items can be moved from the backlog to achieve this goal?**

The user stories moved from the backlog and associated tasks are included below. The team member delegated to work on the task is provided next to the task.
- #1: MUST: Be able to see the Landing Page when I first enter the website, so that I know where and how to navigate around the app.
  - Scaffold initial React app code  - Chris & Mick (Pair Program)
  - Deploy Client App to Netlify and GitHub  - Chris & Mick (Pair Program)
  - Show Landing Page on root visit  - Chris & Mick (Pair Program)
- #4: MUST: Be able to see a link and forms to sign up/register so that I can create an account for myself if I choose to do so.
	- Configure React Router ??? Chris
	- Create Sign Up & Sign In forms - Chris
- #8 - MUST: Know that my name, email address and password are secured if I choose to sign up so that my details are kept safe.
	- Secure User Sign Up/In Forms ??? Chris
	- Firebase Client User Sign Up/Sign In ??? Chris
	- Send User ID Token to Server API App- Chris
- #3 - MUST: Be able to create & update a cleanup event with the important information about it so that other registered users can join if they wish.
  - Create Form to Create/Update Events ??? Mick
  - Create Mapbox Geocoding Component - Mick
- #12 - MUST: Be able to view all existing cleanup events so I can see what is happening.
	- Display Event Locations on Map ??? Mick
	- Filter and Display Events as a List - Mick

**How should we break down the chosen items into daily increments?**

- Each of the tasks was designed to be less than one day of work. The tasks were broken down further into subtasks which can be viewed within the Trello board by following the link. 

### Sprint Review

The screenshots below show the implementation board at the end of sprint 3. The Gantt chart shows which items were worked on each day of the sprint. We successfully completed all of the major tasks and are on track to complete part B of the assignment by the due date. 

There were no major adaptations to the project. We had some discussions about possibly using TailwindCSS for styling. We thought that using TailwindCSS may save us some time and provide a consistent style across the app. 

![Sprint 3 Review Implementation Board](./docs/trello-screenshots/sprint3-implement.png)

![Sprint 3 Gantt Chart](./docs/trello-screenshots/sprint3-gantt.png)

## Sprint 4

### Planning meeting

**The topics discussed were:**

**What is the main sprint goal and the value that would bring to the project?**

- The main sprint goal this week was to continue working through user stories with the aim to have a functioning minimum viable product (MVP) by the end of the week. Some of the main features we focused on were the administration dashboard, user account page, event comments, adding styling and improving flow.
- The value these goals would bring to the project would be that we would have a fully functioning app that we can start road testing with users and continue testing. Achieving these goals would also mean that we would be on track to complete part B of the assignment on time. 

**Which items can be moved from the backlog to achieve this goal?**

User stories moved from the backlog, associated tasks, and delegation included:
- #5: MUST: Be able to navigate backwards and forwards between all the web pages available to me so that I don't get lost or find broken links.
  - Configure React Router ??? Chris & Mick
- #7: MUST: Expect what the interface elements do such as buttons and input fields so that I know how to interact with the application.
	- Create & Implement Styled-Components - Mick
	- Update Wireframes based on testing feedback - Mick
- #10: WOULD LIKE: For the interface to be aesthetically pleasing so that I feel pleasure using the app.
	- Add CSS-in-JS Styling for all Styled Components ??? Mick
- #11: MUST: Be able to join any existing, open cleanup event if I choose to do so.
  - Add User Registration Feature to Events ??? Mick
- #13: MUST: Be able to add comments on an event that I am attending so that I can openly share information and ask questions for other attendees to see.	
  - Add Comments Feature to Events ??? Mick
- #19: MUST: Be able to delete any users' created events deemed inappropriate so that the community is kept safe and welcoming.
	- Configure protected route for admin to delete events ??? Chris
	- Change admin dashboard to view and delete events ??? Chris
- #20: MUST: Be able to disable or reenable a user's account that is fake, inappropriate, or violating terms of use of the app so that the community is kept safe and welcoming.
  - Configure protected route for admin to disable/reenable users ??? Chris
  - Change admin dashboard to disable/reenable users ??? Chris
- #21: MUST: To be able to assign the administrator role to any non-admin registered user, so that other administrators can help out.
	- Configure protected route for admin to assign/revoke admin role
	- Change admin dashboard to assign/revoke admin role
- #22: MUST: Be able to delete any users' comments deemed inappropriate so that the community is kept safe and welcoming.
	- Configure protected route for admin to delete comments ??? Chris
	- Change admin dashboard to view and delete comments ??? Chris

**How should we break down the chosen items into daily increments?**

- Each of the tasks was designed to be less than one day of work. The tasks were broken down further into subtasks which can be viewed within the Trello board by following the link. 

### Sprint Review

The screenshots below show the implementation board at the end of sprint 3. The Gantt chart shows which items were worked on each day of the sprint. Sprint 4 was our largest sprint in terms of workload for the entire project. We both were able to clear our schedules for the entire week to solely work on the project. We were able to achieve a working application that meets the requirements of the project that we can continue testing and refining. 

A notable adaptation to the project during this sprint was the inclusion of the Styled Components library as a way to create a consistent look and theme for the application and create reusable styling. We discussed in detail about the pros and cons of using either Material UI, TailwindCSS or Styled Components. Both of us had little experience with Material UI and Mick only had experience with TailwindCSS. Both of us had strong CSS skills so we decided to go with Styled Components. 

![Sprint 4 Review Implementation Board](./docs/trello-screenshots/sprint4-implement.png)

![Sprint 4 Gantt Chart](./docs/trello-screenshots/sprint4-gantt.png)

## Sprint 5

### Planning meeting

**The topics discussed were:**

**What is the main sprint goal and the value that would bring to the project?**

- This is the final sprint for the project. It is a half sprint has the assignment is due on Wednesday, 23rd November. 
- The main sprint goals this week was to add finishing touches to the app, finalise testing and documentation, and submit on time.

**Which items can be moved from the backlog to achieve this goal?**

User stories moved from the backlog, associated tasks, and delegation included:
- #2: MUST: Be able to read about the app's purpose on the Landing Page or About Page so that I can learn what the app is for and why it might be useful for me.
  - Add the About Page ??? Mick
- #6: MUST: Be able to read the Terms and Conditions, or Privacy Policy, of the app, so that I am aware of my privacy and I understand how the app uses my information.
	- Add Policy Pages ??? Mick
- Finalise Front-End Jest Tests ??? Chris & Mick
- Complete User Testing Spreadsheets & work through Issues ??? Chris & Mick
- Create Client (user) google feedback form and work through responses - Chris
- List and describe Libraries used in client and server ??? Chris & Mick
- Presentation Slides ??? Mick
- Finalise Documentation & Submit ??? Chris & Mick

**How should we break down the chosen items into daily increments?**

- Each of the tasks was designed to be less than one day of work. The tasks were broken down further into subtasks which can be viewed within the Trello board by following the link. 

### Sprint Review

The screenshots below show the implementation board at the end of sprint 5. The Gantt chart shows which items were worked on each day of the sprint.  **Due to this being the final sprint, the implementation board has been re-arranged to better display which tasks were completed on each sprint** 

Sprint 5 mainly consisted of finalising our app by finishing all testing and fixing any small issues that arose. Through Agile processes and consistent effort, we achieved the MVP that was scoped at the beginning of the project. 

![Sprint 5 Review Implementation Board](./docs/trello-screenshots/sprint5-implement.png)

![Sprint 5 Gantt Chart](./docs/trello-screenshots/sprint5-gantt.png)

## User Testing

### Testing Process

The documented testable items have their test cases categorised to provide extensive code-coverage, using a mixture of the following testing categories:
- Black-box testing (client feedback)
- White-box testing (developers)

The below user testers, as the primary developers of Co Cleanup app, have knowledge of the inner-workings of the app codebase. As such, an estimated capability of a typical end-user's webpage UI interaction capability and computer literacy skills will be considered in evaluating the pass/fail status of any black-box testing, test cases.

### User Testers
- Chris Hullman (Developer)
- Mick Caffery (Developer)

### Testable Modules

#### Functional Testing:

Test Modules:
- #1: User Sign Up
- #2: User Sign In
- #3: Event CRUD Operations
- #4: Event Comments CRUD Operations
- #5: Administrator User CRUD Operations

#### Non-Functional Testing:

Test Modules:
- #6: Page Navigation

### Development Testing Environment

Please refer to the [Application Architecture Diagram](#application-architecture-diagram) as the infrastructure used for development testing, with the following modifications for the development testing environment:
- Netlify: 
    - Netlify will instead be replaced with a `localhost` instance on a local machine running a version of `Node JS` that is capable of executing the packages defined in the client app's `package.json`.
    - Local private copies of related environment variables will be referred to instead of Netlify.
- Heroku:
    - Heroku will instead be replaced with a `localhost` instance on a local machine running a version of `Node JS` that is capable of executing the packages defined in the server app's `package.json`.
    - Local private copies of related environment variables will be referred to instead of Heroku.

The `localhost` environments listed above are configured to represent the cloud-hosted services as accurately as possible within the scope of the aforementioned testable items to minimise future potential testing errors in production.

Production instances of the below external services/APIs are used for development testing:
- Firebase authentication
- MongoDB
- MapBox

### Production Testing Environment

Please refer to the [Application Architecture Diagram](#application-architecture-diagram) as the infrastructure used for production testing.

All environment variables required by both the server app and client app code are securely stored in the production Heroku and Netlify instances, respectively.

### Test Schedule

Manual testing of test cases, and Jest unit-testing or integration-testing, are each performed on-demand by the user testers at a time when the developers agree that the corresponding testable module for the test cases has been programmed and integrated into the Co Cleanup app.

### Completed Test Cases

The numbered test modules listed in **Testable Modules** above have been sorted into the below spreadsheets and completed by testers

#### Completed Test Cases - Development

Please find the link to the latest completed development test cases spreadsheets below:
**Link:** [**Completed Development Testing Spreadsheets**](https://docs.google.com/spreadsheets/d/1BV3NmIpS4TwTJyvf1_pC0X-nhtN5ZabfryrJLH98Mgs/edit?usp=sharing)

#### Completed Test Cases - Production

Please find the link to the latest completed production test cases spreadsheets below:
**Link:** [**Completed Production Testing Spreadsheets**](https://docs.google.com/spreadsheets/d/1D71VNlbsv3_D9KFeyZcGyVWGpsjTuH32cBMGcCHDnAs/edit?usp=sharing)

### Production Client Feedback

To facilitate black-box testing with real end-users, the following client feedback form has been developed and sent to potential clients/end-users and their anonymous responses will be recorded and charted throughout production use:

[**https://forms.gle/2ioNPsYYRaesKjbh7**](https://forms.gle/2ioNPsYYRaesKjbh7)
