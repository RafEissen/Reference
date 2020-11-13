## Generating a new SSH key

1. Open terminal <br>

2. Paste the command text below, substituting in your GitHub email address. 

> `>` $ ssh-keygen -t ed25519 -C "your_email@example.com"

This will result in: 

> Generating public/private ed----- key pair.
Enter file in which to save the key (/home/dci/.ssh/id_ed----): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/dci/.ssh/id_ed-----
Your public key has been saved in /home/dci/.ssh/id_ed-----.pub
The key fingerprint is:
SHA256: "*here is the long key* -----------@----.com
The key's randomart image is: <br>
And here is the image for the key.

3. After you've generated the public/private key pair, you will be asked to "Enter a file in which to save the key", so hit Enter. <br>
It will choose the default location. 

4. Then you will have to enter your secure passphrase 2-times. 

## Adding your SSH key to the ssh-agent

1. Start the ssh-agent in the background 

> `>` eval "$(ssh-agent -s)"

> Output: Agent pid ----

2. Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace *id_rsa* in the command with the nae of your private key file. 

> `>` ssh-add ~/.ssh/id_ed-----

> Output: <br>
> Enter passphrase for /home/dci/.ssh/id_ed-----: <br>
Bad passphrase, try again for /home/dci/.ssh/id_ed-----: 
> Identity added: /home/dci/.ssh/id_ed----- (----------------@-----.com)

## Adding a new SSH key to your GitHub account 

1. Copy the SSH key to your clipboard. First you have to check the `.ssh` directory for any `.pub` extensions:

> `>` ls -al ~/.ssh

> Output: <br>
> total 16
drwx------  2 dci dci 4096 Nov 10 10:28 . <br>
drwxr-xr-x 25 dci dci 4096 Nov 10 10:35 .. <br>
-rw-------  1 dci dci  484 Nov 10 10:28 id_ed25519 <br>
-rw-r--r--  1 dci dci  115 Nov 10 10:28 id_ed25519.pub <br>

After that copy the contents of your `pub` file: 

> `>` gedit ~/.ssh/id_ed25519.pub

-   Now go to the *Settings* in your GitHub account 
-   click on *SSH and GPG keys* 
-   paste the key 
-   click on *New SSH Key* 
-   if prompted, confirm your GitHub password
  
2. Checking with hte GitHu host: 

Simply type in your terminal:

> `>` ssh -T git@github.com

> Output: 
> 
> The authenticity of host 'github.com (140.82.121.4)' can't be established. <br>
RSA key fingerprint is SHA256:--------------------------------. <br>
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes <br>
Warning: Permanently added 'github.com,140.82.121.4' (RSA) to the list of known hosts. <br>
Hi -------! You've successfully authenticated, but GitHub does not provide shell access.

