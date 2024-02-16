# Wordpress

* `curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar`
* `php wp-cli.phar --info`
* `chmod +x wp-cli.phar`
* `mv wp-cli.phar /usr/local/bin/wp`
* `wp --info`
* `wp cli update`


Install WordPress :
* `wp core download`
* `wp core config --dbname=mydbname --dbuser=mydbuser --dbpass=mydbpass --dbhost=localhost --dbprefix=whebfubwef_ --extra-php <<PHP
define( 'WP_DEBUG', true );
define( 'WP_DEBUG_LOG', true );
`
* `wp db create`
* `wp core install --url=http://siteurl.com --title=SiteTitle --admin_user=username --admin_password=mypassword --admin_email=my@email.com`


Core reinstall :
* `wp core download --skip-content --force`


Change url :
* `wp option update home 'http://example.com'`
* `wp option update siteurl 'http://example.com'`


Plugin :
* `wp plugin list`
* `wp plugin deactivate wordpress-seo`
* `wp plugin deactivate --all`
* `wp plugin update wordpress-seo`


Wordpress CLI :
* Verify Wordpress checksums : `wp core verify-checksums`
* Get Wordpress version : `wp core version`
* List users : `wp user list`
* List plugins : `wp plugin list`
* List posts : `wp post list`
* Config : `wp config list`
* List deleted posts : `wp post list --post_status=trash`
* Update uptions : `wp option update home 'http://example.com'`
* Search and replace in db : `wp search-replace 'example.dev' 'example.com' --skip-columns=guid`
* Theme install : `wp theme install twentytwentyone --activate`


