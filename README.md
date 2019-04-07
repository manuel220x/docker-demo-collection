#### Docker Demo Collection
This is a collection of Dockerfiles to be used for demo purposes, they are not in any way ready to be used in production. Images will also be available at docker hub for faster pickup and use. 

##### PHP

- Apline based
- Nginx (http port **80**)
- php7 (fpm, /run/php-fpm.sock)
- supervisord
- index.php & info.php under **/var/www/app/web/**

```
docker run -d -P manuel220/aplinephp
```
