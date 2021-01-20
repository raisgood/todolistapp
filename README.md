Name: Rashad Humphrey

Overview/description of the project:

This is a ReactJS 

"To Do List" with add and clear button.

Details: This is used to mark your schedule.

Technologies Used: HTML, CSS, JavaScript and ReactJS.

Ideas for future improvements: 

1) Add additional JavaScript to the site. 

2) Implement multiple pages together.

3) Add a time feature to the page.

State and Component Planning:

Project 3 State Tree:

Link:https://repl.it/@RashadHumphrey1/Project-3-State-tree

(Code):

const todo = [
{ name: "Name1", symbol: "Gym"},
{ name: "Name2", symbol: "Shop"},
{ name: "Name3", symbol: "Study"},
{ name: "Name4", symbol: "Sleep"}
];

function listMenu([
  {name: name1, symbol: symbol1},
  {name: name2, symbol: symbol2},
  {name: name3, symbol: symbol3},
  {name: name4, symbol: symbol4}
]) {
  //if symbol1 and symbol2 are the same, then return "Booked!"
  if(symbol1 == symbol2) {
      return "Booked!";
  }
     
  //if symbol1: "Gym" and symbol2: "Shop": return P1
  //if symbol1: "Stop" and symbol2: "Study": return P1
  //if symbol1: "Study" and symbol2: "Sleep": return P1
  const menuList = ['Gym=Shop', 'Shop=Study', 'Study=Sleep'].includes('${symbol1}>${symbol2}');

// Both solutions work, you can use TodoList or MenuList interchangibly
const todoList = 
(symbol1 === "Guy" && symbol2 === "Shop") ||
(symbol1 === "Shop" && symbol2 === "Study") ||
(symbol1 === "Study" && symbol2 === "Sleep");

  if (menuList) {
    return '${name1} Booked!';
  }

   //P2 wins (return P2)
      return '${name2} Booked!';
}

console.log(listMenu(todo));

List of Actions:

import { ADD_TABLE_ITEM } from "../constants/constants.js";

const addTableItem = (name, price, id) => {
  return {

    type: ADD_TABLE_ITEM,
    tableId: id,
    item: {
      name: name,
      price: price
    }
  };
};

export default addTableItem;

List of Container and Presentational Components:

Container-
 <div class="w3-container w3-teal">
  <h1>Header</h1>
</div>

Presentational Components- 
Todo.jsx
App.js


# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
