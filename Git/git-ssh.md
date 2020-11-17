## Configuring Username and Email for GitHub

<br>

Before setting your ssh you first have to configure your global username and email address after installing Git.
<br>

> `>` git config --global user.name "_your-name_" <br>

> `>` git config --global user.email "_your-email_"

## Generating a new SSH key

1. Open terminal <br>

2. Paste the command text below, substituting in your GitHub email address.

> `>` \$ ssh-keygen -t ed2.... -C "your_email@example.com"

This will result in:

![generating_public/private_key](pics/creating_ssh.png)

1. After you've generated the public/private key pair, you will be asked to "Enter a file in which to save the key", so hit Enter. <br>
   It will choose the default location.

2. Then you will have to enter your secure passphrase 2-times.

## Adding your SSH key to the ssh-agent

1. Start the ssh-agent in the background

> `>` eval "\$(ssh-agent -s)"

> Output: Agent pid ----

2. Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing key that has a different name, replace _id_rsa_ in the command with the nae of your private key file.

> `>` ssh-add ~/.ssh/id_ed-----

> Output: <br>
> Enter passphrase for /home/dci/.ssh/id_ed-----: <br>
> Bad passphrase, try again for /home/dci/.ssh/id_ed-----:
> Identity added: /home/dci/.ssh/id_ed----- (----------------@-----.com)

## Adding a new SSH key to your GitHub account

1. Copy the SSH key to your clipboard. First you have to check the `.ssh` directory for any `.pub` extensions:

> `>` ls -al ~/.ssh

> Output: <br>
> total 16
> drwx------ 2 dci dci 4096 Nov 10 10:28 . <br>
> drwxr-xr-x 25 dci dci 4096 Nov 10 10:35 .. <br>
> -rw------- 1 dci dci 484 Nov 10 10:28 id_ed25519 <br>
> -rw-r--r-- 1 dci dci 115 Nov 10 10:28 id_ed25519.pub <br>

After that copy the contents of your `pub` file:

> `>` gedit ~/.ssh/id_ed25519.pub

- Now go to the _Settings_ in your GitHub account
- click on _SSH and GPG keys_
- paste the key
- click on _New SSH Key_
- if prompted, confirm your GitHub password

2. Checking with hte GitHu host:

Simply type in your terminal:

> `>` ssh -T git@github.com

> Output:
>
> The authenticity of host 'github.com (140.82.121.4)' can't be established. <br>
> RSA key fingerprint is SHA256:--------------------------------. <br>
> Are you sure you want to continue connecting (yes/no/[fingerprint])? yes <br>
> Warning: Permanently added 'github.com,140.82.121.4' (RSA) to the list of known hosts. <br>
> Hi -------! You've successfully authenticated, but GitHub does not provide shell access.

<br>
