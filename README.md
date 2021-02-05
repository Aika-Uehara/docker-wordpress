# Build

```=shell
docker-compose up -d
```

# MySQL Dump

```=Shell
docker exec -it db sh -c 'mysqldump `db_name` -u `db_user`  -p`db_pass` 2> /dev/null' > db_data/mysql.dump.sql
```

/db_data/配下に sql ファイルがダンプされる。（中身を書き換えた状態で保存することで、立ち上げ時のデータベースを維持できる。）
