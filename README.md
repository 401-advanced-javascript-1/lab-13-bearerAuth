# JS401 - Lab-11 Authentication
## Author: Cory Henderson
This lab contains a working server with basic auth and OAuth.  The assignment requires the addition of a bearer authenticaion system with optional token expiry, api keys, and single use tokens.

## Links and Resources
- [Github Repo](https://github.com/401-advanced-javascript-1/lab-13-bearerAuth/tree/submission)
- [Travis](https://www.travis-ci.com/401-advanced-javascript-1/lab-13-bearerAuth)
- [Heroku](https://blooming-eyrie-20362.herokuapp.com/)

## Documentation

# Modules
- index.js
- app.js
- middleware - 404.js, 500.js 
- middleware.js
- router.js
- users-model.js

# Setup
- .env requirements
  - MONGODB_URI=mongodb://localhost:27017/teams
  - PORT=3000 (for nodemon)
- Running the app:
  - Start mongo server: mongo
  - Running http signup: echo '{"username":"Cory", "password":"things"}' | http post :3000/signup
    - This will generate a user token
  - After signup, user info will be saved to mongoDB.
  - Now use http post :3000/signin "Authorization: Bearer (your token) to signin with bearer authorization

## Tests
- Testing for expected route endpoints is performed using jest.
