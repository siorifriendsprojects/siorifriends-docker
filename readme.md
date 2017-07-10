# 栞フレンズ。
開発中。

# cloneした後やること
## Dockerの準備
./siorifriends/dockerディレクトリに移った後  
    $ docker-compose build  
    $ docker-compose run --rm composer install
## Laravelの準備
www-dataユーザとwww-dataグループに以下のディレクトリの読み書き権限を与える  
    /siorifriends/www/storage  
    /siorifriends/www/bootstrap/cache  

/siorifriends/wwwディレクトリに移った後にartisanでkey生成  
    $ cp -p .env.example .env  
    $ php artisan key:generate

# 起動方法
dockerディレクトリに移った後  
    $ docker-compose up -d
# 終了方法
dockerディレクトリで  
    $ docker-compose down

# dockerの設定のベースにさせてもらったもの

https://github.com/kotamat/laravel-docker-cluster
