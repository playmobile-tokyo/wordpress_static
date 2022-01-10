# 管理画面
http://localhost:8001/wp-admin

# ID/PW
test/xxxxxxx

# db
```
docker-compose exec db sh
mysql -u exampleuser -p examplepass

use database exampledb;
```

## WordPress アドレス (URL)を間違って更新したら
```
SELECT option_value FROM wp_options WHERE option_name = 'siteurl';
UPDATE wp_options SET option_value='http://localhost' WHERE option_name = 'siteurl';
```

# nginx wordpress
```
docker-compose exec nginx sh
docker-compose exec wordpress sh
```

# Simply Static

```
docker-compose up -f docker-compose_static.yml
```

WordPress が 192.168.10.3 から自分自身にリクエストを行うことができるか確認します	Not a valid url.
サイトアドレス (URL)	http://nginx

http://nginx としてホストOSからアクセスできるようにする
```
vi /etc/hosts

127.0.0.1 nginx
```

static 生成させてnginxでアクセス
http://nginx/archives/1

# Cocoon

