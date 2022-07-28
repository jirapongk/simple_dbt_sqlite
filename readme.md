#
```
docker-compose up -d dbt-console
```

```
docker exec -it dbt_console /bin/bash
```

```
#rebuild
sudo docker-compose stop dbt_console # stop if running
sudo docker-compose rm -f dbt_console # remove without confirmation
sudo docker-compose build dbt_console # build
sudo docker-compose up -d dbt_console # create and start in background
```

```
Attach Shell
    docker exec -it 639af51563bbb2a6677500b948f1048e03727c63f440274a076541485ae56eba bash
dbt init simple_dbt_sqlite
```