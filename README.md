# Build

`.env.sample` をコピーし、 `.env `に書き換えた上で値を入れる。

```
WORDPRESS_DB_USER=hoge
WORDPRESS_DB_PASSWORD=hoge

MYSQL_ROOT_PASSWORD=hoge
MYSQL_DATABASE=hoge
MYSQL_USER=hoge
MYSQL_PASSWORD=hoge
```

```=shell
docker-compose up -d
```

立ち上げが正常に完了したら下記リンクで開く

wordpress : `http://localhost:8000`  
phpmyadmin : `http://localhost:8080`

# MySQL Dump

```=Shell
docker exec -it db sh -c 'mysqldump `db_name` -u `db_user`  -p`db_pass` 2> /dev/null' > db_data/mysql.dump.sql
```

/db_data/配下に sql ファイルがダンプされる。（中身を書き換えた状態で保存することで、立ち上げ時のデータベースを維持できる。）
