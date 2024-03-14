<h1 align="center">Laravel + Vue  Admin Panel</h1>
<h3 align="center">Vue + Tailwind CSS admin panel for Laravel projects.</h3>

## Built with

-   [Laravel 11](https://github.com/laravel/framework)
-   [Laravel Breeze](https://github.com/laravel/breeze)
-   [Vue 3](https://vuejs.org/)
-   [Tailwind CSS](https://tailwindcss.com/)
-   [Inertiajs](https://inertiajs.com/)

## Installation

### With Docker Desktop

-   To get started, you need to install [Docker Desktop](https://www.docker.com/products/docker-desktop).
-   You may run the following command in your terminal
-   Windows open WSL2 Linux terminal. [Docker Desktop WSL 2 backend](https://docs.docker.com/desktop/windows/wsl/)
-   `docker run --rm -v "$(pwd)":/opt -w /opt laravelsail/php83-composer:latest bash -c "composer create-project balajidharma/laravel-vue-admin-panel admin-app && cd admin-app && php artisan sail:install --with=mysql,redis,meilisearch,mailpit,selenium"`
-   `cd admin-app`
-   `./vendor/bin/sail pull mysql redis meilisearch mailpit selenium`
-   `./vendor/bin/sail build`
-   `./vendor/bin/sail up`
-   `./vendor/bin/sail npm install`
-   `./vendor/bin/sail npm run dev`
-   `./vendor/bin/sail artisan vendor:publish --tag=admin-core`
-   `./vendor/bin/sail artisan migrate --seed --seeder=AdminCoreSeeder`
-   Now open http://localhost/

### Without Docker Desktop

-   To get started, you need to install [PHP Composer](https://getcomposer.org/).
-   `composer create-project balajidharma/laravel-vue-admin-panel admin-app`
-   `cd admin-app`
-   Create a new MYSQL database and update database details in `.env` file
-   `php artisan vendor:publish --tag=admin-core`
-   `php artisan migrate --seed --seeder=AdminCoreSeeder`
-   `npm install`
-   `npm run dev`
-   `php artisan serve`
-   Now open http://localhost:8000/

###### Super Admin Login

-   Email - superadmin@example.com
-   Password - password

#### Admin Configuration:

To change the Admin Prefix, change `prefix` on `config/admin.php` or add the `ADMIN_PREFIX` on env

```php
'prefix' => env('ADMIN_PREFIX', 'admin'),
```

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
