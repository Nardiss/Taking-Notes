# Taking-Notes
# Express.js: Note Taker - UW Coding Bootcamp


# Description
For week 11 of the UW Coding Bootcamp my homework invited me to build an application called Note Taker that can be used to write and save notes. This application uses an Express.js back-end and it saves and retrieves note data from a JSON file.

This assignment started with a front-end for the application, I built the back end, connected the two and have deployed the application to Heroku.

Built With
JavaScript
Express.js
Node.js
npm modules
Heroku
Developer Mozilla
Link to Site GitHub Repo
Deployed Site via Heroku

# Github Repo



# Installation
Clone or download repo via Github and install dependencies.
Or visit the deployed site via Heroku with the link provided above.

# Usage
Deployed via Heroku (see link above)

# Tests
Not applicable.

# Snippet
This a code snippet from the server.js file..

// DEPENDENCIES - npm packages that will give our server useful functionality
const express = require('express');

// EXPRESS CONFIG - sets up basic properties for our express server
// Tell node we are creating "express" server
const app = express();
// Setting a port - will be used later in our listener
const PORT = process.env.PORT || 3000;

// Sets up the Express app for data parsing
app.use(express.urlencoded({ extended: true}));
app.use(express.json());
app.use(express.static('public'));

// ROUTER - points our server to a series of "route" files
// These routes give our server a "map" of how to respond when users visit or request data from URLs.
require('./routes/apiroutes')(app);
require('./routes/htmlroutes')(app);

// LISTENER
// Effectively starts our server
app.listen(PORT, function() {
    console.log(`Server is listening on PORT: ${PORT}`);
});




# Authors

Nardos Abraha
