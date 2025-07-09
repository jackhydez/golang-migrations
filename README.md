# Project golang-migrations

create file for environment variables:
```
cp env-example.list .env
```

build and run all containers:
```
docker compose up -d db pgadmin
```

link on pgAdmin:
```
http://localhost:8080/login?next=/
```


### Регистрация сервера в pgAdmin после логина
После входа по email/паролю из .env, нужно добавить сервер вручную:
```
Клик по Servers → Register → Server...
```
На вкладке General:
```
имя (например, local-db).
```
На вкладке Connection:
```
Host name/address: db
Port: 5432
Maintenance DB: postgres или ваш DB_NAME
Username: из .env (DB_USER)
Password: из .env (DB_PASS)
Нажать Save — сервер появится в дереве, и можно работать
```

