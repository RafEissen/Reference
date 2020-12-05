# Overview

[Box Model](#-box-model)

# Layouts

## //////////////////////////////////////////////////////////// Box-Model

The <ins>box model</ins> is for formula upon which layout boxes are based, and comprises content, padding, border, and margin. CSS lets you alter these values to change the overall site and shape of elements' display.

![box-model-diagram](pics/box-model-diagram.png)

If you are a Firebug user, you might be used to the diagram like this, which does a nice job of showing you the numbers affecting any box on the page:

![Firebug's_Box_Model_Display](pics/Firebugs_Box_Model_Display.png)

The size of the box itself is calculated like this:

| Size       | Calculation                                                        |
| ---------- | ------------------------------------------------------------------ |
| **Width**  | width + padding-left + padding-right + border-left + border-right  |
| **Height** | height + padding-top + padding-bottom + border-top + border-bottom |

<br>

## The `display` property

Block elements assume all of the available space in one dimension. Typically, this is the horizontal dimension, because the `writing-mode`is set to `horizontal-tb`.

![writing_modes](pics/writing_modes.png)

If a box is defined as a block, it will behave in the following ways:

- The box will break onto a new line.
- The box will extend in the inline direction to fill the space available in its container. In most cases this means that the box will become as wide as its container, filling up 100% of the space available.
- The _width_ and _height_ properties are respected.
- Padding, margin and border will cause other elements to be pushed away from the box

<ins>Inline</ins> elements behave differently. THey are laid out <ins>in line</ins> with the current context, writing mode, and direction. They are only as wide as their content, and are placed adjacently wherever there is space to do so. Block elements follow 'flow direction' (from top to bottom), and inline elements follow writing direction.

![writing-direction](pics/writing-direction.png)

If a box has an outer display type of `inline`, then:

- The box will not break onto a new line.
- The _width_ and _height_ properties will bot apply.
- Vertical padding, margins, and borders will apply but will not cause other inline boxes to move away from the box.
- Horizontal padding, margins, and borders will apply and will cause other inline boxes to move away from the box.

Thinking typographically, it could be said that <ins>block elements are like paragraphs, and inline elements are like words</ins>.

**Block elements** (also called <ins>block-level</ins> elements) afford you control over both the horizontal and vertical dimensions of the box. That is, you can apply width, height, margin, and padding to a block element and it will take effect.
On the other hand, inline elements are sized _intrinsically_ (prescribed width and height values do not take effect) and only _horizontal_ margin and padding values are permitted. Inline elements are designed to conform to the flow of horizontal placement among other inline elements.

`Inline-block` is a hybrid of `block`and `inline`. You can set vertical properties on _inline-block_ elements, although this is not always desirable - as the proceeding illustration demonstrates.

![inline-block](pics/inline-block.png)

## Content in Boxes

Without intervention, it is the contents of an element that determines its size and shape. Content makes `inline` elements grow horizontally, and `block` elements grow vertically. Left to its own devices, the area of a box is determined by the area of the content it contains. Because web content is _dynamic_ (subject to change), static representations of web layouts ar extremely misleading.

## The `box-sizing` property

By default, the dimensions of a box are the dimensions of the box's content _plus_ its padding and border values (implicitly: `box-sizing`: `content-box`). That is, if you set an element to be 10rem wide, then add padding on both sides of 1rem, it will be 12rem wide:

```
10rem + 1rem of left padding + 1rem of right padding
```

If you opt for `box-sizing`: `border-box`, the content area is reduced to accommodate the padding and the total width equals the prescribed width of 10rem.

<ins>**Generally**</ins>, it is considered preferable to use the `border-box` model for all boxes. It makes calculating/anticipating box dimensions easier.

Any styles, like `box-sizing: border-box`, that are applicable to all elements are best applied using the * ("wildcard") selector. Being able t affect the layout of multiple elements (in this case, *all\* elements) simultaneously is how CSS brings efficiency to layout design.

```
* {
    box-sizing: border-box;
}
```

**Alt:** To ensure the parent element retains a height of `100vh`, despite the additional padding, a `box-sizing: border-box` value must be applied. Where it is not, the padding is _added_ to the total height.

Only where the height or width of a box is constrained does the difference between `content-box`and `border-box` come into play.

For illustration, consider a block element placed inside another block element. Using the `content-box` model and a padding of `1rem`, the child elemet will overflow by `2rem` when `width: 100%` is applied.

![content-box-ex](pics/conten-box-ex.png)

Why? Because `width: 100%` means _"make the width of this element the same as the parent element"_. Since we are using the `content-box` model, the _content_ is made 100% wide, then the padding is added on to this value.

But if we use `width: auto` (we can just remove `width: 100%`, since `auto` is the default value) the child within the parent box perfectly. And that's _regardless_ of the `box-sizing` value.

![width_auto](pics/width_auto.png)

Implicitly, the `height` is also set to `auto`, meaning it is derived from the content. Again, `box-sizing` has no effect.
