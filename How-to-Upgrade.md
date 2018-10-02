Upgrading from one OpenSupports version to another consists in replacing the current files on your server and sometimes run a `.php` script to upgrade your MySQL database.

## Upgrade v4.0b -> v4.1
1. Do a database backup before upgrading for safety
2. Download the upgrade [zip file](https://github.com/opensupports/opensupports/releases/download/v4.1.0/opensupports_v4.1_update.zip)
3. Replace the OpenSupports files in your server with the content of the zip file.
4. Execute [this script](https://github.com/opensupports/opensupports/blob/master/version_upgrades/4.1.0/4.1.0.sql) in your OpenSupports' MySQL database.
5. Upgrade should be complete. If you had some issues, feel free to open a ticket here at github.

## Upgrade v4.1.1 -> v4.1.2

1. Do a database backup before upgrading for safety
2. Download the upgrade [zip file](https://github.com/opensupports/opensupports/releases/download/v4.1.2/opensupports_v4.1.2_update.zip)
3. Replace the OpenSupports files in your server with the content of the zip file.
4. Go to the folder `version_upgrades/4.1.3/` and run the script with `php 4.1.2.php`
5. After the script is done, remove the folder `version_upgrades`
6. Upgrade should be complete. If you had some issues, feel free to open a ticket here at github.


## Upgrade v4.1.2 -> v4.1.3

1. Do a database backup before upgrading for safety
2. Download the upgrade [zip file](https://github.com/opensupports/opensupports/releases/download/v4.1.3/opensupports_v4.1.3_update.zip)
3. Replace the OpenSupports files in your server with the content of the zip file.
4. Go to the folder `version_upgrades/4.1.3/` and run the script with `php 4.1.3.php`
5. After the script is done, remove the folder `version_upgrades`
6. Upgrade should be complete. If you had some issues, feel free to open a ticket here at github.

## Upgrade v4.1.3 -> v4.2.0

1. Do a database backup before upgrading for safety
2. Download the upgrade [zip file](https://github.com/opensupports/opensupports/releases/download/v4.2.0/opensupports_v4.2.0_update.zip)
3. Replace the OpenSupports files in your server with the content of the zip file.
4. Go to the folder `version_upgrades/4.2.0/` and run the script with `php 4.2.0.php`
5. After the script is done, remove the folder `version_upgrades`
6. Upgrade should be complete. If you had some issues, feel free to open a ticket here at github.

## Upgrade v4.2.0 -> v4.2.1 HOTFIX

1. Download the upgrade [zip file](https://github.com/opensupports/opensupports/releases/download/v4.2.1/opensupports_v4.2.1_update.zip)
2. Merge and replace the OpenSupports files in your server with the content of the zip file.
3. Upgrade should be complete. If you had some issues, feel free to open a ticket here at github.