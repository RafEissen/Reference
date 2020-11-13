# Updating VSCode on Linux Ubuntu

Type in following commands: 

> `>` $ wget https://vscode-update.azurewebsites.net/latest/linux-deb-x64/stable -O /tmp/code_latest_amd64.deb

> `>` $ sudo dpkg -i /tmp/code_latest_amd64.deb

... or you can simply paste those two commands in a bash script and run them at any time whenever VSCode wants to upgrade. 