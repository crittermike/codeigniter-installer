CodeIgniter Installer
======================

General Information
--------------------

CI Installer is a starting point for giving your downloadable CodeIgniter
application an installer.

If you're making a CI app that is designed to be downloaded and self-hosted,
CI Installer provides an easy way for the user to get the database structure and 
configuration in place.

NOTE: This is to be used as a starting point. You will have to customize it to 
make it work for your application, and you might have to dig into the code
a little bit. It's pretty simple, so if you have a basic understanding of PHP
you shouldn't have trouble.

General Instructions
---------------------

1. Download CI Installer (https://github.com/collb/codeigniter-installer/zipball/master), extract it, 
rename the folder to 'install' and put it in the root
directory of your CI install (next to /application folder).
2. Make an SQL dump of your desired database structure and intial data and paste 
it into assets/install.sql
3. Open up index.php and change "Your App" in the <title> to your app's name.
4. If you have .htaccess file in CodeIgniter root folder, change the line:
	RewriteCond $1 !^(index\.php|img|css|js|robots\.txt|favicon\.ico|update\.php|install\.php)
to:
	RewriteCond $1 !^(index\.php|img|css|js|install|robots\.txt|favicon\.ico|update\.php)
	
- In index.php, around line 37 change 'welcome' to the URL of the page
(in CodeIgniter) that you want the user to be redirected to after installing.
- Visit http://example.com/path/to/yourapp/install and see how it goes.

If you have problems or have recommendations, please file an issue at
https://github.com/collb/codeigniter-installer/issues
