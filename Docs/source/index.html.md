---
title: Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - swift: Swift
  - java: Java
  - javascript: JavaScript

toc_footers:
  - <a href='https://github.com/Gellert5225/UniPlus.git'>GitHub Repository</a>
  - <a href='localhost:4040'>Database Dashboard</a>

includes:
  - datamodel
  - cloudcode
  - rest

search: true
---

# Introduction

Welcome to the UniPlus documentation! You can use this document as a refrence to data models, REST routes and cloud functions. 

We have language bindings in Swift, Objective-C, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.


# Installation

## Prerequisite

You need to have Node.js installed on your machine. 

We use [Parse](http://parseplatform.org) as our backend service, and you can find their documentations [here](http://docs.parseplatform.org).

## Usage

Our server is deployed on Heroku, to run the server locally, clone the GitHub repo, and go to the folder "Server/Dev" or "Server/Prod". First, you need to install all node dependencies, simply run

`npm install` 

and then you need to start the server using 

`npm start` 

Donezo! Go visit the webpage at localhost:1337

## Dashboard

We also provide a visual tool for viewing our database. To run the dashboard, go to `Dashboard` directory and run

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

# Style Guide

<aside class="notice">Please read this section carefully, it is very important for all team members to have a consistent coding style.</aside>

## Indentation and spacing

> Indentation and spacing

```swift
// correct
let a = 3
let b = 4
let c = a + b

if (c < 10) {
    // do sth.
} else {
    // do sth else.
}

// wrong
let d=3
if(d>3)
{
//do stuff

}
else 
{

}

```

Both swift and Java should use one tab(4 spaces) as indentation, and 2 spaces for JavaScript. 

You should leave one space on the left and right side of operators. And leave one space after keywords.

The opening curly bracket should be in-line.


## Naming and identifiers

> Naming and identifiers

```swift
// correct
let numberOfStudents = 10
let availableSpots = 8

func getExtraStudent() {

}

// wrong
let nos = 10
let s = 8

func my_func1() {

}

```

You should always use camel case for variables and functions, and identifiers should have meaningful and descriptive names. All variables and function names should begin with lower case, all class, struct, and enum should begin with capital letter.

Always initialize your variables! And only declare them right before you gonna use them.

Note, Swift has optional types which allow NULL values, so it is okay to use optional instead of initializing.

