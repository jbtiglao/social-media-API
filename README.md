# Social Media API 👥

Unit 18, NoSQL Assignment 

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

  ---
  ## Description 📌

This is an API for a social network web application where users can share their thoughts, react to friends' thoughts, and create a friend list. It uses Express.js for routing, a MongoDB database, the Mongoose ODM, and native JavaScript Date object to format timestamps. The seed data is created using Insomnia.  


<img width="1380" alt="image1_social-media-api-insomnia" src="https://user-images.githubusercontent.com/94569484/167376248-b824a670-d62a-49bc-b1f1-b6d3c8836e5c.png">


To see how the API works using Insomnia, see the **walk through demonstration videos** here:

* [User Routes](https://drive.google.com/file/d/1vATUYGYqmK8ixaTrdq78J7NV95eTX112/view)
* [Friend Routes](https://drive.google.com/file/d/1dgRadPEfgyq9ELoz-bKzoqlW6SU-Q1bd/view)
* [Thought Routes](https://drive.google.com/file/d/1bSaxRDOr6DB3RVDTEBH2RXNu-fdMkEJ2/view)
* [Reaction Routes](https://drive.google.com/file/d/10Pfe7YwvYndorHrBQNautqRnRgqSQzhM/view)

The application **files** can be accessed on my [GitHub Repository](https://github.com/jbtiglao/social-media-API).

  ---
  ## Table of Contents 📌
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
  ## Installation 📌
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

      * *Prior to installation, you might also need to ensure that you have the current Node.js version (at least Version 17.0).**

      * To invoke the application, run `npm start`.

      * When the server is started, the Mongoose models are synched to the MongoDB database.
      
      * Open MongoDB and connect to the MongoDB URI `mongodb://localhost:27017`. On the list of databases, click on `socialmedia` to see `thoughts` and `users` data. 

<img width="1358" alt="image2_mongodb-connect" src="https://user-images.githubusercontent.com/94569484/167376510-257e4b41-eefa-4e62-afea-6180f395c08d.png">


  * To create seed data and test the API routes, open Insomnia. Also, see the Tests section below.
  
  ---
  ## Usage 📌
A user can utilize this API to create a new user with a valid username and email, add other users as friends, post "thoughts" as well as "reactions" to thoughts, update and delete thoughts and reactions, and delete friends.

### Features and Functionalities  🔌

  1. This is a social network API that uses MongoDB, a NoSQL database, which allows the website to handle large amounts of unstructured data.

  2. When the command to invoke the application is entered, the Mongoose models are synced to the MongoDB database.
  

<img width="1384" alt="image3_mongodb-database" src="https://user-images.githubusercontent.com/94569484/167377164-9904befa-c198-4230-9f0b-d228d28682f8.png">


  3. When API GET routes for users and thoughts are opened in Insomnia, the data for each of the routes is displayed in formatted JSON.

  4. **User**, **Friend**, **Thought**, and **Reaction** routes are created to create the database and test the API on Insomnia.

<img width="243" alt="image4_routes" src="https://user-images.githubusercontent.com/94569484/167378910-d15f2882-3858-489d-9ccc-2dc3145f009d.png">

  5. **User Routes** - a user can create a user with a username and valid email address. When created, the user is assigned a unique user ID. 

  * To create a user, click the `POST` request and enter the user's username and email address. Click Send.

<img width="1390" alt="image5_create-user" src="https://user-images.githubusercontent.com/94569484/167379026-7b30c0dd-2f05-4e5f-a3e8-704f916e6305.png">


  * There are two `GET` requests that return user information. To return all users, click the `GET All Users` request, then click on Send. To return a single user, click the `GET a User by Id` request. On the URL, enter the user's ID. 
          

<img width="1389" alt="image7_get-single-user-id" src="https://user-images.githubusercontent.com/94569484/167388751-ba7220b2-b3dc-48fc-80fd-b0e73ff44003.png">

         
  * To update a user by ID, click the `PUT` request. On the URL, enter the ID of the user whose information is going to be updated.
      

<img width="1385" alt="image8_update-user" src="https://user-images.githubusercontent.com/94569484/167388789-2dff6a1c-93df-44a5-961b-f211cb5052c6.png">


  * To delete a user by ID, click the `DEL` request and enter the user's ID. 
      
  * A message that reads, `"User and associated thoughts deleted!"` will appear if the user has been deleted from the database. If there is no such user or user ID in the system, the message, `"No user with this id!"` is shown.
      
  <img width="1387" alt="image9_delete-user" src="https://user-images.githubusercontent.com/94569484/167388824-b13b966e-b833-46cc-a18f-8b4853e24482.png">

  * Click `GET All Users` to see if the user has been deleted. 

  6. **Friend Routes** - a user can add a friend and delete a friend.

  * To add a friend, click the `POST` request. On the URL enter the user ID of the user who is adding a friend, then the user ID of the friend the user is adding. *(Note: Please see the section on Tests for the API routes.)*

<img width="1385" alt="image11_add-friend" src="https://user-images.githubusercontent.com/94569484/167388920-8c9cff8b-e646-4d67-88e8-13c11d5b567a.png">


  * To see the user's friends, click `GET All Users`. The ID of the friends the user added are listed under `"friends"`. The `"friendCount"` indicates the number of friends the user added.

  * To remove or delete a friend, click the `DEL` request. On the URL, enter the friend's ID. 
      
<img width="1385" alt="image12_delete-friend" src="https://user-images.githubusercontent.com/94569484/167388958-30af7391-e9b0-4f9c-a2be-b54fe8f9b803.png">

  * To check if the friend has been removed from the user's friend list, click `GET All Users`.

  7. **Thought Routes** - a user can create a thought, get all thoughts or a single thought by ID, update a thought by ID, and delete a thought by ID.

  * To create or add a thought, click the `POST` request. Enter the `"thoughtText"`, `"username"`, `"userID"` of the user creating the thought.

  * To get all thoughts, click the `GET All Thoughts` request. All the thoughts that were created will appear, as well as the date and time they were created. Each created thought is assigned a unique thought ID. Click `GET All Users` to access the thought ID. 

  * To get a thought by ID, click the `GET a Thought by Id` request and enter the thought ID.

  * To update a thought, click the `PUT` request. On the URL, enter the thought ID. Enter the necessary changes on the text body. To see the changes, click `GET All Thoughts`. 

<img width="1367" alt="image15_update-thought" src="https://user-images.githubusercontent.com/94569484/167389182-0abd3b7b-4f38-4d43-b122-775d0ae1bb8b.png">

* To delete a thought by ID, click the `DEL` request. On the URL, enter the thought ID that will be deleted.

* When the thought is successfully deleted, the text can no longer be found when you try to access it by clicking `GET All Thoughts.` The thought ID is also deleted when you click `GET All Users.`
      
* The following messages will appear upon creation, update, or deletion of a thought:

    - `"Thought successfully created!"` - if the thought is successfully created and associated with a user ID.
      
    - `"Thought successfully deleted!"` - if the thought is deleted from the database.
       
    - `"No thought with this ID!"` if there is no thought associated with the ID in the database.
       
    - `"Thought created but no user with this id!"` - if a thought is created but no user ID is associated with it.

8. **Reaction Routes** - a user can create a reaction and delete a reaction.

  * To create a reaction, click the `POST` request. On the URL, enter the ID of the thought the user is reacting or commenting on. Then enter the `"reactionBody"` and `"username"` of the user creating the reaction.
      
<img width="1387" alt="image18_create-reaction" src="https://user-images.githubusercontent.com/94569484/167389494-7120c0dd-1ac0-4d62-adc7-6625c16e1f6a.png">

  * Click on `GET All Thoughts`to see the reaction, the username of the user who created the reaction, the reaction ID, date and time the reaction is created, and the user's reaction count. This request will also show if the reaction has been deleted from the user's list. 
      

<img width="1374" alt="image20_get-all-thoughts-reactions" src="https://user-images.githubusercontent.com/94569484/167389529-2fa7b9f0-730a-4c2f-9801-9d218ba630a1.png">


  * To delete a reaction, click the `DEL` request. On the URL, enter the ID of the thought the user created a reaction or commented on, then the reaction ID.  
      
  * The message, `"No thought with this id!"` will appear when a reaction is deleted or a reaction is not associated with a user ID. 
  
--- 
 ## Technologies 📌
  * JavaScript
  * Node.js
  * Express.js
  * MongoDB
  * Mongoose
  * Insomnia

  ---
  ## License 📌
  License used for this project - MIT
  
  For more information on the above license, please see the following websites:  
  - [Open Source Initiative](https://opensource.org/licenses)
  - [Choose a License](https://choosealicense.com/)

  ---
  ## Contributing 📌
  To contribute to this application: 
  Please email the author for guidelines.

  ---
  ## Tests 📌
  Insomnia is used to test REST API calls. Please see the walk-through demonstration videos as well as the sections on Description and Usage to see how data is added and tested using Insomnia. 

  When the API GET routes for users and thoughts are opened in Insomnia, the data for each of the routes is displayed in formatted JSON.

  4. When the API POST, PUT, and DELETE routes are tested in Insomnia, the user can successfully create, update, and delete users and thoughts in the user's database.

  5. When the API POST and DELETE routes are tested in Insomnia, the user can successfully create and delete reactions to thoughts, and add and remove friends to a user's friend list.
  
  The following API routes are created to add and test data:
 🔌 ### API Routes 
On Insomnia, the following API routes have been created and used to add, update, or remove users, friends, thoughts, and reactions in the user's database. 

 📁 **USER**
  * Create a new user:  `POST /api/users`
  * Get all users: `GET /api/users`
  * Get a single user by its `id`: `GET /api/users/:userId`

  * Update a user by its `id`: `PUT /api/users/:userId`

  * Delete a user by its `id`: `DEL /api/user/:userId`

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
  ## Credits 📌
  The following applications and resources were consulted and/or utilized in the development of this application:
  
  * UCI Boot Camp study materials and internet resources.
  * [MongoDB Documentation](https://www.mongodb.com/docs/manual/reference/connection-string/)
  * [Insomnia](https://insomnia.rest/)
  * [How to Install MongoDB on Mac by MammothInteractive](https://www.youtube.com/watch?v=4crXgQZG4W8&t=40s)

  ---
  ## Author 📌
  Jane Tiglao

  ---
  ## Questions 📌 
  For questions or issues, please contact: 
  - Jane Tiglao 
  - Email: janeytiglao@gmail.com
  - GitHub Username: jbtiglao
  - GitHub Profile: https://github.com/jbtiglao


