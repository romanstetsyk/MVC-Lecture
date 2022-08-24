# MVC Architectural pattern

## What is MVC?

Over the years websites have changed from simple static documents to complex applications with hundreds of developers working on them. As the application grows in size it is essential to organize the codebase in a way to make it easy to work with. That's why developers created different architectures to structure their applications, the so called "skeletons" on which they are built, that define how different components, interfaces, databases, etc. interact with one another.

MVC is a popular software pattern used to break up the logic of an application into three different components:

- **M**odel
- **V**iew
- **C**ontroller

## Brief History

- First introduced in 1979 by computer scientist Trygve Reenskaug
- Throughout the 1980's and early 90's, the MVC pattern was primarily used in desktop applications.
- By the late 1990's, it became pretty popular within web applications.

## Usage in popular projects

- Ruby on Rails
- ASP.NET MVC
- Laravel
- Angular
- Django

> NOTE: Frameworks implement the MVC structure, but MVC itself is not a framework.

## CRUD application flow:

1. Client makes a request to the server
1. Server process the request.
1. Server interacts with the database to get/add/update/delete data
1. Server creates a page and sends it back to the client
1. Client renders the page

All of this can be summarized in the diagram below:

![Application flow diagram](/images/appflow.png)

This is the structure that happens regardless of the application architecture, whether it's MVC or not.
But this is what MVC is built around.

## MVC structure

- Code related to the database section goes into the model.

- Code that's processing the information to or from the database or before it gets to the view is the controller.

- Code that should be sent to the client goes into the view.

You can see that the Model - Veiw - Controller come directly from this traditional flow of websites.

![Application flow diagram](/images/mvc.jpg)

## Model

- Responsible for maintaining data
- Interacts with database
- Communicates with the controller
- Never communicates with the view directly

## View

- Responsible for all of the visual aspects of the application
- Can be implemented using templating engines (ejs, handlebars, pug, etc.), or front-end frameworks (React, Vue, etc.)
- Communicates with the controller
- Never communicates with the database directly

## Controller

- Responsible for handling user interaction
- Takes care of all the logic in our application
- Processes HTTP requests
- Interacts with the model
- Interacts with the view
