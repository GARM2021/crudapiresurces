20211124 
php artisan make:model Product -m
php artisan migrate
php artisan make:controller api/ProductController --api
php artisan make:resource Product

siguiente paso hacer las api/routes
siguiente paso definir los metodos en ProductController
siguiente paso modificar el app\Providers\AppServiceProvider.php 