
##### Dump heroku db into rails <br>
`pg_restore -O -d development_db_name db/database_dump_file.dump`


##### Remove twitter bootstrap
* `rake assets:clean`
* `rails destroy bootstrap:install`

##### Fix error after bundle update
CLIENT: 1.1.3, SERVER: 1.1.2
* spring stop
* stop rails server
* restart rails server
