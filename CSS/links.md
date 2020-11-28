# Links

[:active-pseudo-selector](#-active) <br>
[:first-pseudo-element](#-first) <br>
[:first-child](#-first-child) <br>
[::first-letter](#-first-letter) <br>
[::first-line](#-first-line) <br>
[:first-of-type](#-first-of-type) <br>
[:focus](#-focus) <br>
[:not](#-not) <br>
[:not](#-nth-child) <br>

<hr>

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

<hr>

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

<hr>

## //////////////////////////////////////////////////////////// :first-child

Represents the first element among a group of sibling elements.

## Example:

![first-child](pics/first-child.png)

## Example Files

[lists.html 3rd part](/html/lists.html) <br>
[lists.css 3rd part](/css/lists.css) <br>

[To Top](#links)

<hr>

## //////////////////////////////////////////////////////////// ::first-letter

Applies styles to the first letter of the first line of a block-level element, but only when not preceded by other content (such as images or inline tables).

## Example:

![::first-letter](pics/first-letter.png)

## Example Files:

[lists.html 1st part](/html/lists.html) <br>
[lists.css 1st part](/css/lists.css) <br>

[To Top](#links)

<hr>

## //////////////////////////////////////////////////////////// ::first-line

Applies to the first line of a block-level element.

**Note:** The length of first line depends on many factors, including the width of the element, the width of the document, and the font size of the text.

## Example:

![::first-line](pics/first-line.png)

## Example Files:

[lists.html 4th part](/html/lists.html) <br>
[lists.css 4th part](/css/lists.css) <br>

[To Top](#links)

<hr>

## //////////////////////////////////////////////////////////// :first-of-type

Represents the first element of its type among a group of sibling elements.

## Example:

![first-of-type](pics/first-of-type.png)

## Example Files:

[lists.html 5th part](html/lists.html) <br>
[lists.css 5th part](css/lists.css) <br>

[To Top](#links)

<hr>

## //////////////////////////////////////////////////////////// :focus

Represents an element (such as a form input) that has received focus. It is generally triggered when the user clicks or taps on an element or selects it with the keyboard's `Tab` key.

## Example:

![focus.png](pics/focus.png)

## Example Files:

[rgd.html 4th part](html/rgd.html) <br>
[rgd.css 4th part](css/rgd.css) <br>

[To Top](#links)

<hr>

## //////////////////////////////////////////////////////////// :not()

Represents elements that do not match a list of selectors. Since it prevents specific items from being selected, it is known as the _negation pseudo-class_.

## Implementation:

![not.png](pics/not.png)

## Example:

This example shows the exclusion of all the html elements except for the last class ".notIt" which border is colored yellow-green.

![not.png](pics/notII.png)

## Example Files:

[text.html 5th part](html/text.html) <br>
[text.css 5th part](css/text.css) <br>

[To Top](#links)

<hr>

## //////////////////////////////////////////////////////////// :nth-child()

Matches elements based on their position in a group of siblings.

`:nth-child()` takes a single argument that describes a pattern for matching element indices in a list of siblings.

## Keyword Values:

<ins>**odd**</ins>

Represents elements whose numeric position in a series of siblings is odd: 1, 3, 5, etc.

<ins>**even**</ins>

Represents elements whose numeric position in a series of siblings is even: 2, 4, 6 etc.

## Functional Notation:

<ins>**An+B**</ins>

Represents elements in a list whose indices match those found in a custom pattern of numbers, defined by _An+B_, where:

- `A` is an integer step size,
- `B` is an integer offset,
- `n` is all positive integers, starting from 0.

It can be read as the *An+B*th element of a list.

## Examples:

![nth_child_examples](pics/nth-child_examples.png)

## Example Files:

[lists.html 6th part](html/lists.html) <br>
[lists.css 6th part](css/lists.css) <br>

[To Top](#links)

<hr>
