Hypothesis Wordpress Theme
==========================

Our own shiny custom theme.

Installation
------------

This is just a wordpress theme, so first you'll need to actully get Wordpress
up and running. You'll need MySQL, PHP 5.4.x and latest Nodejs. Download the
latest Wordpress bundle from:

http://wordpress.org/download/

Unzip the bundle into a directory then cd into the theme directory.

    $ cd wp-content/themes

Clone the repo:

    $ git@github.com:hypothesis/wordpress-theme-hypothesis.git

Install the required dependencies:

    $ npm install

Build the assets:

    $ make build

Then to run Wordpress ensure MySQL is running and cd back into the root
directory. Use the following instructions to allow Wordpress to be run using
the built in PHP server.

http://ripeworks.com/run-wordpress-locally-using-phps-buily-in-web-server/

Then starting the server should be as simple as:

    $ php -S localhost:9393 -t /path/to/wordpress router.php

Visit http://localhost:9393 in your browser and follow the installation
instructions. Once Wordpress is installed, you just need to change your theme
in the admin panel to use the hypothetheme.

To upload to WordPress, first build a zip file:

    $ make zip

Then upload the zip file to WordPress as usual.

IcoMoon Fonts
-------------

The homepage.scss uses fonts from IcoMoon directly embedded in the stylesheet.
If additonal icons need to be added then visit https://icomoon.io/app/.

And select the projects icon in the top right (it looks like a stack of paper).
From here select "Import project" and choose the icomoon-selection.json file.

Once new icons have been added, update the stylesheet with the new font and
update the icomoon-selection.json file (it will be called selection.json in
the downloaded font bundle).