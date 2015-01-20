
##### Dump heroku db into rails <br>
`pg_restore -O -d development_db_name db/database_dump_file.dump`


##### Remove twitter bootstrap
* `rake assets:clean`
* `rails destroy bootstrap:install`
