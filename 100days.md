# 100days of code 

Not necessaryly consecutive. If I miss a day I will subtract it from day total.

## D1 1/6/18

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

## D2 1/7/18

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

### D3 1/8/18

CSS animations and page location triggers
codepen:https://codepen.io/aaronms/pen/MrrPpE?editors=0110

### D4 1/9/18

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

### 1/14/18

not productive

### D8.2 1/15/18

Worked on GOF project. refactored existing code and added logic to compute lifecycle. SLOWWWW

### D9 1/16/18

Got program to work... computer runs out of memory though. So that isn't ideal. Will have to refactor. Maybe ditch canvas and go back to a more DOM centric approach.

### D10 1/17/18

Looked at WP docs - updated all sites. 
Will add more animations to work site.
refactor GOF to remove canvas - good example: https://codepen.io/chemok78/pen/aBgRGm?editors=0010
https://codepen.io/giveback007/pen/aybGVb?editors=0010

### D11 1/18/18

ARticles to look into further:
1. https://medium.mybridge.co/learn-react-js-from-top-45-tutorials-for-the-past-year-v-2018-28b7f4d4b2c4
1. https://medium.com/@strapi/building-a-static-blog-using-gatsby-and-strapi-8b5acfc82ad8
1. https://hackernoon.com/migrating-your-node-js-rest-api-to-serverless-d2a170e0856c 

### D12 1/19/18

Refactoring GOF - created a new branch to save the memory hogging code. Maybe revisit later - curious to how the program can eat up gigs of ram.

### D11 1/20/18 and D10 1/21/18

*crickets* -2 days

### D11 1/22/18

(2) codewars.com kata: interesting pattern using indexOf to generate numbers of a pattern - useful if numbers are sequential. Regex revisted. https://www.codewars.com/kata/5938f5b606c3033f4700015a

intersting article on implicit / explicit coercion: https://medium.freecodecamp.org/js-type-coercion-explained-27ba3d9a2839 

I should work on React later.

### D12 1/23/18

Worked on work website. Took several hours to run all necessary updates/scans and pull a fresh copy of the site down. Probably should have done them concurrantly. Added some animation to the home page - had issues with adding multiple animation with my bare bones script. Might have to go with a more robust custom script to deal with having custom animations. 

A couple animation /scroll libs
1. https://github.com/michalsnik/aos
  1. https://css-tricks.com/aos-css-driven-scroll-animation-library/
1. https://github.com/matthieua/WOW 

### D13 1/24/18

Work on work website some. 

FEM JS for Wordpress... https://github.com/zgordon/frontend-masters-jsforwp

wp_enqueue_script(
  'unique handle name',
  get_stylesheet_directory_uri() . '/path/to/file.js',
  ['dependency-handles'], //used for load order
  'version' //used for caching
  loadInFooter // true(default) or false
);


wp_localize_script(
  'js-handle', 
  'name_for_js',
  [
    'site_url' => esc_url( home_url() ),
    'site_name' => get_bloginfo('name')
  ]
);

add_action('wp_enqueue_scripts', 'my_enqueue_scripts');
  //add my script to the queue

can use any JS included in WP core..
conditionally enqueuing JS

*http://docs.chassis.io* - should look into this for WP dev

### D14 1/25/18

