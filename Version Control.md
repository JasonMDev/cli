#Version Control with GitHub
These are code snippets for general version control using GitHub via the Command Line Interface.

##Heading 2
###Heading 3
####Heading 4
#####Heading 5

####File & Folder Management
#####Create new file:
- ```sh
$ :> filename.ext
```
- ```` $ :>> filename.ext
- ```` $ touch filename.ext 

Read file in bash: sh,bash, zsh new file $ :> filename.ext or $ :>> filename.ext or $ touch filename.ext Edit in nano: $ nano filename.ext

sh See in cli:

$ cat filename.ext 
bash

$ cat filename.ext 
zsh

$ cat filename.ext 
New Repository Create Folder Create repo in GitHub $ git init $ git add . $ git commit -am "Initialise Repository." $ git remote add origin https://github.com/JasonMDev/project-name.git $ git push -u origin --all # pushes up the repo and its refs for the first time

Fetch and merge

$ git fetch $ git merge origin/master
