#Up and running with ruby on rails and heroku in 10 minutes


##run this rails command with postgresql database option
$rails new rails_and_heroku_in_10_mins -d postgresql

##cd to app directory
#####cd rails_and_heroku_in_10_mins


##set up your gemfile by

###add the following gems

#####gem 'bootstrap-generators'
#####gem 'record_tag_helper', '~> 1.0'

###create new group

#####group :production do
 ##### gem 'pg', '~> 0.18'
 # Use Puma as the app server
##### gem 'puma', '~> 3.0'
#####ends


###set ruby version 
##### $echo "2.3.1" > .ruby-version
##### $echo "2.3.1" > .ruby-version

##install bootstrap templates
##### $rails g bootstrap:install

##update gems
##### $bundle install


##scaffold someting simple using bootstrap templates
###e.g items with fields below
##### $rails g scaffold Items name:string quantity:integer description:string amount:decimal 

##in routes.rb under config
###set root/landing page
##### root 'items#index'

##Create a Heroku account and install toolbelt

##continue on your terminal
##Create a new Git repository
##Initialize a git repository in a new or existing directory

##### $git init
##### $git add ./
##### $git commit -m 'ready for deploy'




##### $ heroku login

##Deploy your application

###Commit your code to the repository and deploy it to Heroku using Git.

##### $ git add .
##### $ git commit -am "make it better"
##### $ git push heroku master

###create your application db
##### $ heroku run rails db:migrate



