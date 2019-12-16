# Koistore

Online-store with Stripe that facilitate online transactions of koi(s) and services through means of the transfer of information and funds over the Internet.

![Home Page](https://user-images.githubusercontent.com/52310638/197668400-6d03cd94-157d-4b77-85f3-1d791c97a0d7.png?raw=true)

![Featured Products](https://user-images.githubusercontent.com/52310638/197669076-d4a30c4f-f583-4afd-a4e9-affa28392667.png)

![Featured Previews](https://user-images.githubusercontent.com/52310638/197669190-3be580f8-b47d-4e45-9afc-7a27be5b147d.png)

![Footer Image](https://user-images.githubusercontent.com/52310638/197669364-4ca757d2-49fe-4005-b2fa-dc76f137e35a.png)

## Fullstack Technologies:
- SPA
- Vue2 (vue-cli)
- Laravel 6
- Stripe API
- Passport
- Mysql

## Configure Frontend:

- install dependencies

  navigate to **frontend/** open terminal and run :

  `npm install`

- setup backend url

  1.  Navigate and open **frontend/src/store/index.js**

  2.  Set backend-api url.

          eg. axios.defaults.baseURL = "http://localhost:8000/public/api/";

- add stripe publish_key

  1.  Navigate and open **frontend/src/views/CheckoutStripe.vue**

  2.  Set Stripe publish key.(line 84)

          eg.
          let stripe = Stripe(`pk_test_7nk...`)

### Initialize Frontend

- run to serve

  `npm run serve`

## Configure Backend:

- requirements:

  1. Php Composer
  2. Mysql Server

- add Database info and Stripe Info

  Navigate **backend/**:

  `Copy .env.example as .env`

  add database info:

  ```
  DB_CONNECTION=mysql
  DB_HOST=127.0.0.1
  DB_PORT=3306
  DB_DATABASE=database_name
  DB_USERNAME=root
  DB_PASSWORD=database_password
  ```

  add Stripe secret_key

  ```
  STRIPE_SK='secret_key'
  ```

Navigate **backend/** open terminal and run:

- install dependencies:

  `composer install`

- add database migrations

  `php artisan migrate`

- Add database dummies

  `php artisan db:seed`

- Install Laravel Passport

  `php artisan passport:install`

- generate key

  `php artisan key:generate`

### Initialize backend

`php artisan serve`
