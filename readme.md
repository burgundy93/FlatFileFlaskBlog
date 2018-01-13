# Flat File Flask Blog

Last updated: 13 January 2018

I'm busy creating my own blog / cms with Flask.

My goal is to have it super basic and simple, very much with the likes of Pico or Jekyll, but with as little dependencies as possible, other than Flask and Django, so you can modify it as you wish as it is open source.

FFFB should:

 - Not contain a database.
 - No admin
 -	Not store any critical info like username/passwords/etc.
 -	Be able to update easily through git push / pull without breaking the site.
 -	Make use of Jinja to simplify templating
 -	Post a new content using using .md files (Markdown)

Basically, imagine a blog / cms using [Flasks "micro" philosophy](http://flask.pocoo.org/docs/0.12/foreword/#what-does-micro-mean).

