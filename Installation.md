The installation of OpenSupports is very simple to do. You only need a web server that supports PHP and MySQL.  It generally works with most shared hosting providers.

----------


Server Requirements
-------------
To install OpenSupports you need to support the following: 

* PHP 5.6+
* MySQL 4.1+
* PDO Extension
* Apache 2.4+

Download installation files
-------------

1. The first thing you have to do is to download the zip file from http://www.opensupports.com/download/ which has the latest stable version of OpenSupports.
2. Unzip the package in a folder of your server, for example: `yourwebsite.com/support`
3. Go to `yourwebsite.com/support` (or the place where you extracted the file) and it should take you to the installation wizard.

Using the installation wizard
-------------------
The installation wizard will assist you to install and configure OpenSupports in your server.

![installation gif](http://www.opensupports.com/gifs/install1.gif)

#### 1. Select Language
You have to first select your language of preference for the installation and the system in general.
It can be English, Spanish, German, French, Portuguese, Japanese, Chinese, Russian, Turkish or Hindi.

#### 2. Server Requirements
In this step, the server requirements will be checked. If everything looks fine, you are able to proceed with the installation. The requirements are the mentioned above and some write permission for some files and folders.

#### 3. Database configuration
Here you have to provide the information for your MySQL database. The MySQL server, generally just `localhost`, an user and password and the database name (it will try to create it automatically if it is left empty)

![installation gif](http://www.opensupports.com/gifs/install2.gif)

#### 4. User System
Select your preferences for the user system. Determine if you want users to register in order to create tickets or not. You can also disable registration if you want (users can be created by other ways).

#### 5. Admin Setup
Put the email, password and name of the master administrator. This account will have access to all the system configuration.

#### 6. Completed
Once the installation is completed, you will be redirected to the admin login. Place go to Settings to change the rest of the configuration.

> **Remember**
> To access to the admin panel you have to go to `yourwebsite.com/support/admin` and use your admin credentials.

Manual installation
-------------
If you want to do a manual installation, you can follow the next steps:

1. Make sure to have the `server/` folder where you want to have the backend of the system.

2. Do a request to the path `/system/init-database` and pass the database values you need. You can avoid this if you want by creating a file called `config.php` with the database server information.

3. Do a request to the path `/system/init-settings` and pass the required parameters. This path will set the default values for the system.

4. Do a request to the path `/system/init-admin` and pass the values for the initial admin account.

> **Config.php content**
> The file must define 4 constants: MYSQL_HOST, MYSQL_DATABASE, MYSQL_USER and MYSQL_PASSWORD. This constants will be used by OpenSupports to connect to your database. 
> For example:
> 
    <?php
     define('MYSQL_HOST', 'localhost');
	 define('MYSQL_USER', 'root');
 	 define('MYSQL_PASSWORD', 'some_password');
 	 define('MYSQL_DATABASE', 'support');


If you want to avoid the use of PHP in the frontend side, or you have the backend located in another folder or server. 

When you unpackage the system files without the `server/` folder, make sure to replace the default file `index.php` with the special version of [index.html](https://github.com/opensupports/opensupports/blob/master/client/src/index.html) and create a [config.js](https://github.com/opensupports/opensupports/blob/master/client/src/config.js) file. So the frontend knows where does it have to make the api requests.
Also make sure that you have the proper configuration for .htaccess if you're using apache to server the frontend.
