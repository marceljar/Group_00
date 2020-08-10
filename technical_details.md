## Back-End

The website is served by an [Apache 2.0](https://httpd.apache.org/) server, running on an Ubuntu 16.04 OS hosted by [Digital Ocean](https://www.digitalocean.com/). It uses a [Django](https://www.djangoproject.com/) framework which implements a model-template-view pattern that links together a number of Python scripts and a SQLite database, to render all pages transmitted to the end-user via HTTP. 

## Front-End

In its Front-End, the website uses [Bootstrap 3.3](https://getbootstrap.com/docs/3.3/) to create a responsive experience. Moreover, the [JQuery](https://jquery.com/) library,  which is required by this version of Bootstrap, is used to simplify the coding of number of AJAX calls. No other JavaScript libraries are used.

## Developing Tools

This website was developed using [Visual Studio Code](https://code.visualstudio.com/) with a Python and Remote-SSH extensions. [Postman](https://www.postman.com/) was used to test a number of HTTP requests in order to decouple back-end and front-end tasks.
