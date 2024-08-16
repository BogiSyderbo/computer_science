
# Just fucking work
```
sudo postgresql-setup --upgrade
```

```
sudo systemctl start postgresql
```
or
```
sudo systemctl restart postgresql
```

```
sudo systemctl status postgresql
```

# PSQL guide
```bash
sudo -u postgres psql
```


**Basic commands**:

*connect*
```
\c database_name
```

*list all databases*
```
\l
```

*list all table in database*
```
\dt
```

*describe table structure*
```
\d table_name
```

*quit*
```bash
\q
```

```bash
1016  sudo -u postgres psql                                                                            │ 14 # set your own database
 1017  psql -d bank24017 -U postgres -h127.0.0.1 -W -f shema.sql                                        │ 15 #db = "dbname='bank' user='postgres' host='127.0.0.1' password = 'UIS'"
 1018  sudo -u postgres psql                                                                            │ 16 db = "dbname='bank24017' user='postgres' host='127.0.0.1' password = '1234'"
 1019  psql template1                                                                                   │ 17 conn = psycopg2.connect(db)
 1020  psql -d bank24017 -U postgres -h127.0.0.1 -W -f shema.sql                                        │ 18
 1021  la                                                                                               │ 19 bcrypt = Bcrypt(app)
 1022  psql -d bank24017 -U postgres -h127.0.0.1 -W -f schema.sql                                       │ 20
 1023  psql -d bank24017 -U postgres -h127.0.0.1 -W -f schema_ins.sql                                   │ 21
 1024  psql -d bank24017 -U postgres -h127.0.0.1 -W -f schema_upd.sql                                   │ 22 login_manager = LoginManager(app)
 1025  psql -d bank24017 -U postgres -h127.0.0.1 -W -f sql_ddl/ddl-customers-001-add.sql                │ 23 login_manager.login_view = 'login'
 1026  cd ..                                                                                            │ 24 login_manager.login_message_category = 'info'
 1027  la                                                                                               │ 25
 1028  python3 run.py   
```

