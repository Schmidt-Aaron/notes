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

There is a weird gap between the rows right now. Padding and margin are both at 0... Starting to get the hang of props and state.