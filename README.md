Auto Deploy WordPress & Roots
====================

For a local Ubuntu 14.04 deverlopment enviropnment. This script automatically deploys a fresh local copy of WordPress with the Roots starter theme. Builds a new database, clones the Roots starter theme, copies Roots and sets up a newly renamed theme, installs node dependencies and sets up a fresh GitHub repo for your project.

Because the script is designed to quickly create a local development site, the database credentials aren't particularly secure - the db name is used as a "salt" for username & password. Please don't use the unedited script to generate a WordPress installation on a public facing server. It would be easy to amend this so that the user is prompted to enter secure db credentials.

Because you might copy the local database to a public server, you should enter a secure username & password for WordPress when prompted.

##What it Does##

* Creates a new directory for a WordPress site in ```/var/www```.
* Creates a new WordPress test site, with a fresh database.
* Downloads, renames and activates the [Roots](https://github.com/roots/roots) theme.
* Sets up a new GitHub repo for the new theme (A GitHub personal token and SSH keys need to be in place)
* Downloads & activates the [Soil](https://github.com/roots/soil) plugin.
* Installs node & bower dependencies by running npm install.
* Requires [WP-CLI](http://wp-cli.org/).

##How to Use##
Clone this script and save the ```roots-spin``` file as ```/usr/local/bin/roots-spin```.
Make it executable: ```sudo chmod +x /usr/local/bin/roots-spin```.
Run the script by entering "roots-spin" in the terminal.

NOTE: depending on your node setup, you may need to amend the ```setup_node ()``` function in this script.
See inline comments for more info.

Pull requests welcome!
