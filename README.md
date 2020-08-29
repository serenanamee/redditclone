# How to build a Reddit Web App in Rails 6

This is my first challenge of Ruby on rails. It took me over a week to finish this App. I’d like to help total beginners for Ruby on rails to solve the problems they might encounter on the way.

### Requirement for this APP:
* Users can sign up and sign-in/sign-out
* Users can submit a link with a title and a URL
* Users can vote up and vote down on the submission
* User can comment on the submission

**Link submissions**
First, create a git new branch
```git checkout -b link_scaffold```
And then generate a scaffold for link submission
```rails g scaffold link title:string url:string```
There are two column name title and url , and the data type is string.
In Ruby on Rails if the data type is string we could omit it.
The code could be :
```$ rails g scaffold link title url```
When you create your Rails application for the first time, it will not have a database yet. In order for it to start, you will need to make sure the database is up and running. Therefore, we need to run
```$ rake db:migrate```
In rails 5 , using rails command for everything. Before rails 5 we used rake for db commands. So, rails db:migrate works as well.

After rake db:migrate , run server again
```$ rails s```
Go to http://localhost:3000/links. The page supposed to be like below:
Let's try to make some New links , make sure it works.
Looks good. Time to merge git branch to git master branch.
Control c to interrupt the server.
Then,
git status
git add .
git commit -m' generate link scaffold'
git checkout master
git merge link_scaffold
git push
