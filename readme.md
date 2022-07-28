#
```
docker-compose up -d dbt-console
```

```
docker exec -it dbt_console /bin/bash
```

```
#rebuild
sudo docker-compose stop webserver # stop if running
sudo docker-compose rm -f webserver # remove without confirmation
sudo docker-compose build webserver # build
sudo docker-compose up -d webserver # create and start in background
```

```
docker exec -it 639af51563bbb2a6677500b948f1048e03727c63f440274a076541485ae56eba bash
dbt init simple_dbt_sqlite
```