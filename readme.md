# Flat File Flask Blog

[EXAMPLE SITE](https://fffb.ronaldlangeveld.com).

Last updated: 20 February 2018

I'm busy creating my own blog / cms with Flask and Python 3

My goal is to have it super basic and simple, very much with the likes of Pico or Jekyll, but with as little dependencies as possible, other than Flask and Python, so you can modify it as you wish as it is open source.

FFFB should:

 - Not contain a database.
 - Have no admin
 -	Be able to update easily through git push / pull without breaking the site.
 -	Make use of Jinja to simplify templating
 -	Post new content by only uploading .md files to your server (Markdown)

Basically, imagine a blog / cms using [Flasks "micro" philosophy](http://flask.pocoo.org/docs/0.12/foreword/#what-does-micro-mean).

## Getting started

It's highly recommended that you run this in a python virtual environment.

Clone this project into your dirctory of choice.

## Requirements
* `pip install flask`
* `pip install markdown2`
* `pip install Flask-Markdown`

Alternativaly 
* `pip install -r requirements.txt`

### Run locally
1. `export FLASK_APP=server.py`
2. `export FLASK_DEBUG=1`
3. `flask run`


## Writing a blog
### Setting parameters
To make use of the title, author and date tags, you must set them at the top of your `blog.md` file in order to parse them correctly. The parameter syntax must be exactly as follows:

``` 
<!-- VARS
##title: Your title ./title
##author: Author name ./author
##date: Date ./date
##image: your-featured-image.jpg ./image
./VARS -->
```

These parameters are called in the templating engine through `{{ post.title }}`, `{{ post.slug }}`, `{{ post.date }}`, `{{ post.image }}` or `{{ post.author }}`. 

#### Setting a featured image
To set a featured image you place your-picture.jpg in the `/static/featured-images/` folder. In your vars section you set `image` tag to `your-picture.jpg` and now you can call this image url with `{{ post.image }}`

#### Setting the slug
The slug of the blogs are now initialized by the filename of the post. So make sure these are meaningfull and unique. `/post/` will be prepended to your slug.



## Production

There's multiple ways you can deploy your flask blog.

[Heroku](https://progblog.io/How-to-deploy-a-Flask-App-to-Heroku/)

[Ubuntu VPS](https://www.digitalocean.com/community/tutorials/how-to-serve-flask-applications-with-gunicorn-and-nginx-on-ubuntu-16-04)

[PythonAnywhere](https://help.pythonanywhere.com/pages/Flask/)


