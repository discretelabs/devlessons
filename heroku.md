
[Heroku Offline](https://devcenter.heroku.com/articles/application-offline)

#### Run migration on heroku <br>
`heroku run rake --trace db:migrate --app name-of-your-app`

#### Restart app on heroku <br>
`heroku restart --app name-of-your-app`

#### Add remote for existing repo
`git remote add heroku git@heroku.com:project.git`

#### Heroku app page won't load
* [Make sure a root route is configure for the app](http://stackoverflow.com/questions/22026492/heroku-rails-setup-the-page-you-were-looking-for-doesnt-exist)


#### Reset Heroku App Db <br>
Got this from [Stack Overflow](http://stackoverflow.com/questions/22043111/delete-and-redeploy-rails-app-to-heroku)
<br>
If you don't want to delete the entire application (*perhaps you want to keep your add-ons and other configuration the same*), you can reset the database and force update the code.<br>

* Deploy your new code, forcing the update by using the -f flag:
`git push heroku master -f` <br>

* Drop and recreate the database: 
`heroku pg:reset <DATABASE_URL>` <br>

* Migrate the fresh database:
`heroku run rake db:migrate` <br>
