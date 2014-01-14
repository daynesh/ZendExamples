MyAlbum
=======

Introduction
------------
This is a simple application used to demonstrate the Zend PHP web framework.  It essentially provides the user with access to a list of music albums stored in a local MySQL database.  

It supports HTTP Requests on the following URL paths:

* GET /
* GET /album
* GET /album/add
* GET /album/edit/:id
* GET /album/delete/:id
* POST /album/add
* POST /album/edit/:id
* POST /album/delete/:id


Web Server Setup
----------------

### PHP CLI Server

The simplest way to get started if you are using PHP 5.4 or above is to start the internal PHP cli-server in the root directory:

    php -S localhost:8080 -t public

This will start the cli-server on port 8080, and bind it to localhost.

**Note: ** The built-in CLI server is *for development only*.

### Apache Setup

To setup apache, setup a virtual host to point to the public/ directory of the
project and you should be ready to go! It should look something like below:

    <VirtualHost *:80>
        ServerName zf2-tutorial.localhost
        DocumentRoot /path/to/zf2-tutorial/public
        SetEnv APPLICATION_ENV "development"
        <Directory /path/to/zf2-tutorial/public>
            DirectoryIndex index.php
            AllowOverride All
            Order allow,deny
            Allow from all
        </Directory>
    </VirtualHost>
