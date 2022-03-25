# Project Overview

## Project Schedule

| Day   | Deliverable                          | Status     |
| ----- | ------------------------------------ | ---------- |
| Day 1 | Planning and Approval                | Incomplete |
| Day 2 | Set up backend files and structure, test and deploy backend | Incomplete |
| Day 3 | Set up frontend files, connect frontend with backend, begin MVP attainment | Incomplete |
| Day 4 | Attain MVP, debug MVP, begin styling | Incomplete |
| Day 5 | Finalize CSS Styling and Responsive Design, begin postMVP if MVP attained | Incomplete |
| Day 6 | Confirm finalized MVP & Bug Fixes | Incomplete |
| Day 7 | Final Touches and deploying frontend | Incomplete |

## Project Description

Love language (name tbd) is an app that allows users to create an account, and then add their top 5 love languages. Users can also search for other users and view their top 5 love languages. 

This app will include a backend database using SQL and Django and a frontend web application using React.js.

## User Stories

Taken from the offical [5 love languages website](https://www.5lovelanguages.com/learn): "different people with different personalities give and receive love in different ways. By learning to recognize these preferences in yourself and in your loved ones, you can learn to identify the root of your conflicts, connect more profoundly, and truly begin to grow closer."

The user of this app values how love languages can impact relationships (both friendship and romantic). However, it is very hard to keep track of your social network's love languages; it's even hard to remember your own love languages! Users of this application look for a centralized place where they can easily access their top 5 love languages as well as their social network's love languages.  

## Wireframes

- [Mobile & Desktop](https://s3.amazonaws.com/assets.mockflow.com/app/wireframepro/company/C9c1df959635a4aee914f74a5cf3d9a7b/projects/M40WmDPcunb/pages/0aea6d2b5be04142ac95939134f00557/image/0aea6d2b5be04142ac95939134f00557.png?1648237490386)

### MVP/PostMVP

#### MVP

- 2 models for data (User, Love)
- Fully functional user authentication (token) (signup, signin, signout, changepassword, deleteaccount)
- Ability to search by email (or username?)
- CRUD functionality (Add User/Love, View Love, Edit User/Love, Delete User/Love)
- Routes and components on frontend (Home, Signup, Signin, Search, About)
- Fetch data from backend API
- Responsive design from mobile to desktop
- Use React bootstrap for design
- Fully Deployed frontend and backend

#### PostMVP

- Social network system (add friends so you can see their love languages without searching)

## Models

```py

# Example from lecture
class User(AbstractBaseUser, PermissionsMixin):
    
    email = models.EmailField(max_length=255, unique=True)
    is_active = models.BooleanField(default=True)
    is_staff = models.BooleanField(default=False)

    USERNAME_FIELD = 'email'

    objects = UserManager()

    def __str__(self):
        """Return string representation of the user"""
        return self.email

class Love(models.Model):
    one: models.CharField(max_length=100)
    two: models.CharField(max_length=100)
    three: models.CharField(max_length=100)
    four: models.CharField(max_length=100)
    five: models.CharField(max_length=100)
    owner = models.ForeignKey(
        get_user_model(),
        on_delete = models.CASCADE
    )

    dunder method 
```

## Routing Table

| **URL**     | **HTTP Verb** | **Description** |
| ----------- | ------------- | ---------------- |
| /sign-up | POST | Sign up a new user |
| /sign-in | POST | User sign in |
| /sign-out | DELETE | User sign out |
| /change-password | PATCH | User change password |
| /love-languages | POST | Add 5 love languages to user's account |
| /love-languages/<int:pk> | GET | View 5 love languages of signed-in user |
| /love-languages/<int:pk> | DELETE | Delete 5 love languages of signed-in user |
| /love-languages/<int:pk> | PUT | Update 5 love languages of signed-in user |
| /love-languages/search/<int:pk> | GET | Search and return another user's 5 love languages |

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
React Bootstrap
## Code Snippet

```
TBD :-) 
```

## Issues and Resolutions
TBD :-)
