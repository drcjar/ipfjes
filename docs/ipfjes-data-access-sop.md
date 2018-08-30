# IPFJES data access sop

## Data access via the application (normal user)

1. Obtain an application user name and password (only central research team Carl, Rupa, Paul, Sara are authorised)

2. Use user name and passord to access IPFJES application on desktop computer in G39 (or over local network)

## Data access via the database dump (data analyst / advanced user)

1. Obtain a linux user name and password (only central research team Carl, Rupa, Paul, Sara are authorised) for a desktop computer in G39

2. Open a terminal (press "ctrl-shift-t")

3. Make a new database to restore the database dump to. Run the command "sudo -u postgres psql" in the terminal to start a psql session. Run the following commands in the psql session

CREATE DATABASE NAME_OF_DATA_BASE_YOU_WOULD_LIKE;

CREATE USER YOUR_USER_NAME;
																																																																																																																																																																																																																																										
GRANT ALL PRIVILEGES ON NAME_OF_DATA_BASE_YOU_WOULD_LIKE TO YOUR_USER_NAME;

exit the psql session ("ctrl-d")

4. Load the database dump into the new database you just made. "sudo -u YOUR_USER_NAME psql -d NAME_OF_DATA_BASE_YOU_WOULD_LIKE -f back.sql.DD.MM.YY"

Note that DD.MM.YY must be complete with the day, month, and year of the database dump you wish to restore. Database dumps live in the sync folder. 

5. Use a client of your choice to access the postgres database. 

## Location of database dumps (backups)

Regular database dumps (backups) are securely made to the local computers in G39 and to a usb stick in a fireproof box.

## Support

A support contract is in place and our support contact is Mr Fred Kingham fredkingham@gmail.com 07843659855.
