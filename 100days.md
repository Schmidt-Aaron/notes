# 100days of code

## Day 1 1/6/18

(~2hrs)

### Front End Masters VS Code by Mike North

(1.5hrs)
tips: ctrl + D to select multiple instances of highlighted word

* Markdown refresher
** Detail/summary is pretty cool
<details>
  <summary>This is a cool Markdown feature</summary>

  ```
  const bird = 'the word';
  ```
</details>

*Emmet refresher

peek editor and find all references (F2) neat!

### Game of life with React
(.5hrs)
game on...
installed create-react-app then got bored?

## R1D2 1/7/18

### Front End Masters VS Code by Mike North
Typechecking
React propTypes(runtime)
Facebook flow(static)
Microsoft TypeScript(static)

to enable type checking in regular js 
// @ts-check at first line

this will lock in the types on the first assignment for the variable. You can also explicitly assign the type.

```
/** new document.js file */
// @ts-check

let x = 15;

x=21;
x='156'; // shows an error bc the variable was previously assigned a number

/** @type {number} */
let value;

value = 21;
value = '21'; //shows an error becuase the type was declared above
```

You can assign the type to be pretty much anything; object, array, function, specific element...

Here the type is an hmtl element
```
/** @type {Element} */
let x = document.querySelector('.passwordField');
```

Or you can be more specific
```
/** @type {HTMLInputElement} */
let x = document.querySelector('.passwordField');
// 🛑 Type 'Element' is not assignable to type 'HTMLInputElement'
// 🛑 Property 'accept' is missing in type 'Element'.
```

example of explicit type casting.
```
/** @type {HTMLInputElement} */
let x = /** @type {HTMLInputElement} */(
  document.querySelector('passwordField')
);
```
this will force the system to see the variable as the declared type. In the exampe above, x will now be accepted as an input element.

### R1D3 1/8/18

CSS animations and page location triggers
codepen:https://codepen.io/aaronms/pen/MrrPpE?editors=0110

### R1D4 1/9/18

Started on my game of life project. Used create-react-app to bootstrap it. 

*Sources*

1. https://www.youtube.com/watch?v=PM0_Er3SvFQ
1. https://codepen.io/rambutan/pen/ONOaaZ?editors=0010

### D5 1/10/18

Listened to syntax.fm about GraphQL. 
Looked over some react game of life code - still don't have a great handle on how to build. Will propably come when I actually start coding it. 
Watched a couple videos on CSS animation.

### D6 1/11/18

Worked on my game of life. I got a grid to display by creating a 2D array and pushing a box class into each spot. 

There is a weird gap between the rows right now. Padding and margin are both at 0... hmm fixed that by setting the line-height and font-size to 0 on the parent element.

Next issue is how to activate cells ie toggle state. MY first idea was to play with toggling the class. This seems to be more difficult that it should be. Should reeval approach.

Starting to get the hang of props and state.

### D7 1/12/18

Watched coding train video on game of life. Will change my approach a little.

1. create array function
1. render array
1. add lifecycle => new array
1. render new array

### D8 1/13/18

rest day. Thinking about order of operations with react + canvas. 

### D9 1/14/18

not productive

### D10 1/15/18

Worked on GOF project. refactored existing code and added logic to compute lifecycle. SLOWWWW

### D11 1/16/18

Got program to work... computer runs out of memory though. So that isn't ideal. Will have to refactor. Maybe ditch canvas and go back to a more DOM centric approach.

### D12 1/17/18

Looked at WP docs - updated all sites. 
Will add more animations to work site.
refactor GOF to remove canvas - good example: https://codepen.io/chemok78/pen/aBgRGm?editors=0010

### D13 1/18/18

ARticles to look into further:
1. https://medium.mybridge.co/learn-react-js-from-top-45-tutorials-for-the-past-year-v-2018-28b7f4d4b2c4
1. https://medium.com/@strapi/building-a-static-blog-using-gatsby-and-strapi-8b5acfc82ad8
1. https://hackernoon.com/migrating-your-node-js-rest-api-to-serverless-d2a170e0856c 