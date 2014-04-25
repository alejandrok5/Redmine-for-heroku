# Redmine-for-heroku

### Redmine version: 2.5.1 (2014-03-29)

## Redmine 

[Redmine](http://www.redmine.org/) is a flexible project management web application. Written using the Ruby on Rails framework, it is cross-platform and cross-database.

## Redmine-for-heroku

Redmine for heroku is a Redmine fork with settings for [heroku](https://www.heroku.com/‎), [amazon s3](http://aws.amazon.com/s3/) for upload files and [madrill](https://devcenter.heroku.com/articles/mandrill) for mail system.

## Installation
1. `bundle install --without development test`
2. `rake generate_secret_token`
3. `heroku create NAME_FOR_YOUR_APP`
4. `git push heroku master`
5. `heroku run rake db:migrate RAILS_ENV="production"`
6. `heroku addons:add mandrill`
7. `heroku config:add AWS_ACCESS_KEY_ID="XXXXXXXXX"`
8. `heroku config:add AWS_SECRET_ACCESS_KEY="XXXXXXXXXXXXXXXX"`
9. `heroku config:add S3_BUCKET_NAME="XXXXXXX"`
10. `heroku run RAILS_ENV=production rake redmine:load_default_data`

Blog [alejandrok5](http://alejandrok5.wordpress.com/)