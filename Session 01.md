# Instruction Materials

## Online
### https://p5js.org/

### p5.js wiki

https://github.com/processing/p5.js/wiki


## Books
### Getting Started with p5.js

https://learning.oreilly.com/library/view/getting-started-with/9781457186769/




# Setup Local Environment

## [[Session 00 - Node]]


## vscode

https://code.visualstudio.com/




# HTML Doc


```html
<html>
  <head>
    <script src="https://cdn.jsdelivr.net/npm/p5@1.9.0/lib/p5.js"></script>
    <script src="sketch.js"></script>
  </head>
  <body>
    <main>
    </main>
  </body>
</html>
```




# First Sketch

## Lone Circle

```js
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  ellipse(50,50,80,80);
}
```


# Mouse following Circles

![[Pasted image 20240120170131.png]]

https://learning.oreilly.com/library/view/getting-started-with/9781457186769/ch02.html#your-first-program

```js
function setup() {
  createCanvas(480, 120);
}

function draw() {
  if (mouseIsPressed) {
    fill(0);
  } else {
    fill(255);
  }
  ellipse(mouseX, mouseY, 80, 80);
}
```



# Basic Shapes

![[Pasted image 20240120171618.png]]



## Rectangle

![[Pasted image 20240120171719.png]]

```js
function setup() {
  createCanvas(480, 120);
}

function draw() {
  background(204);
  rect(180, 60, 220, 40);
}
```


## Ellipse

The _x_ and _y_ coordinates for a rectangle are the upper-left corner, but for an ellipse they are the center of the shape.




# Drawing Order

If you want a shape to be drawn on top of all other shapes, it needs to follow the others in the code.

![[Pasted image 20240120171931.png]]


```js
function setup() {
  createCanvas(480, 120);
}

function draw() {
  background(204);
  ellipse(140, 0, 190, 190);
  // The rectangle draws on top of the ellipse
  // because it comes after in the code
  rect(160, 30, 260, 20);
}
```


## Put It in Reverse

![[Pasted image 20240120172025.png]]




# Shape Properties

## Stroke Weight

```js
function setup() {
  createCanvas(480, 120);
}

function draw() {
  background(204);
  ellipse(75, 60, 90, 90);
  strokeWeight(8);  // Stroke weight to 8 pixels
  ellipse(175, 60, 90, 90);
  ellipse(279, 60, 90, 90);
  strokeWeight(20);  // Stroke weight to 20 pixels
  ellipse(389, 60, 90, 90);
}
```



