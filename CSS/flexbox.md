# Overview

[align content](#-align-content) <br>
[align items](#-align-items) <br>
[align self](#-align-self) <br>
[justify content](#-justify-content) <br>
[justify items](#-justify-items) <br>

Flexbox is very popular because it brought better alignment capabilities to the web and enabled proper vertical alignment, so it's gonna be easier now to center a box. This reference will show most properties for the <ins>parent element (the flex container)</ins> and <ins>the child elements (the flex items)</ins>.

## //////////////////////////////////////////////////////////// `align-content`

Sets the distribution of space between and around content items along a flexbox's cross-axis (vertically) or a grid's block axis.

**Note:** This property only takes effect on multi-line flexible containers, where `flex-flow` is set to either `wrap` or `wrap-reverse`). A single-line flexible container (i.e. where `flex-flow` is set to its default value, `no-wrap`) will not reflect `align-content`.

Short overview:

![align content](pics/align-content.png)

[To Top](#overview)

## Property Values:

<ins>**stretch**</ins>

Default value. Lines stretch to take up the remaining space.

![align-content gif](pics/align-content.gif)

<ins>**center**</ins>

Items are packed to each other in the center of the alignment container along the cross axis (vertically).

![align-content-center](pics/align-content-center.gif)

<ins>**flex-start/start/self-start**</ins>

Items are placed at the start of the cross axis. The difference between these is subtle, and is about respecting the `flex-direction` rules or the `writing-mode` rules.

![align content start](pics/align-content-start.gif)

[To Top](#overview)

<ins>**flex-end/end/self-end**</ins>

Items are placed at the end of the cross axis.

![align content start](pics/align-content-end.gif)

<ins>**baseline**</ins>

Items are aligned such as their baselines align.

Use the overview explanation as an example.

<ins>**space-between**</ins>

Items are evenly distributed along the cross axis. The spacing between each pair of adjacent items is the same. The first line is at the start edge of the alignment container in the cross axis, and the last line is at the end of the alignment container.

![align content space between](pics/align-content-space-between.gif)

<ins>**space-around**</ins>

Items are evenly distributed with equal space around each line. The empty space before the first and after the last item equals <ins>**half of the space**</ins> between each pair of adjacent items.

![align content space around](pics/align-content-space-around.gif)

<ins>**space-evenly**</ins>

The items are evenly distributed within the alignment container along the cross axis. The spacing between each pair of adjacent items, the start edge and the first item, and the end edge and the last item, are all exactly the same.

![align content space evenly](pics/align-content-space-evenly.gif)

[To Top](#overview)

## //////////////////////////////////////////////////////////// `align-items`

Defines the default behavior for how flex items are laid out along the cross axis on the current line.

![align-items-overview](pics/align-items-overview.png)

## Property Values:

<ins>**stretch**</ins>

Default. Items are stretched to fit the container.

![align items stretch](pics/align-items-stretch.gif)

<ins>**center**</ins>

Items are positioned at the center of the container's cross axis.

![align items center](pics/align-items-center.gif)

<ins>**flex-start/start/self-start**</ins>

Items are placed at the start of the cross axis.

![align items flex start](pics/align-items-flex-start.gif)

[To Top](#overview)

<ins>**flex-end/end/self-end**</ins>

Items are placed at the end of the cross axis.

![align items flex end](pics/align-items-flex-end.gif)

<ins>**baseline**</ins>

Items are aligned such as their baselines align.

![align items baseline](pics/align-items-baseline.gif)

[To Top](#overview)

## //////////////////////////////////////////////////////////// `align-self`

Specifies the alignment for the specified item inside the flexible container.

**Note:** The `align-self` property overrides the flexible container's `align-items` property.

Short overview:

![align-self-overview](pics/align-self-overview.gif)

Property values have same behavior as in `align-items` property.

[To Top](#overview)

## //////////////////////////////////////////////////////////// `flex-direction`

Sets how flex items are placed in the flex container defining the main axis and the direction (normal or reversed). Think of flex items as primarily laying out either in horizontal rows or vertical columns.

Example overview:

![flex-direction](pics/flex-direction.png)

## Property Values:

<ins>**row**</ins>

Default. The flex items are displayed horizontally, as a row (from left to right).

<ins>**row-reverse**</ins>

Same as row, but in reverse order.

<ins>**column**</ins>

The flexible items are displayed vertically, as a column.

<ins>**column-reverse**</ins>

Same as column, but in reverse order.

[To Top](#overview)

## //////////////////////////////////////////////////////////// `flex-flow`

This is a shorthand for the `flex-direction` and `flex-wrap` properties, which together define the flex container's main and cross axes. The default value is _row nowrap_.

## //////////////////////////////////////////////////////////// `flex-wrap`

Sets whether flex items are forced onto one line or can wrap onto multiple lines.

![flex wrap](pics/flex-wrap.png)

## Property Values:

<ins>**nowrap**</ins>

Default. All flex items will be on one line.

<ins>**wrap**</ins>

Flex items will wrap onto multiple lines, from top to bottom.

<ins>**wrap-reverse**</ins>

Behaves the same as `wrap`, only in reverse order.

[To Top](#overview)

## //////////////////////////////////////////////////////////// `justify-content`

Defines how the browser distributes space between and around content items along the main-axis (horizontally) of a flex container.

![justify content overview](pics/justify-content-overview.png)

As a GIF:

![justify content overview](pics/justify-content-overviewII.gif)

## Property Values:

In a nutshell, the property values are the same as in the `align-content` property, only for the <ins>main-axis</ins>. For more reference see the [MDN docs](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content).

[To Top](#overview)

## //////////////////////////////////////////////////////////// `justify-items`

Defines the default `justify- self` for all items of the box, giving them all a default way of justifying each box along the appropriate axis.

![justify items overview](pics/justify-items-overview.gif)

**Note:** In flexbox layouts, this property is <ins>**ignored**</ins>.

[To Top](#overview)

## //////////////////////////////////////////////////////////// `justify-self`

Sets the way a box is justified inside its alignment container along the appropriate axis.

**Note:** In flexbox layouts, this property is <ins>**ignored**</ins>.

[To Top](#overview)
