
[Heroku Offline](https://devcenter.heroku.com/articles/application-offline)

Run migration on heroku <br>
`heroku run rake --trace db:migrate --app name-of-your-app`

Restart app on heroku <br>
`heroku restart --app name-of-your-app`

Add remote for existing repo
`git remote add heroku git@heroku.com:project.git`

Heroku app page won't load
* [Make sure a root route is configure for the app](http://stackoverflow.com/questions/22026492/heroku-rails-setup-the-page-you-were-looking-for-doesnt-exist)
