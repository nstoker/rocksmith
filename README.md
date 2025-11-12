# README

Still trying to get Docker to run in a stable form. Based on notes by [nickjj's Docker Rails Examples](https://github.com/nickjj/docker-rails-example/tree/main). All the good stuff is from his repo, the errors are all my own work.

Look at [this](https://www.youtube.com/watch?v=nKiZz8TNHuU)

Stuck with the 

`./bin/run rails db:setup`

```
There is an issue connecting with your hostname: db.
Please check your database configuration and ensure there is a valid connection to your database.
Extracted source (around line #67):
     
    raise ActiveRecord::DatabaseConnectionError.username_error(conn_params[:user])
  elsif conn_params && conn_params[:host] && error.message.include?(conn_params[:host])
    raise ActiveRecord::DatabaseConnectionError.hostname_error(conn_params[:host])
  else
    raise ActiveRecord::ConnectionNotEstablished, error.message




Caused by:
PG::ConnectionBad: could not translate host name "db" to address: Temporary failure in name resolution (PG::ConnectionBad) ???

```

`