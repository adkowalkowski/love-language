# Project Overview

## Project Schedule

| Day   | Deliverable                          | Status     |
| ----- | ------------------------------------ | ---------- |
| Day 1 | Planning and Approval                | Incomplete |
| Day 2 | Set up backend files and structure, test and deploy backend   | Incomplete |
| Day 3 | Set up frontend files, connect frontend with backend | Incomplete |
| Day 4 | Attain MVP, debug MVP, begin styling | Incomplete |
| Day 5 | Finalize CSS Styling and Responsive Design, begin postMVP if MVP attained | Incomplete |
| Day 6 | Confirm finalized MVP & Bug Fixes | Incomplete |
| Day 7 | Final Touches and deploying frontend | Incomplete |

## Project Description

Love language (name tbd) is an app that allows users to create an account, and then add their top 5 love languages. Users can also search for other users and view their top 5 love languages. 

This app will include a backend database using SQL and Django and a frontend web application using React.js.

## User Stories

The user of this app loves to travel and is looking for a way to store flight and hotel ideas and compare for the best options. They are always browsing multiple sites but lose their place and want to hold it all in one location. This user is also concerned with budget and would like to compare different options to see what the most fiscally responsible idea is.

## Wireframes

- [Mobile & Desktop](https://s3.amazonaws.com/assets.mockflow.com/app/wireframepro/company/C9c1df959635a4aee914f74a5cf3d9a7b/projects/M40WmDPcunb/pages/0aea6d2b5be04142ac95939134f00557/image/0aea6d2b5be04142ac95939134f00557.png?1648237490386)

### MVP/PostMVP

#### MVP

- 4 models for our data (Traveller, Trip, Flight, Hotel)
- CRUD functionality
- Have Routes and components on frontend
- Fetch data from backend API
- Responsive design from mobile to desktop
- Use bootstrap for design
- Fully Deployed frontend and backend
- Sorting functionality within each trip based on budget

#### PostMVP

- Login authentication
- View friends' travel plans
- Adding animations

## Models

```js

Traveller = {
    name: String,
    email: String,
    trips: []
}

Trip = {
    name: String,
    budget: Number
    start_date: Date,
    end_date: Date
    flights: [],
    hotels: []
}

Flight = {
    name: String,
    link: String,
    price: Number
}

Hotel = {
    name: String,
    link: String,
    price: Number
}

```

## Routing Table

| **URL**     | **HTTP Verb** | **Action** | **Description**              |
| ----------- | ------------- | ---------- | ---------------------------- |
| /traveller  | POST          | create     | add new user                 |
| /trip       | POST          | create     | add new trip                 |
| /trip       | GET           | show       | show all of this users trips |
| /trip/:id   | GET           | show       | show specific trip           |
| /trip/:id   | PUT           | update     | update specific trip         |
| /trip/:id   | DELETE        | delete     | delete specific trip         |
| /flight     | POST          | create     | add flight                   |
| /flight/:id | GET           | show       | show flight                  |
| /flight/:id | PUT           | update     | edit flight                  |
| /flight/:id | DELETE        | delete     | delete flight                |
| /hotel      | POST          | create     | add hotel                    |
| /hotel/:id  | GET           | show       | show hotel                   |
| /hotel/:id  | PUT           | update     | edit hotel                   |
| /hotel/:id  | DELETE        | delete     | delete hotel                 |

## Functional Components

| Component                      |                   Description                    |
| ------------------------------ | :----------------------------------------------: |
| Home                           |        Landing Page to add new traveller         |
| Trips                          | Page to view trips and add new trips to plan for |
| Trips - Specific Trip          |  View all potential flights and hotels for trip  |
| Trips - Specific Trip - Flight |        Add/update/delete flights for trip        |
| Trips - Specific Trip - Hotel  |        Add/update/delete hotels for trip         |
| About                          |            About the site and creator            |
| Header                         |                  Logo and Menu                   |
| Footer                         |         Copyright tag and link to github         |

#### MVP

| Component                          | Priority | Estimated Time | Actual Time |
| ---------------------------------- | :------: | :------------: | :---------: |
| Installing and Setup for backend   |    H     |      1hr       |     hr      |
| Models                             |    H     |      3hr       |     hr      |
| CRUD Routes and testing on Postman |    H     |      3hr       |     hr      |
| Deploying backend                  |    H     |     1.5hr      |     hr      |
| Creating React App                 |    H     |      1hr       |     hr      |
| Add Routes                         |    H     |      2hr       |     hr      |
| Create Components                  |    H     |      5hr       |     hr      |
| Sorting functionality              |    H     |      3hr       |     hr      |
| Fetch and test data on frontend    |    H     |      5hr       |     hr      |
| Responsive Design                  |    H     |      4hr       |     hr      |
| CSS and Bootstrap                  |    H     |      5hr       |     hr      |
| Deploy frontend                    |    H     |      1hr       |     hr      |
| Total                              |    H     |     34.5hr     |     hr      |

#### PostMVP

| Component            | Priority | Estimated Time | Actual Time |
| -------------------- | :------: | :------------: | :---------: |
| Friends              |    L     |      6hr       |     hr      |
| Login Authentication |    H     |      4hr       |     hr      |
| Animations           |    H     |      4hr       |     hr      |
| Total                |    H     |      14hr      |     hr      |

## Additional Libraries

## Code Snippet

```

```

## Issues and Resolutions

