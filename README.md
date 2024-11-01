# Database designer plugin for phpPgAdmin

I haven't fully tested it yet, but this fork works for PostgreSQL 17 and [phpPgAdmin fork by ReimuHakurei](https://github.com/ReimuHakurei/phpPgAdmin).

Here’s what I did to fix this plugin:

- Fixed some typos that caused the plugin not to run.
- Changed some queries regarding OIDs, since PostgreSQL 12+ doesn't support OIDs.
- Renamed Table.php to TableHeader.php to resolve conflicts with php/pear/Table.php.

Additional Feature:

- Capture diagram image.

How to operate this plugin is explained in this [video](https://www.youtube.com/watch?v=J9tIl3zB9Ro).

## Installation

1. You need a copy of the latest phpPgAdmin version on github.

2. Place this plugin as a subfolder of the directory plugins/ (The name "DBDesigner" must be preserved).

3. Go to the file sql/erdiagrams-pgsql and run the sql commands to create a the database responsible for storing the ER Diagrams.

4. Enable the plugin by adding and entry in the phpPgAdmin's file config/config.php.inc. It should look something like this: $conf['plugins'] = array('DBDesigner');

5. Navigate to the schema where you want to create the ER Diagram and you're done!.
