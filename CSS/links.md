# Links

[:active-pseudo-selector](#-active) <br>
[list-style-position](#-list-style-position) <br>
[list-style-type](#-list-style-type) <br>

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
