# Overview

[](#)

# Layouts

## //////////////////////////////////////////////////////////// Box-Model

The <ins>box model</ins> is for formula upon which layout boxes are based, and comprises content, padding, border, and margin. CSS lets you alter these values to change the overall site and shape of elements' display.

![box-model-diagram](pics/box-model-diagram.png)

If you are a Firebug user, you might be used to the diagram like this, which does a nice job of showing you the numbers affecting any box on the page:

![Firebug's_Box_Model_Display](pics/Firebugs_Box_Model_Display.png)

The size of the box itself is calculated like this:

| **Width**  | width + padding-left + padding-right + border-left + border-right |
| ---------- | ----------------------------------------------------------------- |
| **Height** | width + padding-left + padding-right + border-left + border-right |
