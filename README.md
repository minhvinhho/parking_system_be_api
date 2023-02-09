# project setup
composer install || composer update
cp .env.example .env
php artisan key:generate
php artisan storage:link
php artisan migrate
php artisan db:seed
php artisan config:cache
php artisan cache:clear
composer dump-autoload