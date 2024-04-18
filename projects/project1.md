md is a mackdown file 

# Projects Related to DOM

## Projects Links
[click here](https://stackblitz.com/edit/dom-project-chaiaurcode?file=1-colorChanger%2Findex.html)

# Solution Code

## Project 1(Color Changer)
### html code
 ``` 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript Background Color-switcher</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <nav>
        <a href="/" aria-current="page">Home</a>
        <a target="_blank" href="https://www.youtube.com/@chaiaurcode"
          >Youtube channel</a
        >
      </nav>
      <div class="canvas">
        <h1>Color Scheme Switcher</h1>
        <span class="button" id="grey"></span>
        <span class="button" id="white"></span>
        <span class="button" id="blue"></span>
        <span class="button" id="yellow"></span>
        <span class="button" id="purple"></span>
        <h2>
          Try clicking on one of the colors above
          <span>to change the background color of this page!</span>
        </h2>
      </div>
      <script src="chaiaurcode.js"></script>
</body>
</html>
 ```
 ### css code
 ```
 html {
    margin: 0;
  }
  
  span {
    display: block;
  }
  .canvas {
    margin: 100px auto 100px;
    width: 80%;
    text-align: center;
  }
  
  .button {
    width: 100px;
    height: 100px;
    border: solid black 2px;
    display: inline-block;
  }
  
  #grey {
    background: grey;
  }
  
  #white {
    background: white;
  }
  #blue {
    background: blue;
  }
  #yellow {
    background: yellow;
  }
  #purple {
    background: purple;
  }
 ```
 ### javascript code
 ```
const buttons = document.querySelectorAll('.button')
console.log(buttons)
const body= document.querySelector("body");
console.log(body)
buttons.forEach(function (button) {
  console.log(button);
  button.addEventListener('click',function(e){
    console.log(e);
    console.log(e.target);
    if (e.target.id === 'grey') {
        body.style.backgroundColor = e.target.id;
      }
      if (e.target.id === 'white') {
        body.style.backgroundColor = e.target.id;
      }
      if (e.target.id === 'blue') {
        body.style.backgroundColor = e.target.id;//yaha hum direct value bhe likh sakte h like"blue" aur acche se programmer banne ke liye yaha hum aise e.target.id kar ke likhte h"
      }
      if (e.target.id === 'yellow') {
        body.style.backgroundColor = e.target.id;
      }
      if (e.target.id === 'purple') {
        body.style.backgroundColor = e.target.id;
      }
  });
});
 ```