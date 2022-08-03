---
title: "Intro to Flask (2)"
date: 2020-11-05T20:46:05Z
draft: false
tags: [web, flask, html]
author: Ziyi
---

Last week was my first meeting with Flask and pretty much the concept of web development, since it was at most "Heads up HTML" in the past. This week I will be dabbling a bit on basic Flask features and usages, templates, template inheritance and Bootstrap framework.

### Flask basics

Firstly, quoting flask website:
>A Flask application is an instance of the Flask class. Everything about the application, such as configuration and URLs, will be registered with this class.

So in order to do that, I'm also including a code snippet from the website to save time:

myapp/`__init__`.py
```
import os

from flask import Flask


def create_app(test_config=None):
    # create and configure the app
    app = Flask(__name__, instance_relative_config=True)
    app.config.from_mapping(
        SECRET_KEY='dev',
        DATABASE=os.path.join(app.instance_path, 'flaskr.sqlite'),
    )

    if test_config is None:
        # load the instance config, if it exists, when not testing
        app.config.from_pyfile('config.py', silent=True)
    else:
        # load the test config if passed in
        app.config.from_mapping(test_config)

    # ensure the instance folder exists
    try:
        os.makedirs(app.instance_path)
    except OSError:
        pass

    # a simple page that says hello
    @app.route('/hello')
    def hello():
        return 'Hello, World!'

    return app
```

So we can see that the file is in the '`__init__.py`', which prompts that this file contains the _application factory_ and will tell python to treat this folder as a package.

In the creation of the flask instance(the application factory), we used `__name__` for convenience, so that the app knows where to set up the path easily. We can also have a config.py file that stores the configuration settings if we are not passing them with the FLask function. 

Finally some copy-and-paste:
>os.makedirs() ensures that app.instance_path exists. Flask doesn’t create the instance folder automatically, but it needs to be created because your project will create the SQLite database file there.

>@app.route() creates a simple route so you can see the application working before getting into the rest of the tutorial. It creates a connection between the URL /hello and a function that returns a response, the string 'Hello, World!' in this case.

>app.config.from_mapping() sets some default configuration that the app will use:
>>SECRET_KEY is used by Flask and extensions to keep data safe. It’s set to 'dev' to provide a convenient value during development, but it should be overridden with a random value when deploying. <br><br>
>>DATABASE is the path where the SQLite database file will be saved. It’s under app.instance_path, which is the path that Flask has chosen for the instance folder. You’ll learn more about the database in the next section.





