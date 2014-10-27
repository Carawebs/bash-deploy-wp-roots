bash-deploy-wp-roots
====================

Automatically deploy a fresh local copy of WordPress with the Roots starter theme. For Ubuntu 14.04. Builds a database, clones the starter theme, sets up a fresh GitHub repo.

This script:

* Creates a new directory for a WordPress site in ```/var/www```.
* Creates a new WordPress test site, with a fresh database.
* Downloads, renames and activates the [Roots](https://github.com/roots/roots) theme.
* Sets up a new GitHub repo for the new theme (A GitHub personal token and SSH keys need to be in place)
* Downloads & activates the [Soil](https://github.com/roots/soil) plugin.
* Installs node & bower dependencies by running npm install.
* Requires [WP-CLI](http://wp-cli.org/).

Save this script as ```/usr/local/bin/roots-spin```.
Make it executable, then you can invoke it by typing "roots-spin" in the terminal.

NOTE: depending on your node setup, you may need to amend the ```setup_node ()``` function in this script.
See inline comments for more info.

Pull requests welcome!
