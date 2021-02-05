WP Basic
=========

Extremely basic docker-compose setup for Wordpress.

**Includes:**

* docker-compose 3.3
* latest version of Wordpress
* mysql:latest
* data volume for db
* uploads.ini file to bump all the annoying default size restrictions
* mapping for wp-content

### Installation

Clone this repo. Create a wp-content folder

    git clone https://github.com/naglalakk/wp-basic && \
    cd wp-basic && \
    
    # Create folder and give permissions to user www-data
    mkdir wp-content && chown -R www-data:www-data wp-content

### Run

    docker-compose up

Wordpress runs on port 8080 by default. You can change this
in the docker-compose file under wordpress -> ports.


### Notes about .htaccess/apache2.conf

When setting up a staging environment to test out features or updates we often
have to make a copy of the entire site we are testing. Depending on the size
of the web this tends to be tedious when it contains a lot of media uploads.
The default settings in this repo is to include a apache2.conf (allows
overwriting the .htaccess file) and a .htaccess file which will overwrite the
default .htaccess provided with the docker image. 
If you don't prefer this behaviour simply remove the last two lines in
wordpress:volumes that map .htaccess/apache2.conf into the container. 
