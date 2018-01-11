Upgrading from one OpenSupports version to another consists in replacing the current files on your server and sometimes run a `.sql` script to upgrade your MySQL database.

## Upgrade v4.0b => v4.1

1. Download the upgrade [zip file](https://github.com/opensupports/opensupports/releases/download/v4.1.0/opensupports_v4.1_update.zip)
2. Put your system in maintenance (no necessary, but recommended, you can do it in the admin panel).
3. Replace the OpenSupports files in your server with the content of the zip file.
4. Execute [this script](https://github.com/opensupports/opensupports/blob/master/version_upgrades/4.1.0/4.1.0.sql) in your OpenSupports' MySQL database.
5. Upgrade should be complete. If you had some issues, feel free to open a ticket here at github.