```
Reference : https://github.com/dbt-labs/jaffle_shop
```

```
docker-compose up -d dbt-console
```

```
docker exec -it dbt_console /bin/bash
```

```
#rebuild
docker-compose stop dbt-console # stop if running
docker-compose rm -f dbt-console # remove without confirmation
docker-compose build dbt-console # build
docker-compose up -d dbt-console # create and start in background
```

```
1. Attach Shell
    docker exec -it 639af51563bbb2a6677500b948f1048e03727c63f440274a076541485ae56eba bash
2. สร้างโปรเจค dbt
    dbt init simple_dbt_sqlite
3. โหลดข้อมูลโดยใช้ Seeds
    cd simple_dbt_sqlite
    dbt seed --profile simple_dbt_sqlite
    dbt seed --full-refresh --profile simple_dbt_sqlite
4. run model
    dbt run --model staging.jaffle_shop
    dbt run --model marts.jaffle_shop
```