# Questions

**With a partner**, answer these questions as completely as possible. Feel free to look at past lecture notes, the web, anything. 

Take the time to explain it to each other. 

The power of this exercise is in the act of _formulating_ and _explaining_ the concepts to someone else (your teammate).

## One

Run the app. Write out the steps, the _pseudo code_, required to create this app. It doesn't have to be totally accurate, or in the right order.

Only move on to the next question when you have enough detail that you would be able to start coding it yourself.

```
create html file 
add head, body, footer 
add form that stores info variable 
takes that info and adds to list 


```

## Two - `server.js`

Take a look at the `server.js` file.

We have a new module in there, `body-parser` that is required on line `4`. What is it for? What is its use-case? What other lines are related to this module?

_The NPM site might be a good place to start. Feel free to provide links as relevant._

```
It acts as a middleman to validate the source of the request.
In the code for the app it distinguises the difference between html requests and json requests. 
The other lines related to this module are lines 17 - 30 in the handlers.js and line 18 in server.js

```

## Three - `server.js`

Look at lines `23` and `24`. Explain the methods used. How are they different? What are the usecases for each?

```
Line 23 calls the handleHomePage function which renders the homepage for the ToDo list 
Line 24 calls the handleFormData function which posts the input data on a list on the homepage 
Line 23 is executed when there is a request 
Line 24 is executed when you click on submit
```

## Four - `server.js`

Line `6`. That's new. What do you think it's for?

```
Line 6 imports the functions {handleHomepage, handleFormData, handle404} from handlers.js file into server.js

```

## Five - `handlers.js`

Explain line `1`. Where, why and how is `items` being used?

```
items is being delcared as an empty array which contains the variables input through the handleFormData function. items is then used to push the input onto the homepage.  

```

## Six - `handlers.js`

Why is there `redirect` on line `11`;

```
The redirect on line 11 exists to add the new item into the ToDo list 
by refreshing the page. 

``` 

## Seven - `handlers.js`

The `handle404` function is a more complex than we've seen thus far, what is the extra functionality for?

```
The extra functionalities denoted in the other if functions and res.type deteremine what response to send back based on the type of request recieved. The handle404 function determines whether to send an html 404 page back to broweser requests and an error message to Node, server users and all other remianing request types.  

```

## Eight - `ejs`

Take a look at `homepage.ejs` and `todoInput.ejs`. What is happening in there? Explain line-by-line...

```
Line 1 on homepage.ejs adds the header to the homepage
Line 2 creates a div which adds the 
Line 3 adds the todoInput.ejs which adds the input form 
Line 4 closes div
Line 5 creates a div containing a class 
Line 6 creates an unordered list with a class named 'todo-list' 
Lines 7,8,9 creates a forEach loop that takes each element in items and 
makes a new item in the list for it
Line 10 closes unordered list
Line 11 closes div 
Line 12 renders the footer to the homepage  

```

## Nine - `styles.scss`

What are lines `2` to `7` for this file? Where are these values being used? Take a look at `_homepage.scss` as well? What do you notice?

```
Lines 2 - 7 are variables that contain styling data so that they can be referred to in the _homepage.scss file. These values are used in _homepage.scss to display border-color values, content width and input height which were defined in styles.scss. 

```

## Ten - `_homepage.scss`

Line `16`. See if by searching the Sass documentation, you can determine what _exactly_ is going on here. That `#{}` notation very specific to this use-case. Why?

```
It allows the variable inside the curly brackets to converted into a numerical value. It is necessary because css is not able to to these types of actions. 

```







