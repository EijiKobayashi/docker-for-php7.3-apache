# docker-for-apachedocker-for-php7.3-apache

- Apache
- PHP 7.3
- MySQL

## docker-compose ビルド

/docker/localhost ディレクトリに移動して

```
$ docker-compose build --no-cache
```

## docker-compose 起動

docker-compose up -d 実行後 http://localhost:3000/ でブラウズ

```
$ docker-compose up -d
```

> <strong>サブドメインに対応</strong>  
> /var/www/subdomain/ -> http://subdomain.localhost:3000/  
> ※ Firefox などのブラウザによっては /etc/hosts 設定が必要です！
>
> ```
> 127.0.0.1 subdomain.localhost
> ```

## docker-compose シャットダウン

```
$ docker-compose down
```

## ディレクトリ構成

```
├─ docker/
│  └─ パッケージ各種
│
├─ docker/（Dockerファイル一式）
│  ├─ localhost/
│  │  ├─ mysql/ (MySQL関連)
│  │  ├─ php-apache/ (Apache関連)
│  │  └─ phpmyadmin/ (PHPMyAdmin関連)
│  └─ docker-compose.yml
│
├─ localhost/（ビルド前のソース）
│  └─ var/
│      └─ www
│
└─ README.md
```
