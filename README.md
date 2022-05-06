# Social Media API

Unit 18, NoSQL Assignment 

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


(This is a working draft - project not yet submitted)


  ---
  ## Description

This is an API for a social network web application where users can share their thoughts, react to friends' thoughts, and create a friend list. It uses Express.js for routing, a MongoDB database, the Mongoose ODM, and native JavaScript Date object to format timestamps. The seed data is created using Insomnia.  

[Image seed data on Insomnia](Image)

To see how the API works using Insomnia, see the **walk through demonstration** video [here](Google Drive link).

While the application **files** can be accessed on my [GitHub Repository](https://github.com/jbtiglao/social-media-API).

  ---
  ## Table of Contents
  1. [Title](#title)
  2. [Description](#description)
  3. [Installation](#installation)
  4. [Usage](#usage)
  5. [Technologies](#technologies)
  6. [License](#license)
  7. [Contributing](#contributing)
  8. [Tests](#tests)
  9. [Credits](#credits)
  10. [Author](#author)
  11. [Questions](#questions)
  
  ---
  ## Installation
  * Clone my repository on GitHub.

  * On Visual Studio Code:
      * Open the cloned file. 
      * Create your  `.gitignore` file.
      * Check the dependencies and dev dependencies needed on `package.json`. 
  
  * To set up all the existing npm packages, run `npm init`.

  * To install the dependencies on the `node_modules` folder, run `npm install` or

      * `npm i express` to install Express.js;
      * `npm i mongoose` to install Mongoose; and 
      * `npm i nodemon` to install Nodemon.

  * Ensure that MongoDB is installed on your machine. 
      * Otherwise, follow the instructions on the [MongoDB website](https://www.mongodb.com/docs/manual/installation/).
      
      * *Note: If you're a Mac user and you're using an older version of Mac, you may need to install MongoDB via Homebrew. There are a number of tutorials on YouTube, but the video that helped me troubleshoot my installation, after trying everything else, was [this](https://www.youtube.com/watch?v=4crXgQZG4W8&t=40s).* 

      * *Prior to installation, you might also need to ensure that you have the current Node.js version (at least Version 17.0).*

  * To invoke the application, run `npm start`.

      * When the server is started, the Mongoose models are synched to the MongoDB database.
      
      * Open MongoDB and connect to the MongoDB URI `mongodb://localhost:27017`. On the list of databases, click on `socialmedia` to see `thoughts` and `users` data. 

  * To create seed data and test the API routes, open Insomnia. Also, see Test below.
  ---
  ## Usage
A user can utilize this API to create a new user with a valid username and email, add other users as friends, post "thoughts" as well as "reactions" to thoughts, update and delete thoughts and reactions, and delete friends.
  ### Features and Functionalities

  1. This is a social network API that uses MongoDB, a NoSQL database, which allows the website to handle large amounts of unstructured data.

  2. When the command to invoke the application is entered, the Mongoose models are synced to the MongoDB database.

  3. When the API GET routes for users and thoughts are opened in Insomnia, the data for each of the routes is displayed in formatted JSON.

  4. When the API POST, PUT, and DELETE routes are tested in Insomnia, the user can successfully create, update, and delete users and thoughts in the user's database.

  5. When the API POST and DELETE routes are tested in Insomnia, the user can sucessfully create and delete reactions to thoughts, and add and remove friends to a user's friend list.

### Objects and API Routes
 📁 **USER**
  * Create a new user:  `POST /api/users`
  * Get all users: `GET /api/users`
  * Get a single user by its `id`: `GET /api/user:userId`
  * Update a user by its `id`: `PUT /api/user:userId`
  * Delete a user by its `id`: `DEL /api/user:userId`

 📁 **FRIEND**
  * Add a new friend to a user's friend list: `POST /api/users/:userid/friends/:friendId`
  * Delete a friend from a user's friend list: `DEL /api/users/:userid/friends/:friendId`

📁 **THOUGHT**
  * Create a new thought: `POST /api/thoughts/`
  * Get all thoughts: `GET /api/thoughts/`
  * Get a single thought by its `id`: `GET /api/thoughts/:thoughtId`
  * Update a thought by its `id`: `PUT /api/thoughts/:thoughtId`
  * Delete a thought by its `id`: `DEL /api/thoughts/:thoughtId`

📁 **REACTION**
  * Create a reaction: `POST /api/thoughts/:thoughtId/reactions`
  * Delete a reaction by the `reactionId`: `DEL /api/thoughts/:thoughtId/reactions/:reactionId`

--- 
 ## Technologies
  * JavaScript
  * Node.js
  * Express.js
  * MongoDB
  * Mongoose
  * Insomnia

  ---
  ## License
  License used for this project - MIT
  
  For more information on the above license, please see the following websites:  
  - [Open Source Initiative](https://opensource.org/licenses)
  - [Choose a License](https://choosealicense.com/)

  ---
  ## Contributing
  To contribute to this application: 
  Please email the author for guidelines.

  ---
  ## Tests
  Insomnia is used to test RESTful API calls.

  Please see the demonstration video, as well as the sections on Usage, Features and Functionalities, and objects and API Routes.
  
  ---
  ## Credits
  The following applications and resources were consulted and/or utilized in the development of this application:
  
  * UCI Boot Camp study materials and internet resources.
  * [MongoDB Documentation](https://www.mongodb.com/docs/manual/reference/connection-string/)
  * [Insomnia](https://insomnia.rest/)
  * [How to Install MongoDB on Mac by MammothInteractive](https://www.youtube.com/watch?v=4crXgQZG4W8&t=40s)

  ---
  ## Author
  Jane Tiglao

  ---
  ## Questions
  For questions or issues, please contact: 
  - Jane Tiglao 
  - Email: janeytiglao@gmail.com
  - GitHub Username: jbtiglao
  - GitHub Profile: https://github.com/jbtiglao


