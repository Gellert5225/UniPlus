# RESTful Routes

In this section you will find request and response params for all the routes. You will find information about each route's functionality, params for res and req, to help you communicate between server and front-end.

## Login

URL | HTTP Verb | Function
-------------- | -------------- | -------------- 
/login | POST | Login the user

param | HTTP Message | Description
-------------- | -------------- | -------------- 
username | request | Username for the user
password | request | Password for the user
back | response | Redirect back to previous page

## Register

URL | HTTP Verb | Function
-------------- | -------------- | -------------- 
/register | POST | Register a new user

param | HTTP Message | Description
-------------- | -------------- | -------------- 
username | request | Username for the user
password | request | Password for the user
email | request | Email for the user
back | response | Redirect back to previous page

## Logout

Logout function will be handled on server side.


