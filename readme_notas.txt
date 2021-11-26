20211124 
https://www.youtube.com/watch?v=WxjFFbHKQ_Y&list=PLOIvuivTitrphPX0X8gF3wUYOG6ogz7Ok&index=3&t=3s

composer create-proyect --prefer-dist laravel/laravel crudapi


.env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=crudapidb
DB_USERNAME=root
DB_PASSWORD=

config\database.php
 'mysql' => [
            'driver' => 'mysql',
            'url' => env('DATABASE_URL'),
            'host' => env('DB_HOST', '127.0.0.1'),
            'port' => env('DB_PORT', '3306'),
            'database' => env('DB_DATABASE', 'crudapidb'),
            'username' => env('DB_USERNAME', 'root'),
            'password' => env('DB_PASSWORD', ''),
            'unix_socket' => env('DB_SOCKET', ''),
            'charset' => 'utf8mb4',
            'collation' => 'utf8mb4_unicode_ci',
            'prefix' => '',
            'prefix_indexes' => true,
            'strict' => true,
            'engine' => null,
            'options' => extension_loaded('pdo_mysql') ? array_filter([
                PDO::MYSQL_ATTR_SSL_CA => env('MYSQL_ATTR_SSL_CA'),
            ]) : [],
        ],



php artisan make:model Product -m
php artisan migrate
php artisan make:controller api/ProductController --api
php artisan make:resource Product

siguiente paso hacer las api/routes
siguiente paso definir los metodos en ProductController
siguiente paso modificar el app\Providers\AppServiceProvider.php 