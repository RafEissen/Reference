# Overview

[display](#-display) <br>
[Grid Template Area](#-grid-template-areas) <br>

## //////////////////////////////////////////////////////////// `display`

Defines the element as a grid container and establishes a new grid formatting context for its contents.

## Property Values:

<ins>**grid**</ins>

Generates a block-level grid container.

<ins>**inline-grid**</ins>

Generates an inline-level grid container.

[To Top](#overview)

## //////////////////////////////////////////////////////////// `grid-template-areas`

Defines a grid template by referencing the names of the grid areas which are specified with the `grid-area` property. Repeating the name of a grid area causes the content to span those cells. A period (`.`) signifies an empty cell. The syntax itself provides a visualization of the structure of the grid.

Take a look at following example:

![grid-template-example](pics/grid-template-exampleII.png) <br>
![grid-template-example](pics/grid-template-exampleI.png) <br>
![grid-template-result](pics/grid-template-result.png) <br>

By repeating _head_ area two times will cause our header span over two columns. On the other side the _nav_ area spans two rows cells.

[To Top](#overview)

## //////////////////////////////////////////////////////////// `grid-template-rows`

Defines the line names and track sizing functions of the grid rows. 
