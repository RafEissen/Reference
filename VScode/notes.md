# Overview

[Updating VScode on Linux (Ubuntu)](#updating-vscode-on-linux-ubuntu)

<hr>

## Updating VSCode on Linux Ubuntu

Type in following commands:

> `$` wget https://vscode-update.azurewebsites.net/latest/linux-deb-x64/stable -O /tmp/code_latest_amd64.deb

> `$` sudo dpkg -i /tmp/code_latest_amd64.deb

... or you can simply paste those two commands in a bash script and run them at any time whenever VSCode wants to upgrade.

[To Top](#overview)

<hr>

## Adding boilerplate code to CSS stylesheets (on Mac)

- Open VScode and press:

  ```
  Shift + Cmd + P
  ```

- Type in _snippets_ and select _css_ or _css.json_ option
- Right after the commented text paste this code chunk:

```
"CSS Boilerplate": {
		"prefix": "cssbp",
		"body": [
		  ":root {",
		  "\tbox-sizing: border-box;",
		  "}",
		  "",
		  "* {",
		  "\tbox-sizing: inherit;",
		  "\tpadding: 0;",
		  "\tmargin: 0;",
		  "}"
		]
	  }
```

- Close it, open CSS file and type in the name after _"prefix"_ (`cssbp` in our example)
