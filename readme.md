# Fetching Stuff

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Instructions](#instructions)
  - [Setting up Server](#setting-up-server)
  - [Creating a Database](#creating-a-database)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- Search pokemon from API

### Screenshot

![](./screen.JPG)

### Links

<!-- - Live Site URL: [View](https://camkol.github.io/DragonRepeller/) -->

## My process

### Built with

- Semantic HTML5 markup

- Mobile-first workflow
- Mobile-Responsive Design
- JavaScript - Scripting language

### What I learned

How to ask for data from a API.

### Continued development

## Instructions

```javascript
// Define an asynchronous function named fetchData
async function fetchData() {
  try {
    // Get the value of the input element with id "pokemonName" and convert it to lowercase
    const pokemonName = document
      .getElementById("pokemonName")
      .value.toLowerCase();

    // Fetch data from the Pokémon API for the specified Pokémon name
    const response = await fetch(
      `https://pokeapi.co/api/v2/pokemon/${pokemonName}`
    );

    // Check if the response is not ok (status is not in the range 200-299)
    if (!response.ok) {
      // If the response is not ok, throw an error with a specific message
      throw new Error("Could not fetch resource");
    }

    // Parse the JSON data from the response
    const data = await response.json();

    // Log the data to the console for debugging purposes
    console.log(data);

    // Get the URL of the Pokémon's front sprite from the data
    const pokemonSprite = data.sprites.front_default;

    // Get the image element with id "pokemonSprite"
    const imgElement = document.getElementById("pokemonSprite");

    // Set the src attribute of the image element to the URL of the Pokémon's sprite
    imgElement.src = pokemonSprite;

    // Display the image element by setting its display style to "block"
    imgElement.style.display = "block";
  } catch (error) {
    // If an error occurs, log the error to the console
    console.error(error);
  }
}
```

### 1. Asynchronous Function Definition:

- `async function fetchData()` defines an asynchronous function named `fetchData`.

### 2. Try-Catch Block:

- The `try` block contains the code that might throw an error.
- The `catch` block handles any errors that occur in the `try` block.

### 3. Getting the Pokémon Name:

- `document.getElementById("pokemonName").value.toLowerCase();` retrieves the value from an input element with the `id` `pokemonName`, converts it to lowercase, and stores it in the `pokemonName` variable.

### 4. Fetching Data from the API:

- `await fetch(`https://pokeapi.co/api/v2/pokemon/${pokemonName}`);` sends a request to the Pokémon API using the Pokémon name entered by the user.
- `await` pauses the execution of the function until the `fetch` call completes.

### 5. Handling the Response:

- `if (!response.ok) { throw new Error("Could not fetch resource"); }` checks if the response status is not OK (i.e., not in the range 200-299). If it's not OK, an error is thrown.

### 6. Parsing JSON Data:

- `const data = await response.json();` parses the JSON data from the response and stores it in the `data` variable.

### 7. Logging the Data:

- `console.log(data);` logs the data to the console for debugging purposes.

### 8. Getting and Displaying the Pokémon Sprite:

- `const pokemonSprite = data.sprites.front_default;` retrieves the URL of the Pokémon's front sprite from the `data`.
- `const imgElement = document.getElementById("pokemonSprite");` gets the image element with the `id` `pokemonSprite`.
- `imgElement.src = pokemonSprite;` sets the src attribute of the image element to the URL of the Pokémon's sprite.
- `imgElement.style.display = "block";` sets the display style of the image element to "block", making it visible.

### 9. Error Handling:

- `catch (error) { console.error(error); }` catches any errors that occur in the try block and logs them to the console.

## Author

- Website - [Cameron Howze](https://camkol.github.io/)
- Frontend Mentor - [@camkol](https://www.frontendmentor.io/profile/camkol)
- GitHub- [@camkol](https://github.com/camkol)
- LinkedIn - [@cameron-howze](https://www.linkedin.com/in/cameron-howze-28a646109/)
- E-Mail - [cameronhowze4@outlook.com](mailto:cameronhowze4@outlook.com)

```

```
