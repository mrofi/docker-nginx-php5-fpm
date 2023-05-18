# docker-nginx-php5-fpm
Dockerfile for nginx and php-fpm together.

This is a fork from [byrnedo/docker-nginx-php5-fpm](https://github.com/byrnedo/docker-nginx-php5-fpm)

Composer is also installed for convenience.

Doc root in default conf is `/usr/share/nginx/html` so mounting files there will get them served. 

## ENVs

- An `ERRORS` env can be set to toggle error reporting. Check out `cmd.sh` to see what happens. 
`ERRORS=1` will trigger error reporting, everything else keeps it turned off.

- A `PHP_FPM_POOL_CONF` env can be set with the contents of a conf which will be created as a file in `/etc/php/${IMAGE_PHP_VERSION/fpm/pool.d/z-www.conf`
