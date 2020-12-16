# Selectors & Combinators

[universal selector](#universal-selector-) <br>
[type selector](#-type-selector) <br>
[class selector](#-class-selector) <br>
[id selector](#-id-selector) <br>
[attribute selector](#-attribute-selector) <br>

## //////////////////////////////////////////////////////////// Universal Selector

Matches elements of any type.

![type selector](pics/uni-selector.png)
![type selector](pics/uni-selector-result.png)

## Example Files:

[selector.html, 1st part](html/selector.html) <br>

[To Top](#selectors--combinators)

<hr>

## //////////////////////////////////////////////////////////// Type Selector

Matches elements by node name. In other words, it selects all elements of the given type within a document.

![type selector](pics/type-selector.png)

## Example Files:

[selector.html, 2nd part](html/selector.html) <br>

[To Top](#selectors--combinators)

<hr>

## //////////////////////////////////////////////////////////// Class Selector

Matches elements based on the contents of their `class` attribute.

![class selector](pics/class-selector.png)

## Example Files:

**No Files**

[To Top](#selectors--combinators)

<hr>

## //////////////////////////////////////////////////////////// ID Selector

Matches an element based on the value of the element's `id` attribute. In order for the element to be selected, its `id` attribute must match exactly the value given in the selector.

![id selector](pics/id-selector.png)

## Example Files:

**No Files**

[To Top](#selectors--combinators)

<hr>

## //////////////////////////////////////////////////////////// Attribute Selector

Is used to select elements with a specified attribute.

<ins>**[attribute]**</ins>

Is used to select elements with a specified attribute.

![attribute](pics/attribute.png)

<ins>**[attribute=value]**</ins>

Is used to select elements with a specified attribute and value.

![attribute](pics/attr=value.png)

<ins>**[attribute~=value]**</ins>

Is used to select with an attribute value containing a specified word.

Following example selects all elements with a title attribute that contains a space-separated list of words, one of which is "flower":

![attribute](pics/attr~=value.png)
![attribute](pics/attr~=valueII.png)
