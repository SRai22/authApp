# authApp with Express, Passport, and MongoDB
Web-602-Spring 2025

## Overview
This project is a user authentication system built using **Node.js**, **Express**, **Passport.js**, and **MongoDB**. It provides a simple login and session management system with authentication and authorization features. The front-end is built using **HTML, CSS, and JavaScript**.

## Features
- User registration and authentication using **Passport.js** and **passport-local-mongoose**.
- Secure session management using **express-session**.
- Login system with redirection to a private admin area.
- Logout functionality with session destruction.
- Client-side JavaScript to dynamically display user-specific content.
- Persistent storage using **MongoDB** with Mongoose ORM.

## Technologies Used
- **Backend:** Node.js, Express.js
- **Authentication:** Passport.js, passport-local-mongoose
- **Database:** MongoDB, Mongoose
- **Frontend:** HTML, CSS, JavaScript

## Installation
### Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- [MongoDB](https://www.mongodb.com/)

### Steps to Install
1. Clone the repository:
   ```bash
   git clone https://github.com/SRai22/authApp.git
   cd authApp
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start MongoDB (if not already running):
   ```bash
   mongod
   ```
4. Run the server:
   ```bash
   npm start
   ```
5. Open a browser and navigate to:
   ```
   http://localhost:3000/login
   ```

## Folder Structure
```
project-folder/
│-- html/
│   │-- index.html
│   │-- login.html
│   │-- private.html
│-- css/
│   │-- styles.css
│-- index.js
│-- package.json
│-- README.md
```

## Usage
### Register Users
By default, the system does not have a registration page. To register users manually, use the commented-out registration lines in `index.js`:
```javascript
// UserDetails.register({username:'paul', active: false}, 'paul');
// UserDetails.register({username:'joy', active: false}, 'joy');
// UserDetails.register({username:'ray', active: false}, 'ray');
```
Uncomment these lines, restart the server, and comment them again after running once.

### Login
- Navigate to `/login` and enter credentials.
- If successful, the user is redirected to `/` (home page), where their username is displayed dynamically.

### Logout
- Clicking "Log Out" removes the session and redirects to the login page.

## API Endpoints
| Method | Route     | Description |
|--------|----------|-------------|
| GET    | `/login`  | Serves the login page |
| POST   | `/login`  | Authenticates user and starts session |
| GET    | `/`  | Serves the main page with user session info |
| GET    | `/private` | Serves the private admin page |
| GET    | `/user` | Returns logged-in user data |
| GET    | `/logout` | Logs out the user and redirects to login |


## License
This project is licensed under the MIT License.



