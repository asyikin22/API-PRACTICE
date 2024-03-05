# JOKE-GENERATOR

**OBJECTIVE**: <br>
* These codes demonstrate how we can use fech function to get data from API and display it on the webpage.
* We learn how to add a button and attach event lister to it in JS so that when user clicks, it will display a new joke.
* We learn how to create a simple animation in css where the joke text will fade in and out with each click of the button.

**SOURCE**: https://sv443.net/jokeapi/v2/

**HTML**
* Create one div with class=wrapper
* Inisde it, create p element with id=joke. This is where the text of the joke will be displayed
* Create one div button with id=btn

**CSS**
* You can style it however you like, i chose to center the whole thing on teh webpage.
* To create an animation effect where the joke fades in and out with every click of button, add 'opacity' proeprty to 'p' element
* Create a '.fade' class with property 'opacity' and 'transition'. Bear in mind that this will be used in JS code for animation effect.

**JAVASCRIPT**

**How to fetch data from API and how it will look on our console:**
* Create 3 variables for joke container, button and url
* Create a function to fetch data from API named getJoke

**Now we are going to fetch specific data object which is 'joke' (Nothing appears yet on webpage at this stage)**:
* On the second promise function, we log hte value of 'joke' property of 'item' object.
* On our console, we will see a single joke. Other irrelevant data that we dont want no longer appear on console.
* At this point nothing appears on the webpage yet 

**We are going to tweak the second promise chain and display jokes inisde the jokeContainer on our webpage**:
* To display the joke, we have to set 'textContent' property of the 'jokeContainer' element to the value of joke retrieved from the response.
* Value of the joke is: ${item.joke}
* We are using template literal to embed expressions directly inside the string.
* Inside template literal, we include the value of joke,  ${item.joke}, so it will retrieve value from joke property from item object and includes it within string.
* Note that the joke is now displayed on our webpage when the code runs.

**Add event lsitener to button element so new joke will be displayed everytime button is clicked**:
* When button is clicked, getJoke function will be called

**And the final step, we will add animation function where the text of the joke in jokeContainer will fade in and fade out when button is clicked**:
* This will trigger CSS transition effect in the 'fade' class we created in CSS file earlier. 

