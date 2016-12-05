# css-pseudoselectors-lesson
Educational exercise for CSS pseudoselectors, transitions and animation

###Explanation
You have already learned about CSS selectors--the way you select an element on the page to change its styles. CSS has the ability to use pseudo-selectors as well. "Pseudo" means "kind of, but not really"--these pseudoselectors are kind of, but not really, selectors. This means they can change the styles of an element, but they have to have a real selector helping them, and they can only change those elements when certain things happen on the page. Because of this, they can help you make a page respond to the user's actions. You can even use them for animating elements!

####CSS Pseudoselectors
Pseudoselectors must be attached to the selector of the element you wish to use them on. You do this with a `:`.

The most common pseudoselectors are `:visited`, `:hover`, and `:active`.
-`:visited` is used for links. You have probably seen this one before. All browsers include a built-in default style for links: they are underlined and blue when first viewed, and when they are clicked, they turn purple. Most sites override this default with their own style, but you can still see it on sites like Wikipedia.
-`:hover` can be used on almost any element. This pseudoselector lets you change the style of an element whenever the mouse is on top of it. The styles go back to how they were before when the mouse is moved away from the element.
-`:active` is used for elements that allow user interaction, like buttons and text input boxes. Browsers usually have defaults for these, too: when you click a button, its style changes so it looks like it's pressed in. When you click a text input box, some browsers apply a blue border around it to show which one you're typing in.

#####Example

```
button {
  background-color: purple;
}

button:active {
  background-color: red;
}
```

When you click any button on the page you used this CSS on, those buttons will turn red when clicked.

####CSS Transitions
CSS transitions are commonly used with pseudoselectors. A transition is a smooth change between one state and another. CSS knows how to do this automatically, but it needs to know a few things in order to make it happen.

#####Example
```
button {
  background-color: purple;
}

button:active {
  background-color: red;
  transition: background-color 0.5s;
}
```

#####Explanation
A CSS transition is created by the `transition` property. At its most basic, it needs to know which property to change, and how long the change should take. In this example, the button will slowly turn red over half a second when it is clicked.

You can change more than one property with one `transition`. Just separate each one with a comma, like so:
```
div:hover {
  background-color: blue;
  font-size: 18px;
  transition: background-color 0.5s, font-size 0.5s;
}
```

###Exercise Instructions

#####HTML file
Create an index.html with three objects:
-One div that has an id and some text in it.
-A link to another page (yours or someone else's) inside that div.
-One button that has an id and says "click me".
-A wrapper div with the id "main" that has these two elements placed inside it.

#####CSS file
Create a CSS file that uses the following:
-A rule that changes the text color of a link you've already visited. Make it a color that is not the default purple.
-A rule that adds a width and a background color to your div with the id.
-A rule that changes one or more of those properties when you hover over the div.
-A rule that changes something about your button when your button is clicked.
-A rule or rules that make those properties change smoothly rather than instantly.

####Bonus round
-Add an onclick to your button that changes the background color of the "main" div. Make sure it changes smoothly!
-Add an onclick to your button that plays a sound.
-Add both for MAXIMUM COOL!
-Research what other properties work with CSS transitions and add some to your div.