FEM JS for wp... a couple videos.
Eloquent JS ch3
not much done today :(

### D15 1/26/18

eloquent JS ch4 ex completed: all
eloquent JS ch5 ex completed: 1, 
FEM JS for wp- finished AJAX in WP section
TODO: [Scrimba](https://scrimba.com/g/gflexbox)) flexbox and CSS grid courses
 

 ### 1/27 + 1/28 
 
 *PDX Holiday* -2 days

 ### D14 1/29/18

 article to read more closely: https://medium.freecodecamp.org/the-authoritative-guide-to-blockchain-development-855ab65b58bc

Page speed stuff
 critcal css: https://www.sitelocity.com/critical-path-css-generator 
 https://criticalcss.com/
 WP plugin to try: https://wordpress.org/plugins/autoptimize/

 Thinking of rewriting work website with understrap theme to follow updated best practices + squeeze out more perf / faster load time. It could also be a good time to revamp my WP workflow... although the bang for my buck there might be pretty low. a more modular approach would be ideal though. 

 worked on react GoL - got grid set up, and generation logic done. Next step is to get the running logic working. I might have an error on my generation logic - should check it out. 

 FEM js for WP a couple vids: need to finish challenge 5 + 6

### D15 1/30/18

FEM JS for WP - finished accessing APIs inside Wordpress

### D16 1/31/18

finished JS for WP

### D17 2/1/18

Tired => no actual coding
1. Coding train videos
1. other youtube coding vids

### D18 2/2/18

1. Codewars kata (1)
1. github practice
1. started Colts Advanced

cool sites: 
1. [30 species](http://www.species-in-pieces.com/) 
  1. [Making of ^ ](https://www.smashingmagazine.com/2015/06/the-making-of-in-pieces/)
1. [waaark](https://waaark.com/)
1. [vscode stuff](http://vscodecandothat.com/)

### D19 2/3/18

1. youtube vids

### D19 2/4/18

nothing -1 day

### D20 2/5/18

1. codewars kata(1)
1. youtube vids
1. worked on game of life. A bit of a struggle to get the lifecycle thing figured out. The two main obstacles are how to get the incrementGeneration function to only be called after the previous call is done, and how to assign a clickhandler to change the state of the individual cells. 

### D21 2/6/18

Made decent progrss on game of life. Refactored with more components. I moved all the state into a game class and pulled the board, counter, and buttons into that class. [this post](https://forum.freecodecamp.org/t/nagging-little-questions-about-my-react-game-of-life-program/113482/2) as the linked GOL demonstrated how to pass functions down as props and how to pass this back up the chain. 
I finished up the toggle on click function. 
Something is still wrong with how I figure out neighbors though - I will have to look into that more.

### D22 2/7/18

debuggin my gol... :(
udemy vids

### D23 2/8/18

More debuggins...sigh
udemy vids

### D24 2/9/18

udemy vids

### D25 2/10/18

Node videos

### D26 2/11/18 
node videos

### D27 2/12/18

codewars kata(2)
udemy vids

### D28 2/13/18

codewars katas rank 6 => 5
udemy vids - animation practice: https://codepen.io/aaronms/pen/QQMONd?editors=1100 sunrise animation. used straight lines; would be cool to have an actual arc. tough to figure out though :(

### D29 2/14/18

udemy more animation practice.
https://codepen.io/pen/?editors=1100
udemy vids - flexbox

codewars 335 => 347

### D30 2/15/18

codewars 347 => 371

### D31 2/15/18

codewars 371 => 371 ?? no increase; did several algos

### D32 2/16/18

Codewars and???

### D31 2/19/18

codewars 386 => 392

### D32 2/20/18

Worked through flexbox section of Udemy course. Will practice by creating a responsive landing page. use their template as a starting point and create my own instead of following along.
[codepen](https://codepen.io/aaronms/pen/oEqOBd) about 40% done with sections, then need to fine tune the design a bit. 
 
codewars 392 => ...

### D33 2/21/18

Watched Udemy vids
codewars 392 => 407
I think I made [this one](https://www.codewars.com/kata/simple-frequency-sort/train/javascript) far more complicated then it needed to be. I should perhaps revisit and refactor at some point... maybe...
worked on udemy landing flexbox landing page.
started asyc section of udemy.

### D34 2/22/18

codewars 407 => 415
found a neat way to assign values to an array/string based on their place in the alphabet. Version 1 was my first answer, version 2 was the new way.

Version 1: create a alphabet, manually/programically, and then iterate through an index created from the string with indexOf() to get the value of each character.

```
const stringToVal = string => {
  let key = " abcdefgh...z";
  let sum = 0;
  [...string].forEach(l => sum += key.indexOf(l));
  return sum;
}
```

Version 2: this approach uses the fact that the undercase alphabet starts at charcode 97. So substracting 96 from the charCode of a lowercase letter gives you its place in the alphabet. The reduce function then iterates through the array and adds all of the character values together, starting with 0. Neat!

```
const stringToVal = string => [...string]
  .reduce((res, l) => res += l.charCodeAt() -96, 0);
```

[CodeWars](https://www.codewars.com/kata/last-digit-symmetry)

Fun with primes 

first attempt: ugh this got longer than I thought.. 
```
const isPrime = (num) => {
  if( num < 2) return false;
  
  if (num === 2) return true;
  
  if (num % 2 === 0) return false;
  
  for (var i = 3; i*i <= num; i += 2) {
    if (num % i === 0) {
      return false;
    }
  }
  return true;
}

const first = (num) => {
  if (num > 9) {
    let temp = num.toString()
    return parseInt(temp[0] + temp[1], 10);
  }
}

const last = (num) => {
  if (num > 9) {
    let temp = num.toString();
    return parseInt(temp[temp.length - 2] + temp[temp.length - 1], 10);
  }
}

const solve = (a, b) => {
  let ans = 0;
  for(let i = a; i < b;  i++) {
    if(i >= 11) {
      const square = i * i;
      
      if(isPrime(first(i)) === true) {
        if(isPrime(first(square)) === true) {
          if(last(i) === last(square)) {
            ans += 1
          }
        }
      }
    }
  }
  
  return ans;
}
```
OK. I admit it is not very pretty. Lets refactor it a bit. First let's make the isPrime function a little nicer.
```
const isPrime = num => {
    for(let i = 2, s = Math.sqrt(num); i <= s; i++)
        if(num % i === 0) return false; 
    return num !== 1;
}
```

That's a bit more succint, yah? Next up I can shave down them the first and last helper functions by using substr(). I can also remove the first 'if' check as their are no numbers that qualify that are less than 2 digits. 

```
const first = (num) => {
  return parseInt( num.toString().substr(0,2), 10 );
}

const last = (num) => {
  let temp = num.toString();
  return parseInt( temp.substr(temp.length - 2, 2), 10 );
}
```

### D35 2/23/18

Read a few articles. This [one](https://medium.freecodecamp.org/how-i-applied-lessons-learned-from-a-failed-technical-interview-to-get-5-job-offers-656fcf58034d) about a new dev's first coding job was pretty inspiring.

codewars 422 =>

[Bad Apples](https://www.codewars.com/kata/bad-apples/train/javascript)

unfinished snippet
```
const badApples = input => {
  const boxSum = arr => arr.reduce((a,b) => a + b);
 
  let inputCopy = input.filter(box =>  (box[0] !== 0 || box[1] !== 0) ) 
  let firstSpare, secondSpare, insertion;  
  //console.log(inputCopy);
  inputCopy.forEach((box, i) => {
    if( box.includes(0) ) {
      if( ) 
      firstSpare === undefined ? firstSpare = sum : secondSpare = sum;  
    } 
  })
}
```
### 2/24/18 + 2/25/18 

No coding -2 days

###  D34 2/26/18

Codewars 422 => 440;

First challenge was pretty simple; add up all numbers that are multiples of 3 || 5 that are less than 'n'.


My first solution was to use a for loop to fill an array with every number that met the criteria and then reduce it. This got a little messy when the array didn't have numbers in it. I added a ternary statement to deal with this.

```
const solution = number => {
  let numArr = [];
  for ( let i = 1; i < number; i++ ) {
    if (i % 3 === 0 || i % 5 === 0) {
      numArr.push(i)  
    }
  }
  return numArr.length > 0 ? numArr.reduce( (a, b) => a + b ) : 0;
}
```

The top voted answer on this one did without the added complexity of an array, and just used a sum variable that the loop added to as it went. Not as flashy, but probably more efficient and definately easier to read. 

```
function solution(number){
  var sum = 0;
  
  for(var i = 1;i< number; i++){
    if(i % 3 == 0 || i % 5 == 0){
      sum += i
    }
  }
  return sum;
}
```

Using higher order functions and added complexity is not always a good idea. simple !== bad. 

Next Kata: [Find the odd int](https://www.codewars.com/kata/find-the-odd-int/train/javascript)

"Given an array, find the int that appears an odd number of times.

There will always be only one integer that appears an odd number of times."

For this problem I will need a way to count how often each value occurs in the array, then filter for a odd value. 

```
const findOdd = arr => {
  let counts = {};
  arr.forEach(x => counts[x] = (counts[x] || 0) + 1 );
  console.log(counts);
}
```

After thinking about this one for a bit, I came across a pretty clever/eloquent solution to the counting part of the problem. I have no doubt that my solution would have been much more verbose. 

What the above code does is loop through the supplied array and assign a key value pair for each element in the array. If the key is repeated then the loop adds 1 to the value. Pretty neat!

Now let's tackle returning the int that occurs an odd # of times. 

My first impulse would be to reach for a .filter() as I have dealing with arrays so much lately, but that would require converting our object to an array. One way of doing this would be to use Object.entries(obj), but that doesn't look like it is supported for this kata... luckily we can iterate over the object with a for...in loop. winning!

final solution:
```
const findOdd = arr => {
  let counts = {};
  arr.forEach(x => counts[x] = (counts[x] || 0) + 1 );
  
  for( let prop in counts ){
    if( counts[prop] % 2 !== 0 ) {
      return +prop;
    }
  }
}
```

Top voted solution:
```
const findOdd = (xs) => xs.reduce((a, b) => a ^ b);
```

Wow, that is above my head. As far as I understand it, the XOR ('^') operator returns 0 if a pair of bits match, or 1 if they dont match. Since there is only one odd number integer in the array only one value will return 1. All the over value pairs will cross themselves out.

Elegant. Hard to read though. It will take much more exposure to wrap my head about bitwise operators. 

more on [bitwise operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators) 

Another succinct solution (that I didnt think of):
```
// Cool one liner using ES6
const findOdd = A => A.filter(x => A.filter(v => x === v).length % 2 === 1).reduce(a => a);
```

This one is pretty neat. It filters the initial array for values that occur an odd amount of times then reduces those values into a single occurance.


[Equal Sides of an Array](https://www.codewars.com/kata/equal-sides-of-an-array)

```
const findEvenIndex = arr => {
  const sum = array => array.reduce((a, b) => a + b);

  if( sum(arr) === 0) { return 0 };

  for( let i = 1; i < arr.length - 1; i++ ) {
    if ( sum(arr.slice(0, i)) === sum(arr.slice(i + 1)) ) {
      return i;
    }
  }
  
  return - 1
}
```
This approach is not efficient as there are so many loops.

[performance](https://jsperf.com/codewars-equal-sides-of-an-array) of the above problem. The best performing code is below:
```
function findEvenIndex4(arr) {
      var i,
          left,
          right = 0,
          len = arr.length;
  
      if (len === 0) {
          return -1;
      }
  
      left = arr[0];
  
      for (i = 1; i < len; i++) {
          right += arr[i];
      }
  
      for (i = 1; i < len; i++) {
          right -= arr[i];
          if (left === right) {
              return i;
          }
          left += arr[i];
      }
  
      return -1;
  }
```

Much more verbose, but much much faster as it only needs two loops to solve. 

### 2/27/18

Today was super busy and I didn't get to play with much code. Read a few articles and listened to a Shoptalk podcast -1 day.

### D34 2/28/18
 
 watched some UDemy vids; read some YKDJS about Types. Need to code later!

 ### D35 3/1/18

 codeWars
 [Bad Apples](https://www.codewars.com/kata/bad-apples/train/javascript) 

 first attempt:
 ```
const badApples = input => {
 const sum = arr => arr.reduce((a, b) => a + b);
 let inputCopy = input.filter(box =>  (box[0] !== 0 || box[1] !== 0) ) 
 let spares = [];  
 let ans = [];
 let inserted = 0;
 
 inputCopy.forEach((box, i) => {
   if (box[0] === 0 || box[1] === 0) {
     spares.push([box, i])
   } else {
     ans.push(box);
   }
 })

 while(spares.length > 1) {
   let index = spares[0][1];
   let newBox = [ sum(spares[0][0]), sum(spares[1][0]) ]; 
   ans.splice(index - inserted, 0 , newBox);
   inserted++;
   spares.splice(0,2);
 }

 return ans;
}
 ```

[Simple nearest prime](https://www.codewars.com/kata/simple-nearest-prime/train/javascript)

 ```
const solve = n =>{
   const isPrime = num => {
    for(let i = 2, s = Math.sqrt(num); i <= s; i++)
        if(num % i === 0) return false; 
    return num !== 1;
  }

  for(let i = 0; i < 1000; i++) {
    if( isPrime(n - i) ) { 
      return (n - i)
    }
    
    if( isPrime(n + i) ) { 
      return (n + i)
    }
  }
}
 ```

[Next Prime](https://www.codewars.com/kata/next-prime/train/javascript)
 ```
function nextPrime(n){
  if(n === 0) {n++};
  while( n++ ) {
    if ( isPrime(n) ) {
      return n;
    }
  }
}

const isPrime = num => {
    for(let i = 2, s = Math.sqrt(num); i <= s; i++)
        if(num % i === 0) return false; 
    return num !== 1;
}
 ```

 [Multiplying numbers as strings](https://www.codewars.com/kata/multiplying-numbers-as-strings)

 ```

 ```

 Had to skip this one for now. No idea how to do it.

 ### D36 3/2/18

 Codewars fun

  -> 470

  ### D37 3/3/18

  Wordpress: work on a hero slider. 

  ### D38 3/4/18

  ### D38 3/5/18

  More on windows slider. Went with Slick Slider as it looked pretty flexible. Got it loaded up and had a FOOC issue. Found a clever workaround that set all the slides to visibility: hidden; and opacity: 0 and then used a css transition based of an event that only occurs after the slider script starts to return them to visible. Neat. Next issue was that the arrow were hidden offscreen and behind my background image. Next steps are to customize the arrows and add animations to the textbox. 

  ### D39 3/6/18

  codewars fun.

  Count # of value occurances inside an array using an object:
  ```
const arr = [1, 1, 1, 2, 2, 4];
const checkThreeAndTwo = array => {
  let counts = {};
  for(let i = 0; i < array.length; i++) {
    let value = array[i];
    if( typeof counts[value] === "undefined" ) {
      counts[value] = 1;
    } else {
      counts[value]++;
    }
  }
  console.log(counts); // {1: 3, 2: 2, 4: 1}
}
  ```

  or you can use a similar approach using reduce.
  ```
[].reduce((a, b) => (a[b] = a[b] + 1 || 1) && a, {});
  ```
or a forEach loop..
```
array.forEach(el => count[el] = count[el] +1 || 1);
```

 I am not 100% sure what the && a does for the reduce function... without it the funciton only returns one value though. The forEach approach made a lot more sense to me. 


  Finish up slider intergration...
  add animations to textbox... DONE. not in love with the slider. 
  redo + animate arrows on hover..done. these are moderately classy.

  ### D40 3/7/18

  codewars 479 ->

  First algo was to match CC numbers. My first approach used If statements, but then I saw that other solutions used regex so I solved it again using string.match(re). However, the better approach would be to use Regex.test() as it more performative. Neat!

  