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
    mkdir wp-content

### Run

    docker-compose up
