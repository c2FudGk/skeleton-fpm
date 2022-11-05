
## setup
- docker-compose up -d
- docker exec -it container_php_fpm bash
- composer install

## Run tests
- vendor/phpunit/phpunit/phpunit tests/
