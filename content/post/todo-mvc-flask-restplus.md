---
title: "A TodoMVC Application using Flask-RESTPlus"
date: 2018-03-31T08:06:18-07:00
lastmod: 2018-04-16T13:37:10-07:00
draft: false
keywords: [what]
description: ""
tags: [Python, Flask, Flask-RESTPlus, Flask-SQLAlchemy, PostgreSQL]
categories: [REST, Web Services]
author: "Rajesh Kommu"

comment: true
toc: true
autoCollapseToc: false
postMetaInFooter: true
hiddenFromHomePage: false
reward: false
mathjax: true
mathjaxEnableSingleDollar: true
---
> An introduction to building REST applications using Flask-RESTPlus, Flask-SQLAlchemy

In this blog post, I will go through the steps in building a simple ToDo application using
[Flask](http://flask.pocoo.org) and [Flask-RESTPlus](https://github.com/noirbizarre/flask-restplus). This
post is based on the [quickstart tutorial](http://flask-restplus.readthedocs.io/en/stable/quickstart.html)
except we will be plugging in to [PostgreSQL](http://postgresql.org) via 
[Flask-SQLAlchemy](http://flask-sqlalchemy.pocoo.org). Finally, the front end will be done in 
[Elm](http://elm-lang.org)

# Design
First let's look briefly at the design of the TodoMVC application.

## Static Structure 
![image](/static/todo-mvc-flask-restplus-todo-todolist.png)

The ```ToDoList``` class manages the CRUD operations for the application. 

A ```ToDo``` consists of

* ```description```: a string describing the task.
* ```status```: the status of the todo item --- ```inactive```, ```active```, ```completed```, ```overdue```
* ```due_datetime```: the due date and time for the todo item.

## Dynamic Structure
![image](/static/todo-mvc-flask-restplus-sequence.png)