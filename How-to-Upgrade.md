Upgrading from one OpenSupports version to another consists in replacing the current files on your server and sometimes run a `.sql` script to upgrade your MySQL database.

## Upgrade v4.0b => v4.1

1. Download the upgrade [zip file](https://github.com/opensupports/opensupports/releases/download/v4.1.0/opensupports_v4.1_update.zip)
2. Replace the OpenSupports files in your server with the content of the zip file.
3. Execute [this script](https://github.com/opensupports/opensupports/blob/master/version_upgrades/4.1.0/4.1.0.sql) in your OpenSupports' MySQL database.
4. Upgrade should be complete. If you had some issues, feel free to open a ticket here at github.

## Upgrade v4.1.0 -> v4.1.2

1. Download the upgrade [zip file](https://github.com/opensupports/opensupports/releases/download/v4.1.2/opensupports_v4.1.2_update.zip)
2. Replace the OpenSupports files in your server with the content of the zip file.
3. Set up the environment variables of the database and run 4.2.1.php
```
$ export MYSQL_SERVER=your_mysql_server
$ export MYSQL_DB=your_mysql_database
$ export MYSQL_USER=your_mysql_user
$ export MYSQL_PASSWORD=your_mysql_password
$ cd version_upgrades/4.1.2
$ php 4.1.2.php
```
4. After script in run, remove the folder `version_upgrades`
5. Upgrade should be complete. If you had some issues, feel free to open a ticket here at github.
