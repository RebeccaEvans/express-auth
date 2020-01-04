# Express Auth

This is some boilerplate code for projects. This is a bare bones node/express app with basic local user authentication. It exists so that *I don't have to start from scratch on my projects*.

## What it includes

* Sequelize user model / migration
* Settings for PostgreSQL
* Passport and passport-local for authentication
* Sessions to keep user logged in between pages
* Flash messages for errors and successes
* Passwords that are hashed with BCrypt
* EJS Templating and EJS Layouts

### User Model

| Column Name | Data Type | Notes |
| --------------- | ------------- | ------------------------------ |
| id | Integer | Serial Primary Key |
| createdAt | Date | Auto-generated |
| updatedAt | Date | Auto-generated |
| firstname | String | Must be provided |
| lastname | String | - |
| username | String | - |
| email | String | Must be unique / used for login |
| password | String | Stored as a hash |
| photoUrl | String | Profile Picture |
| admin | Boolean | Defaults to false |
| bio | Text | - |
| birthday | Date | - |

### Default Routes

| Method | Path | Location | Purpose |
| ------ | ---------------- | -------------- | ------------------- |
| GET | / | index.js | Home page |
| GET | * | index.js | Render error/404 page |
| GET | /auth/login | auth.js | Login form |
| GET | /auth/signup | auth.js | Signup form |
| POST | /auth/login | auth.js | Login user |
| POST | /auth/signup | auth.js | Creates User |
| GET | /auth/logout | auth.js | Removes session info |
| GET | /profile | profile.js | Regular User Profile |
| GET | /profile/admin | profile.js | Admin User Profile |

## Steps To Use
