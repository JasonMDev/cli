#Production and Development with Ruby on Rails
This is the place for command line snippets for using Ruby on Rails.

####Version Control: GitHub
####Deployment: Heroku

##Set-Up Development Environment

##Set-Up Development Environment
### Make a workspace
` $ cd              ` *# Change to the home directory.* <br>
` $ mkdir workspace ` *# Make a workspace directory.* <br>
` $ cd workspace/   ` *# Change into the workspace directory.*
 
### First Time Set-up Github
` $ git config --global user.name "Your Name"` *#* <br>
` $ git config --global user.email your.email@example.com`  <br>
` $ git config --global push.default matching` *# Ensures forward compatabilty.*  <br>
` $ git config --global alias.co checkout` *# Creates an alias for checkout.*

### Set-up Heroku

##Development 
### Generate new app and folders
1. ` $ cd ~/workspace  ` *# "~" jumps to workspace*
2. ` $ rails _4.2.2_ new my_app ` *# This ensures that the same version of Rails that has been installed is used to create the first application’s file structure.*
3. Replace default 'Gemfile.rb' with the base 'Gemfile.rb'.
4. ` $ cd my_app/   ` *# Change into the app directory.*
5. ` $ bundle install   ` *# Install the new Gems via command.*
6. ` $ rails server   ` *# Check if everything is working.*
7. ` $ mv README.rdoc README.md` *# Change to md file type.*
8. Replace '.gitignore file with standard.
9. Add license. Preferably GNU.

### First-time repository setup
1. ` $ cd ~/workspace/my_app/   ` *# Change into the app directory.*
2. ` $ git init  ` *# Initialize empty Git repository*
2. ` $ git add .  ` *# Add all files*
3. ` $ git status  ` *# Check files which are in the staging area.*
4. ` $ git commit -m "Initialize repository" ` *# Initialize repository with firts commit.*
5. ` $ git log ` *# See a list of your commit message*
 a. Alternative: ` $ git log --pretty=format:"%h - %an, %ar : %s"`
 b. Alternative: ` $ git log --pretty=format:"%h %s" --graph` 
6. [Got to listing 1.12... firt repo push upstream, find one that works.... dummy]
7. 

##Set-Up Version Control
####New Repository 

##File & Folder Management
#####Moving around:
- A: ```$ cd ~``` *# Go to home location.*
- B: ```$ cd ..``` *# Go down one folder.*


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


