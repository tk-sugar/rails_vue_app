`docker-compose build`  
`docker-compose run --rm web /bin/bash`  

# In Container
## new project
`rails new . --webpack=vue -f -d postgresql`  

## Rails
`docker-compose run web rails new . --force --database=postgres --webpack=vue --skip-coffee --skip-test`  
`docker-compose run --rm web bundle install`  

## DB
`docker-compose run --rm web rails db:create`  
`docker-compose run --rm web rails db:migrate`  
`docker-compose run --rm web rails db:migrate:reset`  

## pry
`docker attach "container_name"`

## if your app doesn't work, exec following cmd on your app dir
`rm -f app/tmp/pids/server.pid`

## Reference
https://qiita.com/asapon_rb/items/507558aad52dc7dd2b32