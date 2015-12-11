#Version Control with GitHub
These are code snippets for general version control using GitHub via the Command Line Interface.

##Heading 2
###Heading 3
####Heading 4
#####Heading 5

##Set-Up Version Control
####New Repository 

##File & Folder Management
#####Create new file:
- A: ```$ :> filename.ext```
- B: ```$ :>> filename.ext```
- C: ```` $ touch filename.ext ````

#####Edit in nano:
 ```sh 
 $ nano filename.ext
 ```

#####See in cli:
```zsh 
$ cat filename.ext 
```
##Initiate Version Control
####New Repository 
- Create Folder : *project-name*
- Create repo in GitHub : *project-name*
- ```$ git init ```
- ```$ git add . ```
- ```$ git commit -am "Initialise Repository." ```
- ```$ git remote add origin https://github.com/JasonMDev/project-name.git ```
- ```$ git push -u origin --all ``` # pushes up the repo and its refs for the first time

####Fetch and merge
Use fetch method:

```$ git fetch ```
<br>
```$ git merge origin/master```

use "git pull" to update your local branch:
```$ git fetch ```
<br>
```$ git pull ```


