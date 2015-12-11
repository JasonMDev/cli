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

##Development Cycle
### Generate new app and folders
1. ` $ cd ~/workspace  ` *# "~" jumps to workspace*
2. ` $ rails _4.2.2_ new my_app ` *# This ensures that the same version of Rails that has been installed is used to create the first application’s file structure.*
3. Replace default 'Gemfile.rb' with the base 'Gemfile.rb'.
4. ` $ cd my_app/   ` *# Change into the app directory.*
5. ` $ $ bundle install --without production` *# Install the new Gems via command.*
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

### Commit cycle
1. ` $ cd ~/workspace/my_app/   ` *# Change into the app directory.*
2. $ git checkout master
$ git checkout -b modeling-users
If you’re using Git, now would be a good time to commit if you haven’t done so in a while:

$ bundle exec rake test
$ git add -A
$ git commit -m "Make a basic User model (including secure passwords)"
Then merge back into the master branch and push to the remote repository:

$ git checkout master
$ git merge modeling-users
$ git push

$ bundle exec rake test
$ git push heroku
$ heroku run rake db:migrate
$ heroku run console --sandbox
>> User.create(name: "Joe Smoe", email: "js@example.com", password: "foobar", password_confirmation: "foobar")

## Test Driven Development
1. Run test suite: `$ bundle exec rake test`
2. Run specific folder test: `$ bundle exec rake test:specific`



##MVC Framework Usages
###Models
#### Modelling Users
1. Generating a User model. `$ rails generate model User name:string email:string`
2. Run the migration: `$ bundle exec rake db:migrate`
3. Roll-back the migration if there was an error or mistake: `$ bundle exec rake db:rollback`
4. Add structure to an existing model via migration generator: `$ rails generate migration add_index_to_users_email`
5. Add the instructions manually in the new migration file: 
````ruby 
 add_index :users, :email, unique: true
 ````
6. Run the migration: `$ bundle exec rake db:migrate`
7. Add password digest to users:`$ rails generate migration add_password_digest_to_users password_digest:string`

#### Exploring Models in console:
##### Creating User Objects
1. Sandbox Rails Console: `$ rails console --sandbox` *# Any modifications you make will be rolled back on exit.*
2. Create new user object in memory: 
````ruby 
 >> user = User.new(name: "Joe Smoe", email: "JS@example.com")
````
3. Test the validity of user: `user.valid?`
4. Save the new user: ` >> user.save`
5. Check user: `>> user`
6. Check user: `>> user.name`
7. Check user: `>> user.email`
8. Check user: `>> user.updated_at`
9. Make and save:
````ruby
 >> User.create(name: "A Nother", email: "another@example.org")
 >> foo = User.create(name: "Foo", email: "foo@bar.com")
````
10. Delete/destroy: `>> User.destroy`
 
##### Finding user objects
1. Find user id 1: `>> User.find(1)`
2. Find user by email: `>> User.find_by(email: "JS@example.com")`
3. Find the first user: `>> User.first`
4. Find all users: `>> User.all`

##### Updating user objects
1. Update user method 1: `>> user.email = "guy@lives.org"`
2. Update user method 2: 
````ruby
 >> user.update_attributes(name: "The Guy", email: "guy@lives.org")
````

#### User Validation:
1. Run model test: `$ bundle exec rake test:models`
2. Check full error message in colsole: `>> user.errors.full_messages`

#### User Authentication:
1. >> User.create(name: "Joe Smoe", email: "JS@example.com", password: "foobar", password_confirmation: "foobar")
2. : ` `>> user = User.find_by(email: "JS@example.com")
2. : ` `>> user.password_digest
3. >> !!user.authenticate("not teh right password") +> returnrs false
4. >> user.authenticate("foobar") => returns user
4. >> !!user.authenticate("foobar")




##Set-Up Version Control
####New Repository 

$ git checkout master
$ git checkout -b modeling-users

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


