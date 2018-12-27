# Introduction

Welcome to the UniPlus documentation! You can use this document as a refrence to data models, REST routes and cloud functions. 

We have language bindings in Swift, Objective-C, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.


# Installation

## Prerequisite

You need to have Node.js installed on your machine. 

We use [Parse](http://parseplatform.org) as our backend service, and you can find their documentations [here](http://docs.parseplatform.org).

## Usage

Our server is deployed on Heroku, to run the server locally, clone the GitHub repo, and go to the folder "Server/Dev". First, you need to install all node dependencies, simply run

`npm install` 

and then you need to start the server using 

`npm start` 

Donezo! Go visit the webpage at localhost:1337

## Dashboard

We also provide a visual tool for viewing our database. To run the dashboard, go to `dashboard` directory and run

`npm start`

and then you can go to localhost:4040 to view or change data in a more beautiful way.

## Documentation

The documentation is inside the `Docs/source/index.html.md` file. You can refer to [this](https://github.com/lord/slate/wiki/Markdown-Syntax) article about Markdown syntax.

# Development

## Web

### Front-end

We use EJS as our view engine, you can find more about EJS [here](http://ejs.co). 

All ejs files should be placed insede `views` folder, for javascript, css and images please put them in `public/asset` folder.

### Back-end

We use Node.js and MongoDB as our server + database service. 

All REST routes js files should be placed inside `routes` folder.
