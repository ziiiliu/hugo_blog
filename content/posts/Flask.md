---
title: "Intro to Flask (2)"
date: 2020-10-29T20:30:20Z
draft: false
author: Ziyi
---
So after delaying this website project for almost a year, I'm back online and will be producing weekly microblogs(stressful terms, sorry) on CS-related contents, as well as other random blogs about life. In the meantime I am still familiarising myself with Hugo, so don't be surprised if the structuring and themes get a bit whimsical - or actually I might just do it for fun :)))

## Flask and Django

Web develpment has not been my top priority, and it is only very recently(last two days) that I decided to start picking up Python web dev as a start. The two important and competing frameworks, Django and Flask, provide different features and functionalities for projects with different scales and goals. Apparently, Django is more fully equipped and all-rounded for different kinds of tasks, while Flask is more lightweight and flexible. This fundamental difference results in their divergence in application purposes: Django more apparopriate and usable with large projects which requires the full set of tool kit, while Flask with mid- and small-projects. 

And I, barely able to pull time to write blogs, certainly cannot afford to either build a large project in the coming future or learn something as heavy as Django for now, will focus more on learning some very basics of Flask to power my application-side web skills. Hopefully this would spark some more motivation of learning the theories soon outta me. 

_Aside: I have, however, seen a few comments saying that Hugo or the sort of stuff is the new trending, especially for blogs(static pages),but neither Flask nor Django stops there. And that's why I am going to explore a bit more. Nonetheless, I will keep my early stage focus on Hugo so that my blogs will, hopefully, look less like of a 1990s product.

## [Flask Basics](https://flask.palletsprojects.com/en/1.1.x/tutorial/deploy/)

As you see, this __Microblog__ has no intention in reinventing the tutorial once again when there's such a nice official tutorial and documentation. Rather, I will put the most useful tips/reminders/structures and some of the very essential codes and ideas here. So as to kick off the resuscitation of my long-ignored blogs, here's a snippet of the 'Hello world'-equivalent Flask code:

```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'
```

Alright, I'll pause here, and my next blog would feature the basics of Flask for a blog project. Until then!


