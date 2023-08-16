
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

## 

1.2. 
```html
<!-- Front-end Code Challenges -->
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <title>A 1Nebula assessment for the Front-End</title>
  <meta name="description" content="A 1Nebula assessment for the Front-End">

  <link rel="icon" href="/favicon.ico">
  <link rel="icon" href="/favicon.svg" type="image/svg+xml">
  <link rel="stylesheet" href="css/main.css">
  <script type="text/javascript">
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
  </script>

</head>

<body>
  <!-- Front-end Code Challenges -->
  <div id="firstDiv" class="red-card"></div>
  <div id="secondDiv" class="red-card"></div>

</body>
</html>
```

## 

1.3. 
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <title>A 1Nebula assessment for the Front-End</title>
  <meta name="description" content="A 1Nebula assessment for the Front-End">

  <link rel="icon" href="/favicon.ico">
  <link rel="icon" href="/favicon.svg" type="image/svg+xml">
  <link rel="stylesheet" href="css/main.css">
  <script type="text/javascript">
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
  </script>

</head>

<body>
  <!-- Front-end Code Challenges -->
  <div id="firstDiv" class="red-card"></div>
  <div id="secondDiv" class="red-card"></div>


<script type="text/javascript">
  var el = document.getElementById("secondDiv");

  el.classList.remove("red-card");
  el.classList.add("yellow-card");
</script>
</body>
</html>
```

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

## 

1.2. 
```javascript
function compareIt(num1, num2) {
    return num1 === num2;
}

console.log(compareIt(5, "5"));  // Output: false
```


## Question 3
1. How would you make a web page mobile friendly (i.e responsive)? 
   * Provide examples of this.
2. What is the benefit of bundling .js scripts into one file? 
3. What needs to be done to ensure the browser understands Sass styling?
4. What should be done to ensure browser compatibility with newer flavours of JavaScript like ES6/7?

## Answer 3
3.1. 
- Viewport Meta Tag:
  
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
 ```
- Fluid Grid Layout (Bootstrap
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap 5 Grid example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js"></script>
  <style>
  .imgF {
    height: 200px;
    background: #aaa;
  }
  </style>
</head>
<body>

<div class="p-5 bg-primary text-white text-center">
  <h1>Bootstrap 5 Grid example</h1>
  <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p> 
</div>

<nav class="navbar navbar-expand-sm bg-dark navbar-dark">
  <div class="container-fluid">
    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link active" href="#">First</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Link 1</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Link 2</a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="#">Second</a>
      </li>
    </ul>
  </div>
</nav>

<div class="container mt-5">
  <div class="row">
    <div class="col-sm-4">
      <h2>About Me</h2>
      <h5>Photo of me:</h5>
      <div class="imgF">Fake Image</div>
      <p>Culpa qui officia deserunt mollit anim..</p>
      <h3 class="mt-4">Some Links</h3>
      <p>Lorem ipsum dolor sit ame.</p>
    </div>
    <div class="col-sm-8">
      <h2 class="mt-5">TITLE HEADING</h2>
      <h5>Title description</h5>
      <div class="imgF">Fake Image</div>
      <p>Some text..</p>
      <p>Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit.</p>
    </div>
  </div>
</div>

<div class="mt-5 p-4 bg-dark text-white text-center">
  <p>Footer</p>
</div>

</body>
</html>

 ```
- Browser Compatibility - Evaluate your website across different browsers to pinpoint and resolve any compatibility issues.
- Performance Optimization: Reduce the utilization of large images and avoid unnecessary scripts that might impede the loading speed on mobile devices.
- Mobile-First Approach: From design to final development version, start by designing for mobile screens and then progressively enhance the design for larger screens using media queries.
## 

3.2. 
- Smaller file size by condense code(removing space, comments and line breaks.
- For improved load speeds on server requests.
- Files are merged into one js file, less server requests.

## 
  
3.3.
- Install a Sass compiler
- Populate the stylesheet with SASS code
- Compile it on run-time, built into frameworks like Angular
- Then make sure you are pointing to the stylesheet

## 
  
3.4. 
- Use Polyfills: Newer versions of JavaScript have some cool features that can't be easily recreated just by translating the code. For these situations, we have something called polyfills.
- Instead of browser detection, employ feature detection techniques to identify whether a specific feature is supported by the user's browser. Libraries like Modernizr can help with this approach.
- Testing Across Browsers: Frequently assess your code across various browsers and their versions to detect any compatibility concerns. Utilize tools such as BrowserStack or Sauce Labs to aid in testing across different browsers and operating systems.
- Keep Learning: Stay updated on the latest JavaScript language features and browser compatibility.
