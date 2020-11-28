# Links

[:active-pseudo-selector](#-active) <br>
[:first-pseudo-element](#-first) <br>
[:first-child](#-first-child) <br>
[::first-letter](#-first-letter) <br>
[::first-line](#-first-line) <br>

## //////////////////////////////////////////////////////////// :active

The `:active` pseudo-class (pseudo selector) represents an element (such as button) that is being activated by the user. When using a mouse, "activation" typically starts when the user presses down the primary mouse button.

The `:active` pseudo-class is commonly used on `<a>` and `<button>` elements.

**Note:**Styles defined by the `:active` pseudo-class will be overridden by any subsequent link-related pseudo-class(`:link`, `:hover`, or `:visited`) that has at least equal specificity.

To style links appropriately, put the `:active` rule after all other link-related rules, as defined by the (_LoVe-HAte_-order): `:link` - `:visited` - `:hover` - `:active`.

## Example:

Here's the button before being clicked: <br>

![button-before-clicking](pics/active-pseudo-selector-NOT-clicked.png)

Here's the button being clicked: <br>

![button-before-clicking](pics/active-pseudo-selector-clicked.png)

## Example Files:

[lists.html 2nd part](html/lists.html) <br>
[lists.css 2nd part](css/lists.css) <br>

[To Top](#links)

## //////////////////////////////////////////////////////////// :first

The `:first` pseudo-class, used with @-rule, represents the first page of a printed document.

**Note:** You can't change all CSS properties with this pseudo-class. You can only change the margins, orphans, widows, and page breaks of hte document. Furthermore, you may only use absolute-length units when defining the margins. All other properties will be ignored.

## Example:

Press the "Print!" button to print the example. The words on the first page should be somewhere around the center,...

![first-page](pics/first-pseudo-selector-first-page.png)

... while other pages will have their contents at the default position. <br>

![first-page](pics/first-pseudo-selector-second-page.png)

## Example Files:

[rgd.html 4th part](html/rgd.html) <br>
[rgd.css 4th part](css/rgd.css) <br>

[To Top](#links)

## //////////////////////////////////////////////////////////// :first-child

Represents the first element among a group of sibling elements.

## Example:

![first-child](pics/first-child.png)

## Example Files

[lists.html 3rd part](/html/lists.html) <br>
[lists.css 3rd part](/css/lists.css) <br>

[To Top](#links)

## //////////////////////////////////////////////////////////// ::first-letter

Applies styles to the first letter of the first line of a block-level element, but only when not preceded by other content (such as images or inline tables).

## Example:

![::first-letter](pics/first-letter.png)

## Example Files:

[lists.html 1st part](/html/lists.html) <br>
[lists.css 1st part](/css/lists.css) <br>

[To Top](#links)

## //////////////////////////////////////////////////////////// ::first-line

Applies to the first line of a block-level element.

**Note:** The length of first line depends on many factors, including the width of the element, the width of the document, and the font size of the text.

## Example:

![::first-line](pics/first-line.png)

## Example Files:

[lists.html 4th part](/html/lists.html) <br>
[lists.css 4th part](/css/lists.css) <br>

[To Top](#links)
