# laravel-commands
create project globally....!
composer create-project laravel/laravel project-name "10.*"

run project : 
php artisan serve

Create a new migration file :
php artisan make:migration create_users_table

Run migrations (apply to DB) :
php artisan migrate

Rollback last migration batch : 
php artisan migrate:rollback

Reset all migrations (drop all tables + run down methods) :
php artisan migrate:reset

Refresh migrations (rollback all + run again) :
php artisan migrate:refresh

To check the status of migrations in Laravel, use this command:
php artisan migrate:status

Create Model + Controller + Migration Together : 
php artisan make:model Product -mc

This will create:
     -> app/Models/Product.php → Model
       -> database/migrations/...create_products_table.php → Migration
         -> app/Http/Controllers/ProductController.php → Controller

Create Only Resource Controller
    -> If you already have a model and just need a controller :
      php artisan make:controller ProductController --resource

      This will create a controller with all 7 RESTful methods:
          index() → Show all
          create() → Show form
          store() → Save data
          show($id) → Show single
          edit($id) → Edit form
          update($id) → Update data
          destroy($id) → Delete data

debugging commands : 
  php artisan cache:clear → Clear cache
  php artisan config:clear → Clear config cache
  php artisan route:list → Show all registered routes (very useful in debugging)
  php artisan log:clear → Clear log files (Laravel 10+)





