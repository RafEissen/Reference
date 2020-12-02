# Overview

(proceed after fill)

[object-fit](#-object-fit) <br>
[object-position](#-object-position) <br>

<hr>

## //////////////////////////////////////////////////////////// display

Sets whether an element is treated as a <ins>block or inline element</ins> and the layout used for its children, such as flow layout, grid or flex.

## //////////////////////////////////////////////////////////// object-fit

Is used to specify how an `<img>` or `<video>` should be resized to fit its container.

## Property Values:

<ins>**fill**</ins>

Default. The replaced content is sized to fill the element's content box. If necessary, the object will be stretched or squished to fit.

![object-fit-fill.png](pics/object-fit-fill.png)

<ins>**contain**</ins>

The replaced content is scaled to maintain its aspect ratio while fitting within the element's content box.

![object-fit-contain.png](pics/object-fit-contain.png)

<ins>**cover**</ins>

The replaced content is sized to maintain its aspect ratio while filling the element's entire content box. The object will be clipped to fit.

![object-fit-cover.png](pics/object-fit-cover.png)

<ins>**none**</ins>

The replaced content is not resized.

![object-fit-none.png](pics/object-fit-none.png)

<ins>**scale-down**</ins>

The content is sized as if _none_ or _contain_ were specified, whichever would result in a smaller concrete object size.

Example is the same as the _content_ value.

## Example Files:

[links.html, 3rd part](html/links.html) <br>

[To Top](#overview)

<hr>

## //////////////////////////////////////////////////////////// object-position

Is used together with _object-fit_ to specify how an `<img>`or `<video>` should be positioned with x/y coordinates withing the element's box. Areas of the box which aren't covered by the replaced element's object will show the element's background.

## Property Values:

<ins>**position**</ins>

Specifies the position of the image or video inside its content box. First value controls the x-axis adn the second value controls the y-axis. Can be a string (left, center or right), or a number (in px or %). Negative values are allowed.

Following example shows the positioning of the image with its right edge flush against the right edge of the element's box (100% on x-axis) and is located 10% of the way down the height of the element's box (y-axis).

![object-position](pics/object-position.png)

## Example Files:

[links.html, 4th part](html/links.html) <br>

[To Top](#overview)

<hr>
