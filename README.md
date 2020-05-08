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

**Table** `amenities`
- id
- location_id
- name

**Table** `restaurants`
- id
- location_id
- name


## Steps to Setting Local Database
If you have a truckstop database created already run the following:
1. Enter `psql` in your terminal
2. `drop database truckstop;`
3. `create database truckstop;`
4. `\c truckstop;`
5. `SHOW config_file;` will return the path to your config file. **Copy the path**
6. `\q` to exit PostgreSQL
7. `vim  [PASTE YOUR PATH THAT YOU COPIED]`
8. Locate `max_connections` in the file and change its value to **500**
9. Click esc and enter `:wq`
10. `brew services restart postgresql`
11. `psql`
12. Enter `SHOW max_connections;` and the value should be changed to **500**


## Connecting to Heroku Database
```
heroku pg:psql -a cc12-vue-project
```
