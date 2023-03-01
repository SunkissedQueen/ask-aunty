# README

https://blog.logrocket.com/how-to-use-react-ruby-on-rails/

- Set up React and Rails at the same time using the following command:
$ rails new ask_aunty -d postgresql -T --webpack=react

- cd into app
$ cd ask_aunty

- create empty database
$ rails db:create

Ran the following to enable the Rails app to compile js because the App.js could not be rendered to views.

$ bundle add webpacker
$ bundle add react-rails
$ rails webpacker:install
$ rails webpacker:install:react
$ yarn add @babel/preset-react
$ yarn add @rails/activestorage
$ yarn add @rails/ujs

Generate the appropriate files and folders for React

$ rails generate react:install
$ rails generate react:component App

Add boilerplate code to App.js

Generate a controller to allow App.js to be rendered in a Rails view. 

Call the App.js file in app/views/home/index.html.erb

Direct our Rails app to let webpacker handle the compiling of JavaScript in app/views/layouts/application.html.erb

Direct the Rails app to serve the React App.js component as the landing page in config/routes.rb