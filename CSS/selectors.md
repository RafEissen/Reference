# Selectors & Combinators

[universal selector](#universal-selector-) <br>
[type selector](#-type-selector) <br>
[class selector](#-class-selector) <br>
[id selector](#-id-selector) <br>
[attribute selectors](#-attribute-selector) <br>
[child-combinator](#-child-combinator) <br>
[adjacent-sibling-combinator](#-adjacent-sibling-combinator) <br>
[general-sibling-combinator](#-general-sibling-combinator) <br>

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

<ins>**[attribute^=value]**</ins>

Matches every element whose attribute value begins with a specified value. Don't forget, case-sensitivity matters.

![caret selector](pics/caret-selector.png)

<ins>**[attribute|=value]**</ins>

Is used to select elements with the specified attribute starting with the specified value.

**Alt:** This selector is very similar to the "starts with" selector. Here, it matches a value that is either the only value or is the _first_ in a dash-separated list of values.

![pipe selector](pics/pipe-selector.png)

<ins>**[attribute$=value]**</ins>

Matches every element whose attribute value ends with a specified value.

![ends-with-selector](pics/ends-with-selector.png)

<ins>**[attribute*=value]**</ins>

Matches every element whose attribute value containing a specified value.

![asterisk selector](pics/asterisk-selector.png)

## Example Files:

**No Files** <br>

[To Top](#selectors--combinators) <br>

<hr>

# Combinators

## //////////////////////////////////////////////////////////// Child Combinator

The child combinator (`>`) is placed between two CSS selectors and is used to select elements with a specific parent.

**Note:** Elements that are not directly a child of the specified parent, are not selected.

![child-combinator](pics/child-combinator.png)
![child-combinator](pics/child-combinatorII.png)

## //////////////////////////////////////////////////////////// Adjacent Sibling Combinator

Is used to select an element that is directly after another specific element.

![adjacent-sibling-combinator](pics/adjacent-sibling-combinator.png)
![adjacent-sibling-combinatorII](pics/adjacent-sibling-combinatorII.png)

## //////////////////////////////////////////////////////////// General Sibling Combinator

The _element1~element2_ selector matches occurrences of _element2_ that are preceded by _element1_. Both elements must have the same parent, but _element2_ does not have to be immediately preceded by _element1_.

![General-Sibling-Combinator](pics/General-Sibling-Combinator.png) <br>
![General-Sibling-Combinator](pics/General-Sibling-CombinatorII.png)
