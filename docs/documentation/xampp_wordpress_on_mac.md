1. Download XAMPP dmg from https://sourceforge.net/projects/xampp/files/XAMPP%20Mac%20OS%20X/8.2.4/xampp-osx-8.2.4-0-installer.dmg/download
2. Download Wordpress zip from https://wordpress.org/latest.zip
3. Run XAMPP dmg and install it.
4. Unzip the wordpress zip.
5. Open XAMPP manager.
6. Open Application Folder.
7. Move the wordpress unzipped folder to htdocs in XAMPP's application folder.
8. Edit the wp-config-sample.php file and set the following configs:
    - DB_NAME
    - DB_USER
    - and more to according to your needs.
9. Restart all services in XAMPP.
10. Navigate to phpmyadmin at top right in 127.0.0.1 or localhost.
11. Set your DB_NAME after navigating to database option.
12. Go to 127.0.0.1/<wordpress_unzipped_folder_name>, in my case it is 127.0.0.1/wordpress.
13. Set your Wordpress Account.
14. TANTANAAAA! All Set!

## FTP SETUP

1. File Permissions

execute these lines first:

```bash
chmod 777 /Applications/XAMPP/xamppfiles/htdocs/wordpress/
chmod 777 /Applications/XAMPP/xamppfiles/htdocs/wordpress/wp-content/uploads/
chmod 777 /Applications/XAMPP/xamppfiles/htdocs/wordpress/wp-content/plugins/
chmod 777 /Applications/XAMPP/xamppfiles/htdocs/wordpress/wp-content/themes/
```

2. Wordpress Config:

Add these to wp-config.php:

/** Add here*/
define('FS_METHOD','direct');
define("FTP_HOST", "localhost");
define("FTP_USER", “my_wordpress_user”);
define("FTP_PASS", “password”);
/** To here*/

where my_wordpress_user and password are the ones used in wordpress.
