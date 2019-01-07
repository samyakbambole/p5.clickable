# 🖱 p5.clickable
**p5.clickable** is a [p5.js](http://p5js.org) library that lets you create and customize buttons and assign event based behaviours to them. Plain speaking, with **p5.clickable** you can create buttons and define what happens when the user *hovers over*, *clicks*, *releases* or moves their cursor *out* of them.

![image](https://lartu.github.io/projects/p5.clickable/canvas.png)

## Code Example
With **p5.clickable** and just a few lines of code you can get a button up and running. For example, to create a plain button at (20, 20) that when pressed changes color and shows an alert message you just do:
``` 
myButton = new Clickable();     //Create button
myButton.locate(20, 20);        //Position Button
myButton.onPress = function(){  //When myButton is pressed
  this.color = "#AAAAFF";       //Change button color
  alert("Yay!");                //Show an alert message
}
```
Easy as pie!

## Live Example
[This example](https://lartu.github.io/projects/p5.clickable/example.html) showcasts some of the main features of this library.
Its source code is available in the `example` folder of this repository.

## How To Use

**p5.clickable** provides the `Clickable` class (aka, the buttons). To create a new button just instantiate a new Clickable, like this:
```
myButton = new Clickable();
```

The starting position of a Clickable defaults to (0, 0) and its size to (100, 50). To move a Clickable you can change its `x` and `y` properties:
```
myButton.x = 100;
myButton.y = 200;
```
or use the `locate` method:
```
myButton.locate(100, 200);
```

Likewise, to resize a Clickable you can modify its `width` and `height` properties:
```
myButton.width = 250;
myButton.height = 100;
```
or use the `resize` method:
```
myButton.resize(250, 100);
```

Clickables also contain other properties that can be changed to alter their appearance:
```
myButton.color = "#FFFFFF";			//Background color of the clickable
myButton.cornerRadius = 10;			//Corner radius of the clickable
myButton.strokeWeight = 2;			//Stroke width of the clickable
myButton.stroke = "#000000";		//Border color of the clickable
myButton.text = "Press Me";			//Text of the clickable
myButton.textColor = "#000000";		//Color of the text
```

To **display** a Clickable, you have to use its `draw` method. For example:
```
function draw(){
  myButton.draw();
}
```
This is very important, for without this step your button will not be shown (nor work).

*TODO: Explicar funciones de click!*
