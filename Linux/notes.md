## ////////////////////////////////////////////////////

### How to start Firefox in private window from your terminal :

> `>` nohup firefox -private-window <_url_> &

The main benefit of using this command is that after closing terminal it wont terminate the process and close the firefox browser.

## ///////////////////////////////////////////////////

# Install updates via apt-get command line

1. > `>` apt-get update

Update is used to resynchronize the package index files from their sources on Ubuntu Linux via the Internet

2. > `>` apt-get upgrade

Upgrade is used to install the newest versions of all packages currently installed on the Ubuntu system.

3. > `>` apt-get install <_package-name_>

Install is followed by one or more packages desired for installation. If package is already installed it will try to update to latest version.

Example :

> `>` sudo apt-get install gpg

Output :

Reading package lists... Done <br>
Building dependency tree <br>
Reading state information... Done <br>
gpg is already the newest version (2.2.19-3ubuntu2). <br>
gpg set to manually installed. <br>
The following packages were automatically installed and are no longer required: <br>
libfprint-2-tod1 libllvm9 python3-click python3-colorama <br>
Use 'sudo apt autoremove' to remove them. <br>
0 upgraded, 0 newly installed, 0 to remove and 26 not upgraded.
