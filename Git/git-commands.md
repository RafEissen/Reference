**proceed with git add or - remote**

## ////////////////////////////// `<git init>` 
<br>

Turns any directory into a Git repository. It’s one way to start a new project with Git. To start a repository, use either git init or git clone.

- `git init` : <br>
  
Transform the cirrent directory into a Git repository

- `git init` <directory> : <br>
  
Transform a directory in the current path into a Git repository. 

- `git init --bare` : <br>
  
Create a new bare repository (a repository to be used as a remote repository only, that won't contain active development)

## ////////////////////////////// `<git clone>` 
<br>

Is used to create a copy of a specific repository or branch within a repository. 

When you clone a repository, you don't get one file, like you may in other centralized version control systems. By cloning with Git, you get the entire repository - all files, all branches, and all commits. 

-   `git clone [url]` :

Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits. 

**Example:** <br>

> `>` $ git clone https://github.com/---------201110-github

> Output: 

Cloning into '201110-github'... <br>
Username for 'https://github.com': RafEissen <br>
Password for 'https://RafEissen@github.com': <br>
remote: Enumerating objects: 3, done. <br>
remote: Counting objects: 100% (3/3), done. <br>
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 <br>
Receiving objects: 100% (3/3), done.

**Note:** By using *https* as your *URL*, you will have to type in your password as well as your username each time you going to clone something, which might become pretty devastating as time goes by. 

## ////////////////////////////// `<git pull>` 




## ////////////////////////////// `<git push>` 
<br>

`git push` updates the remote branch with local commits. It is one of the four commands in Git that prompts interaction with the remote repository. You can also think of `git push` as *update* or *publish*. 

By default, `git push` only updates the corresponding branch on the remote. So, if you are checked out to the *master* branch when you execute `git push`, then only the *master* branch will be updated. It's always a good idea to use `git status` to see what branch you are on before pushing to the remote.

> `>` $ git push

Enumerating objects: 9, done. <br>
Counting objects: 100% (9/9), done. <br>
Delta compression using up to 4 threads <br>
Compressing objects: 100% (4/4), done. <br>
Writing objects: 100% (5/5), 578 bytes | 289.00 KiB/s, done. <br>
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0 <br>
remote: Resolving deltas: 100% (2/2), completed with 2 local objects. <br>
To github.com:RafEissen/hello-world-Raffie.git <br>
   f368a0d..0f24015  main -> main

> `>` $ git push -f

Force a push that would otherwise be blocked, usually because it will delete or overwrite existing commits (*Use with caution!*)

> `>` $ git push -u origin [branch]

Useful when pushing a new branch, this creates an upstream tracking branch with a lasting relationship to your local branch 

> `>` $ git push -all

Push all branches 


**2nd Example:**

**Q: Connect your local repository to a remote repo with the same name on Github.**

**A:** 
- create a repo with the same name (as in local) on GitHub
- in your local repo start terminal and type in :

> `>`  git remote add origin git@github.com:Ra-----en/myCV2.git

- after you connected to your repo under different branch (in this case *dev* branch) - it's time to push:

> `>` git push -u origin dev

## ////////////////////////////// `<git rm>` 

Remove files and folders from the working tree and from the index

> `>` git rm -rf <*folder*>

After that proceed with:

> `>` git add <*file*> <br>

> `>` git commit -m "..." <br>

> `>` git push 