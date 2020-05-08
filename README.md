# cc12-project.continuous-delivery-vue

## Change Log
- Added an .Env File. To locally connect to your database, please add a .env file to your workspace root folder.
- USER = "your user name without the quotes"
- PASSWORD = "your password without the quotes"

## API
**GET** `/api/locations` returns JSON data of locations
 
## Database Schema
**Table** `locations`
- id
- latitude
- longitude
- site_name
- name
- state
- city
- highway
- type
- highway_exit_num,
- street_address,
- telephone,
- fax


# HOW TO CHANGE MAX_CONNECTIONS
```
SHOW config_file;
vim  /usr/local/var/postgres/postgresql.conf
Change line: max_connections = 500           # (change requires restart)
```

# RESTART
```
brew services restart postgresql
```
