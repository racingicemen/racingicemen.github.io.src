---
title: "A TodoMVC Application using Flask-RESTPlus"
date: 2018-03-31T08:06:18-07:00
lastmod: 2018-03-31T08:06:18-07:00
draft: true
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
[Flask-SQLAlchemy](http://flask-sqlalchemy.pocoo.org).

# Design
First let's look briefly at the design of the TodoMVC application.