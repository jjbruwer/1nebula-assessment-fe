
# Front-end Code Challenges

## Question 1
Given the below code snippet, solve the problems that follow:

```html
<div id="firstDiv" class="red-card">
<div id="secondDiv" class="red-card">

<style>
    #secondDiv {
        background: orange;
    }

    div {
        height: 150px;
        width: 150px;
        background: green;
    }

    .red-card {
        background: red;
    }

    .yellow-card {
        background: yellow;
    }
</style>
```

1. What will the colour of both div elements be?
2. How would you dynamically target ```firstDiv``` and make it's colour pink? (provide the code snippet)
3. How would you dynamically target ```secondDiv``` and add the ```yellow-card``` class to its class list? (provide the code snippet)

## Answer 1

1.1. Since non of the divs are closed, only the last div's colour would show, thus orange.
1.2. 
```html
<!-- Front-end Code Challenges -->
<div id="firstDiv" class="red-card"></div>
<div id="secondDiv" class="red-card"></div>

<style>
    #secondDiv {
        background: orange;
    }

    div {
        height: 150px;
        width: 150px;
        background: green;
    }
    div:nth-child(1) {
        background: #FF69B4; /* I prefer hex above named fix colour values. */
    }

    .red-card {
        background: red;
    }

    .yellow-card {
        background: yellow;
    }
</style>
```
1.3. 


## Question 2
Consider the ```compareIt``` function definition

```javascript
function compareIt(num1, num2) {
    return num1 == num2;
}

compareIt(5, "5");
```

1. Why will the function call return true? 
2. How could one change this function so that data types are checked as well as values?

## Answer 2
1.1. The two values would be treated the same. One is a string and the other is a number.


```javascript
function compareIt(num1, num2) {
    return num1 === num2;
}

console.log(compareIt(5, "5")); // This will return false
```

1.2. 



## Question 3
1. How would you make a web page mobile friendly (i.e responsive)? 
   * Provide examples of this.
2. What is the benefit of bundling .js scripts into one file? 
3. What needs to be done to ensure the browser understands Sass styling?
4. What should be done to ensure browser compatibility with newer flavours of JavaScript like ES6/7?

## Answer 3
3.1. 
3.2. 
- Smaller file size by condense code(removing space, comments and line breaks.
- For improved load speeds on server requests.
- Files are merged into one js file, less server requests.
3.3. 
3.4. 
