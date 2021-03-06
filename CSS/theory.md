# Overview

[Box Model](#-box-model) <br>
[Box Sizing](#the-box-sizing-property) <br>
[Box Model Example](#example) <br>
[Minimum Height](#-min-height) <br>
[Maximum Height](#-max-height) <br>
[Minimum Width](#-min-width) <br>
[Maximum Width](#-max-width) <br>
[Vertical Alignment](#-vertical-alignment) <br>
[Aligning Items in a Flex Container](#-aligning-items-in-a-flex-container) <br>
[Flex Grow](#-flex-grow) <br>
[Flex Basis](#-flex-basis) <br>
[Flex Grow Factor](#-flex-grow-factor) <br>
[Flex Shrink](#-flex-shrink) <br>

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

[To Top](#overview)

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

## What if these values are undeclared?

If padding or borders are undeclared, they are either zero (likely if you are using a [css reset](https://css-tricks.com/poll-results-what-css-reset-do-you-use/)) or the browser default value (probably **not** zero especially on form elements that are commonly not reset). More on that read below in [CSS Reset section](#-CSS-Reset)

[To Top](#overview)

## Example:

Lets recreate following example from: [Gradient Hero.](https://github.com/RafEissen/Exercises/blob/main/December/exercises.md#gradient-hero)

Here is the mockup picture:

![mockup picture](pics/example-01-desktop.png)

Here is the HTML-code:

![html part](pics/html-structure.png)

### First Part

Initially we can divide the screen in two parts. First part is going to be filled with image as a background property. For that to happen we have to create a box by mentioning only the visual height of `75vh`:

> height: 75vh;

Once the box is established, we can start to implement our image as a background together with multiple gradient stops. In order to center the image we have to mention `background-position: center` as well as `no-repeat` in order for the image stop repeating itself and also fully cover the given container section.

Here is the CSS snippet:

> background-repeat: no-repeat; <br>
> background-position: center; <br>
> background-size: cover;<br>

Finally we can apply our `linear-gradient` property on the picture and start with the second part of the exercise.

[To Top](#overview)

### Second Part

Second part is text part with a black `background-color` property which is wrapped in another `<section>` called _txt_half_. In the beginning we can crate distance from the 1st half by mentioning the top-bottom `padding` property:

```
.txt_half {
  background-color: black;
  padding: 3.75rem 0;
  color: rgba(255, 255, 255, 0.8);
}
```

Now our page looks like this:

![padding](pics/padding-mockup.png)

The text inside _txt-half_ `<section>` is going to be put in a `<div>` called _main-container_, which will be centered with the maximum width of `60rem` (you can also use `%` unit) and vertically aligned with left-right `padding`.

```
.main-container {
  margin: 0 auto;
  padding: 0 1.25rem;
  max-width: 60rem;
}
```

![padding](pics/div-padding.png)

Next step comes with styling of `<h1>` header:

```
.main-container h1 {
  font-family: "Times New Roman", Times, serif;
  font-size: 3.5rem;
  font-weight: 300;
}
```

After that we can add some distance to our text container:

```
.columns {
  padding: 1.2rem 0;
  margin-top: 1.3rem;
}
```

![columns-container](pics/columns-container.png)

Final step concludes the editing of _txt_half_ section. here we give the maximum width of 70% to text blocks, edit line heights as well as `font-size` and add some margin.

```
.main-container p {
  max-width: 70%;
  line-height: 1.5;
  font-size: 1.1rem;
  margin: 1rem 0;
}
```

The final result looks like this:

![final-result](pics/final-result.png)

[To Top](#overview)

## //////////////////////////////////////////////////////////// `min-height`

Defines the maximum height of an element. If the content is smaller than the minimum height, the minimum height will be applied. If the content is larger than the minimum height, the `min-height` property has no effect.

Let's take an example to demonstrate a simple use case.

We have a section with a description text. The goal is to have a minimum height for the section, so it can handle short or long content.

![min-height-exampleI](pics/min-height-exampleI.png)

The minimum height is `100px`, and with flexbox, the content is centered horizontally and vertically. Now the height of the section will expand to contain the new content. By having that, we can build components that are fluid and responsive to its content.

![min-height-exampleI](pics/min-height-exampleII.png)

[To Top](#overview)

## //////////////////////////////////////////////////////////// `max-height`

Defines the maximum height of an element. If the content is larger than the maximum height, it will overflow, which is defined by the <ins>overflow</ins> property. If the content is smaller than the maximum height, the `max-height` property has no effect.

![max-height-property](pics/max-height-property.png)

Consider the example above. The text content is bigger than the specified space and thus it creates an overflow, which can be controlled with the `overflow` property.

[To Top](#overview)

## //////////////////////////////////////////////////////////// `min-width`

Sets the minimum width of an element. If the content is smaller than the minimum width, the minimum width will be applied. If the content is larger than the minimum width, the `min-width` property has no effect.

**Note:** The `min-width` property prevents the value of the <ins>width</ins> property from becoming smaller than `min-width`.

Note that the default value for `min-width` is `auto`, which resolves to `0`. Let's take a look at the example below:

![min-width-property](pics/min-width-property.png)

We have a button with a varying text within in. The text might range from one word to multiple. To guarantee that it will have a minimum width even if it has one word only, `min-width` should be used. The minimum width is `100px` so that even if the button has a very short content, like "Done" word, or an icon only, it will be big enough to be noticed.

In case the button width gets longer, `padding` on the horizontal sides should be added to achieve a proper looking button.

![min-width_padding](pics/min-width_padding.png)

[To Top](#overview)

## //////////////////////////////////////////////////////////// `max-width`

Sets the maximum width of an element. If the content is larger than the maximum width, it will automatically change the height of the element. If the content is smaller than the maximum width, the `max-width` property has no effect.

**Note:** The `max-width` property prevents the value of the <ins>width</ins> property from becoming larger than `max-width`. The value of the `max-width` property overrides the width property. The default value for `max-width` is `none`.

A common and simple use case for `max-width` is using it with images. Consider the below example:

![max-width-property](pics/max-width-property.png)

The image is larger that its parent element. By using `max-width: 100%`, the width of the image won't exceed the width of its parent. In case the image is smaller than its parent, `max-width: 100%` won't have an actual effect on the image, because it's smaller that its parent.

[To Top](#overview)

## //////////////////////////////////////////////////////////// Vertical Alignment

The `vertical-align` property in CSS controls how elements set next to each other on a line are lined up. It sets vertical alignment of an inline, inline-block or table-cell box.

Here's an example of how it could be used to vertically position an `<img>` in a line of text:

![positioning img in a line of text](pics/vertical-alignment.png)

[To Top](#overview)

## Example:

Let's create a box with two inline-block elements in it. For this we will only use the code snippet below:

```
  <body>
    <main>
      <section class="box text-half">
      </section>
      <section class="box img-half"></section>
    </main>
  </body>
```

By the way our final example will look like mockup picture below:

![mockup](pics/mockup.jpg)

First we have to mention `padding` property in `body` element:

```
body {
  padding: 50px;
    border: 2px solid black;
}
```

This will cause the `main` element in the next step to have a distance from the browser window.

Now we have to center our `main` element:

```
main {
  margin: 0 auto;
  border: 2px solid darkslateblue;
}
```

After these two steps we have our `main` element which has a distance in all four directions from the browser window:

![padding](pics/body-main.png)

Like in the mockup picture above we take two `section` elements (one for text, one for picture) and give each two separate classes:

- "_.box_" for both `section` elements
- "_.text-half_" for the first one and "_.img-half_" for the second one

```
.box {
  border: 2px solid red;
  width: 7.5rem;
  height: 20vh;
  display: inline-block;
  vertical-align: middle;
}
```

![inline blocks](pics/inline-blocks.png)

We have both our inline blocks vertically aligned in the middle and can now style them according to the mockup picture.

[To Top](#overview)

## //////////////////////////////////////////////////////////// Box Folding & Expanding

There might be some special case where you want to preserve an equal distance between a farther border of a box (i.e. input field) and a closer border of adjacent box by expanding/folding of a browser window. Here is an visual example:

![expanding/folding](pics/width-padding.gif)

You can clearly see that the width of input field goes all the way by expanding/folding of a browser window without losing any length in the process.

In the first step you have to declare the width of an input field like so:

```
input {
  width: 100%;
}
```

![width100](pics/width100.png)

It's possible that by declaring 100% width the border may go beyond the required space. In the aforementioned example the input field would transgress the border of our sections. In order to prevent this from happening we have to additionally declare padding:

```
section {
  padding-right: 2rem;
}
```

[To Top](#overview)

## //////////////////////////////////////////////////////////// Creating a Box With Padding

Here is the full html code:

![html](pics/html-card.png)

In order to create a box with a text content without using any width, height or margin properties like the example below:

![using only padding](pics/only_padding.gif)

we first have to define our `padding` property in the `main` element:

![define padding](pics/main-padding.png)

```
main {
  padding: 10rem 3rem;
  border: 1px solid rgba(30, 58, 133, 0.993);
}
```

After that our main job is almost done. We only have to define our `linear-gradient` function to cover full page:

```
body {
  background-image: linear-gradient(
      -40deg,
      rgba(255, 255, 255, 0),
      rgba(255, 127, 80, 0.9)
    ),
    linear-gradient(10deg, purple, hotpink);
}
```

and later edit our `section` element:

```
section {
  padding: 1rem 2.5rem 3rem 2.5rem;
  border-radius: 0.5rem;
  box-shadow: 0px 0px 20px 10px #0000000d;
}
```

[To Top](#overview)

## //////////////////////////////////////////////////////////// Aligning Items in a Flex Container

To center our box we use the `align-items` property to align our item on the cross axis, which in this case is the block axis running vertically. We use `justify-content` to align the item on the main axis, which in this case the inline axis running horizontally.

![position items in flexbox](pics/main-cross-axis.png)

## Properties that control alignment:

- `justify-content` - controls alignment of all items in the main axis.
- `align-items` - controls alignment of all items on the cross axis.
- `align-self` - controls alignment of an individual flex item on the cross axis.
- `align-content` - controls space between flex lines on the cross axis.

[To Top](#overview)

## //////////////////////////////////////////////////////////// Flex Basis

The `flex-basis` property sets the size of the flex item before growing and shrinking happens.

**Alt:** It specifies the initial size of the flex item before any space distribution happens.

The initial value for this property is `auto`. If `flex-basis` is set to `auto` then to work out the initial size of the item the browser first checks if the main size of the item has an absolute size set.

Following example shows a series of inflexible boxes, with both `flex-grow` and `flex-shrink` set to `0`. Here we can see how the first item - which has an explicit width of 150px set as the main size - takes a `flex-basis` of `150px`, whereas the other two items have no width and so are sized according <ins>to their content width.</ins>

![flex basis example](pics/flex-basis-example.gif)

If you want to completely ignore the size of the item when doing space distribution then set `flex-basis` to `0`. This essentially tells flexbox that all the space is up for grabs, and to share it out in proportion. In this case the box will be sized to its content width.
However if the `flex-basis` gets overwritten with the new size of `160px` like this

> **HTML**

```
 <div class="box">
        <div>One</div>
        <div>Two</div>
        <div>Three</div>
      </div>
```

> **CSS**

```
 .box {
        display: flex;
      }

      .box :first-child {
        width: 150px;
      }

      .box > * {
        flex: 0 0 160px;
      }
```

then all flex items will be equally sized to `160px`. including the first one.

## Summary:

1. Is `flex-basis` set to `auto`, and does the item have a width set? If so, the size will be based on that width.
2. Is `flex-basis` set to `auto` or `content` (in a supporting browser)? If so, the size is based on the item size.
3. Is `flex-basis` a length unit, but not zero? If so this is the size of the item.
4. Is `flex-basis` set to `0`? If so then the item size is not taken into consideration for the space-sharing calculation.

[To Top](#overview)

## //////////////////////////////////////////////////////////// Flex Grow

The `flex-grow` property specifies the **flex frow factor**, which determines how much the flex item will grow relative to the rest of the flex items in the flex container when the positive free space is distributed.

If you use `1` as the grow factor, the space would be distributed evenly between all of flex items. However you could also give them all a `flex-grow` of `88`, or `100`, or `1.2` if you like - it is a ratio.

![flex basis example](pics/flex-grow-zero-auto.gif)

```
 .box {
        display: flex;
      }

      .box :first-child {
        width: 150px;
      }

      .box > * {
        flex: 1 0 auto;
      }
```

> `flex: 1 1 auto;`

We are working with a `flex-basis` equal to the content size so the available space to distribute is subtracted from the total available space (the width of the flex container), and the leftover space is then shared out equally among each item. <br>
Our bigger item ends up bigger because <ins>it started from a bigger size</ins>, even though it has the same amount of spare space assigned to it as the others.

> `flex: 1 1 0;`

Here we are saying that the size of the item for the purpose of our space distribution calculation is `0` - all the space is up for grabs and as all of the items have the same `flex-grow` factor, they each get an equal amount of space distributed. The end result is three equal width, flexible items.

[To Top](#overview)

## //////////////////////////////////////////////////////////// Flex Grow Factor

Let's take a look at following example:

![flex-grow-factors](pics/flex-grow-factors.png)

Working from a `flex-basis` pf `0` this means that the available space is distributed as follows. We need to add up the flex grow factors, then divide the total amount of positive free space in the flex container by that number, which in this case is 4. We then share out the space according to the individual values:

- the first item gets one part
- the second one part
- the third two parts

This means that the <ins>third item is twice the size of the first and second items</ins>.

Remember that you can only use positive values and it is the ratio between one item and the others that matters. Next example shows implementation of various ratios:

![flex-grow-factors](pics/flex-grow-factors.gif)

[To Top](#overview)

## //////////////////////////////////////////////////////////// Flex Shrink

The `flex-shrink` property specifies the **flex shrink factor**, which determines how much the flex item will shrink relative to the rest of the flex items in the flex container when negative free space is distributed.

This property deals with situations where the browser calculates the `flex-basis` values of the flex items, and finds that they are too large to fit into the flex container. As long as `flex-shrink` has a positive value the items will shrink in order that they do not overflow the container.

So where `flex-grow` deals with adding available space, `flex-shrink` manages taking away space to make boxes fit into their container <ins>without overflowing.</ins>

In the next example there are three items in a flex container; each item has a width of `200px`, and the container is `500px` wide. With `flex-shrink` set to `0` the items are not allowed to shrink and so they overflow the box.

![flex shrink](pics/flex-shrink.gif)

Change the `flex-shrink` value `1` and you will see each item shrink by the same amount, in order that all of the items now fit in the box. They have become smaller than their initial width in order to do so.

**Note:** The flex shrink factor is multiplied by the flex base size when distributing negative space. This distributes negative space in proportion to how much the item is able to shrink, so that e.g. a small item won't shrink to zero before a larger item has been noticeably reduced.

Flexbox prevents small items from shrinking to zero size during this removal of negative free space. The items will be floored at their `min-content` size - the size that they become if they take advantage of any soft wrapping opportunities available to them.

In the next example you can change the width on the flex container - increasing it to `700px` for example - and then reduce the flex width, you can see that the first two items will wrap, however they will never become smaller than its `min-content` size. As the box gets smaller space is then just removed from the third item.

![flex shrink](pics/flex-shrink-example.gif)

## Summary: Do we have available space?

Items can't grow with no positive free space, and they won't shrink unless there is negative free space.

1. If we take all the widths of flex items and sum them up and this sum is **less** than the total width of the container then you have <ins>positive space</ins> and `flex-grow` comes into play.
2. If the total sum of flex items widths is **more** than the total width of the container, then you have a negative space and `flex-shrink` comes into play.

[To Top](#overview)

## //////////////////////////////////////////////////////////// Grid

CSS Grid Layout is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system. You work with Grid Layout by applying CSS rules both to a parent element (which becomes the Grid Container) and to that element's children (which become Grid Items).

## The Grid Container and Grid Items

We create a _grid container_ by declaring `display: grid`or display: `inline-grid` on an element. As soon as we do this, all _direct children_ of that element become _grid items_.

Take a look at this code:

```
<div class="wrapper">
  <div class="item item-1"> </div>
  <div class="item item-2"> </div>
  <div class="item item-3"> </div>
</div>
```

In this example `wrapper` is the grid container.

The children (i.e. _direct_ descendants) of the grid container. Here the `item` elements are grid items, but `sub-item` isn't.

```
<div class="container">
  <div class="item"> </div>
  <div class="item">
    <p class="sub-item"> </p>
  </div>
  <div class="item"> </div>
</div>
```

[To Top](#overview)

## Grid Line

The dividing lines that make up the structure of the grid. They can be either vertical ("column grid lines") or horizontal ("row grid lines") and reside on either side of a row or column. Here the yellow line is an example of a column grid line.

![grid line](pics/grid-line.png)

[To Top](#overview)

## Grid Cell

The space between two adjacent row and two adjacent column grid lines. It's a single "unit" of the grid. Here's the grid cell between row grid lines 1 and 2, and column grid lines 2 and 3.

![grid line](pics/grid-cell.png)

## Grid Track

The space between two adjacent grid lines. You can think of them like the columns or rows of the grid. Here's the grid track between the second and third row grid lines. We define rows and columns on our grid with the `grid-template-columns` and `grid-template-rows` properties.

![grid-track](pics/grid-track.png)

[To Top](#overview)

## Grid Area

The total space surrounded by four grid lines. A grid area may be composed of any number of grid cells. Here's the grid area between row grid lines 1 and 3, adn column grid lines 1 and 3.

![grid-area](pics/grid-area.png)

## The fr Unit

Grid introduces an additional length unit to help us create flexible grid tracks. The new <code>fr</code> unit represents a fraction of the available space in the grid container. The next grid definition would create three equal width tracks that grow and shrink according to the available space.

![grid-fr-unit](pics/grid-fr-unit.png)

[To Top](#overview)

## repeat() notation

In order to repeat all or a section of the track listing we can also use the repeat() notation. So the same code above can be written as:

```
  display: grid;
  grid-template-columns: repeat(3, 1fr);
```

repeat() notation can be used for a part of the track listing. In this next example I have created a grid with an initial 20-pixel track, then a repeating section of 6 <code>1fr</code> tracks then a final 20-pixel track.

```
  display: grid;
  grid-template-columns: 20px repeat(6, 1fr) 20px;
```

repeat() notation takes the track listing, and uses it to create a repeating pattern of tracks. In this next example the grid will consist of 10 tracks, a <code>1ft</code> track, and then followed by a <code>2fr</code> track. This pattern will be repeated five times.

```
  display: grid;
  grid-template-columns: repeat(5, 1fr 2fr);
```

[To Top](#overview)

## Track sizing with minmax()

When setting up an explicit grid or defining the sizing for automatically created rows or columns we may want to give tracks a minimum size, but also ensure they expand to fit any content that is added.

Following example applies <code>minmax()</code> in the value of <code>grid-auto-rows</code>. This means automatically created rows will be a minimum of `100px` tall, and a maximum of `auto`. Using `auto` means that the size will look at the content size and will stretch to give space for the tallest item in a cell, in this row.

![minmax](pics/minmax.png) <br>
![minmax](pics/minmaxII.png) <br>

[To Top](#overview)

## Grid Lines

It should be noted that when we define a grid we define the grid tracks, not the lines. Grid then gives us numbered lines to use when positioning items.

Example demonstrates a grid with three columns and two rows.

![grid lines](pics/grid-lines.png)

## Positioning items in a Grid

When placing an item, we target the line - rather than the track.

Following shows distribution where the first two items are placed on a three column track grid, using the `grid-column-start, grid-column-end, grid-row-start` and `grid-row-end` properties.

![grid-positioning](pics/grid-positioning.png) <br>

Working from left to right, the first item is placed against column line 1, and spans to column line 4, which in our case is the far-right line on the grid:

```
  grid-column-start: 1;
  grid-column-end: 4;
```

You can also shorten those two commands simply by mentioning `grid-column` property:

```
  grid-column: 1 / 4;
```

**or**

```
  grid-column: 1 / -1;
```

<code>-1</code> will span all your columns.

It begins at row line 1 and ends at row line 3, therefore spanning two row tracks.

```
  grid-row-start: 1;
  grid-row-end: 3;
```

**or**

```
  grid-row-start: 1 / 3;
```

The second item starts on grid column line 1, and spans one track. This is the default so there is no need to specify the end line. It also spans two row tracks from row line 3 to row line 5. The other items will place themselves into empty spaces on the grid.

![grid-positioning](pics/grid-positioningII.png) <br>

[To Top](#overview)

## Layering items with z-index

Grid items can occupy the same cell. If we return to our example with items positioned by line number, we can change this to make two items overlap.

Following example shows the <code>nav</code> bar positioned on top of `header` because of our `z-index` property.

**Tip:** If you have multiple `z` properties in your code, don't pick number like: 1, 2, 3, 4 and so on. Instead choose wider range of numbers like 1, 10, 20 because you'll always have a place to put additional item in between.

> **HTML**

```
  <nav>
    <ul>
      <li>About</li>
      <li>Home</li>
      <li>Contact</li>
    </ul>
  </nav>
  <header><h1>Header</h1></header>
```

> **CSS**

```
nav {
  background-color: #c2c1a8;
  grid-column: 3 / -1;
  grid-row: 1;
  z-index: 10;
  display: flex;
  align-items: center;
}
```

![z-index](pics/grid-z-index.png)

[To Top](#overview)
