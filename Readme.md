
# Bootcamp 3 - Introduction to Frontend Development with React

In this assignment, we will continue to build upon our directory application by creating a frontend interface with React.js to display listings, as well as the ability to add new listings and delete old ones.

This readme file contains an outline and overview of the technologies and concepts we will be using for this project, as well as your assignment instructions. We highly suggest reading through and exploring the external resources linked to fill in any gaps in your knowledge.

## Table of Contents

1. 🙈 [Frontend Introduction](docs/introduction.md)
2. 🎨 [Styling](docs/styling.md)
3. 🏛️ [Architecture](docs/architecture.md)
4. 🔍 [React Basics](docs/react-basics.md)
5. 📝 [Assignment](#assignment-overview)
   1. [Starter Application](#starter-application)
   2. [Development Goals - To Do List](#development-goals---to-do-list)
   3. [Setup](#setup)
   4. [Debugging Tips](#debugging-tips)

## Assignment Overview

For this assignment you will be building upon our UF directory application by creating a frontend interface with React.js to display listings, search/filter, as well as the ability to add new listings and delete old ones. Note: We won't connect the frontend to the back-end in this assignment, we will leave that for Bootcamp #5.

### Starter Application

*After using the [**create-vite**](https://vitejs.dev/guide/#scaffolding-your-first-vite-project) tool with the React template, you can replace the src file in the starter application with the src file from the Bootcamp #4 assignment repo*. You'll then see the following files in your project directory:

- *src/data/data.js* - A list of buildings formatted to work with React and JSX to render the contents to the browser
- *src/App.css* - An empty file that we aren't using for this project but do not delete it as it will affect the functioning of your program
- *src/App.jsx* - This is the main application we are developing. The majority of our development will be in this file.
  - It prints out the directory listings
  - It has a text box for searching/filtering the results
  - It has a display box for printing out more details about the selected building
  - It imports and uses several React Component files to implement this functionality
- *src/index.css* - A starter CSS template for you to use for this project
- *src/main.jsx* - This file is used in creating the application file that you will be manipulating through the App.jsx file. This is where we have injected the data.js file and the building data that we pass around for the entire application.
- React Component Files - *React uses components to organize and squirrel away functionality so that we can reuse it in multiple places. Ultimately, it allows our code to look cleaner and maximizes reusability for future development.*
  - *src/components/BuildingList.jsx* - This is a React Component that prints the building code and the name to the screen
  - *src/components/Credit.jsx* - This is a React Component that displays the credits for the building data
  - *src/components/Search.jsx*  - This is a React Component that filters the contents of the list based on the user's input in the text box
  - *src/components/ViewBuilding.jsx* - This is a React Component that allows us to view additional listing details for the current selected building when a user clicks on a listing

### Development Goals - To Do List

In this assignment, we are only focused on creating your frontend user interface to filter and display listings, as well as add new listings or delete existing listings.

As you develop the solution to this assignment you will need to complete at least the following tasks.  

- App.jsx - Main Application
  - Create the filterUpdate() function - to set the state of filter
  - Create the selectUpdate() function - to set the state of selected building

- BuildingList.jsx: *In this file you will*
  - Create a filter on the building list constant that allows you to filter on the name of the building
  - Display only the buildings the meet the filter criteria
  - Create an onClick listener action that will allow you to click on a building name and capture the ID

- Search.jsx: *In this file you will*
  - Capture the text that is typed into the text box and store this value using the filterUpdate() function
  - Use the onChange listener function
  - Note: You will need to understand how to use ref values from form inputs

- ViewBuilding.jsx:
  - Capture building ID to look up the additional information for the building
  - Return additional details of the building to be rendered on the screen for the user

- Create two new components in the components folder that allow you to add and remove elements from the list.
  - AddBuilding.jsx - Add a building to the listings
  - RemoveBuilding.jsx - remove a building from the listings

- index.css - Style the User Interface of this app using CSS and Bootstrap 4 to make this app look professional and user-friendly, e.g.
  - style the listings
  - add icons for search, add, and delete
  - search bar
  - buttons
  - card for viewing the selected listing (ViewBuilding.jsx)

### Setup

*Note: This is a big assignment, start early and work on getting simple things working first. 

1. Install Bootstrap 5, [there are 3  ways](https://getbootstrap.com/docs/5.3/getting-started/download/):
   1. npm install bootstrap (or yarn add bootstrap) - *Recommended*
      - Install Bootstrap in your Node.js powered apps with [the npm package](https://www.npmjs.com/package/bootstrap):
        - `npm install bootstrap@5.3.2`
      - Install Bootstrap in your Node.js powered apps with [the yarn package](https://classic.yarnpkg.com/en/package/bootstrap):
        - `yarn add bootstrap@5.3.2`
      
   2. CDN via jsDelivr
       - simply add the link in head tag and script before closing body tag
       - see [here](https://getbootstrap.com/docs/5.3/getting-started/download/#alternative-cdns) for alternative CDNs

   3. download - **great for project** not recommended for Bootcamp #4 project

2. Use the [**create-vite**](https://vitejs.dev/guide/#scaffolding-your-first-vite-project) tool with the React template to help you get started with a scaffold for your first React project.
   - Run one of the following commands in terminal to create a starter application my-app (note: you can change this to bootcamp4 if you like.)
   - `npm create vite@latest my-app --template react`
   - `yarn create vite my-app --template react`
   - `pnpm create vite my-app --template react`

3. After it is installed, you should be able to cd into the project directory with `cd my-app`.

4. Inside the newly created project, you can run some built-in commands:
   1. `npm install` or `yarn install` to install the dependencies.
   2. `npm start` or `yarn start` to run the app in development mode.

5. It should auto-open http://localhost:5173 (because 5173 is [leetspeak](https://en.wikipedia.org/wiki/Leet#:~:text=Leet%20(or%20%221337%22),via%20reflection%20or%20other%20resemblance.) for vite) in the browser after it starts up a server for you. If a browser doesn't open up, copy and paste the link into your web browser with a starter page.

6. After this you should open the folder and replace the `src` file with the `src` file from this Bootcamp #4 github repo. You should then be able to see a listing of the building codes and buildings, search/filter text box and space to output details about your project.

7. Use the given starter code to create a frontend interface with React.js to display listings, as well as the ability to add new listings and delete old ones.

**See Development Goals** above for specific implementation details for this project.

### Debugging Tips

1. Use console.log statements in your render functions to print to the browser console to debug your program and to ensure you are passing the data around that you expected. This will help tremendously when you have errors that you can't figure out.

2. Use [**React Developer Tools**](https://react.dev/learn/react-developer-tools) - Download the React Developer Tools Chrome Plug-in, it is specifically designed to help you debug React applications.

### Submission: See Canvas for Submission Instructions
