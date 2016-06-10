# Someline Starter PHP Framework

Someline Starter is a framework for quick building Web Apps and Restful APIs, with modern PHP design pattern foundation, which is built on top of popular Laravel 5 framework, Vue.js, Restful API, Repository Design, OAuth2, JWT, Unit Tests, isolated front-end and back-end layer.

## Someline Starter is born for two reasons:

1. Quick application or Restful API starter without the need to build from scratch using Laravel.

2. Introduce modern design pattern, which have a better foundation when starting, for PHP projects.

## See In Action

##### [Demo](http://starter.someline.com/) 

Email: libern@someline.com 

Password: Abc12345

## Framework Overview

Someline Starter is suitable for Restful API oriented projects.

The Restful APIs as a backend layer which provide simple unified interfaces for frontend: Web and Mobile apps.

It utilized both OAuth2 and JWT for authentication purpose and protecting resources.

For Web frontend: `JWT` is used.

For Mobile frontend or third-party: `OAuth2` is used.

It also provides Unit Tests for API testing and framework testing.

It is shipped with Angulr Theme and features in every part that you can easily reference.

It is fully utilised Repository Design pattern.

## Out-of-box Components

##### If you are not familiar with any of these packages, you are recommended to get to know them as they are really helpful when you needed. 

*Framework*
- Laravel 5.2 [laravel/framework](https://github.com/laravel/framework)
- Laravel IDE Helper [barryvdh/laravel-ide-helper](https://github.com/barryvdh/laravel-ide-helper)
- Clockwork [itsgoingd/clockwork](https://github.com/itsgoingd/clockwork)

*Foundation*
- Redis [predis/predis](https://github.com/nrk/predis)
- GuzzleHTTP [guzzlehttp/guzzle](https://github.com/guzzle/guzzle)
- HTTP Status [lukasoppermann/http-status](https://github.com/lukasoppermann/http-status)

*Core*
- Restful API [dingo/api](https://github.com/dingo/api)
- L5 Repostory [prettus/l5-repository](https://github.com/andersao/l5-repository)
- Fractal [thephpleague/fractal](https://github.com/thephpleague/fractal)
- Laravel Validation [prettus/laravel-validation](https://github.com/andersao/laravel-validator)
- Intervention Image [intervention/image](http://image.intervention.io/)
- Intervention Image Cache [intervention/imagecache](https://github.com/Intervention/imagecache)
- Image Validator [cviebrock/image-validator](https://github.com/cviebrock/image-validator)

*Authentication*
- OAuth2 Server [lucadegasperi/oauth2-server-laravel](https://github.com/lucadegasperi/oauth2-server-laravel)
- JWT Auth [tymon/jwt-auth](https://github.com/tymondesigns/jwt-auth)

*Theme*
- Angulr theme with Bootstrap and jQuery support. For Demo: [Angular version](http://flatfull.com/themes/angulr/angular/#/app/dashboard-v1) and [HTML version](http://flatfull.com/themes/angulr/html/).
  
  *Please [buy a license](http://themeforest.net/item/angulr-bootstrap-admin-web-app-with-angularjs/8437259?ref=Flatfull) if you use this in your project.*

*Frontend*
- [Vue.js](https://vuejs.org/) Reactive Components for Modern Web Interfaces

## Get Started

You can get started from either A or B option:

### A. Fork Repository

`Fork this repository` and `clone` to your working folder. 

After forked:

```
git clone https://github.com/username/someline-starter
```

Note: Change `https://github.com/username/someline-starter` to your own cloned git repository address.

### B. Manually add to another repository

Clone this project to your working folder and open the directory:

```
git clone https://github.com/libern/someline-starter
```

#### B.1. Add to another Git Repository

Change `https://github.com/username/repository-name.git` to your own git repository address.

```
git remote remove origin
git remote add origin https://github.com/username/repository-name.git
git push -u origin master
```

## Installation

### Development Requirements

- PHP: >=7.0
- MySQL: >=5.7
- Laravel 5: https://laravel.com/docs/5.2/installation
- NodeJS: https://nodejs.org/
- Bower: https://bower.io/
- SQLite extention

### Install Essentials

Open `someline-starter` folder

```
cd someline-starter
```

*All these commands should be executed under the root of someline-starter project*

Install composer dependencies
```
composer install
```

Install npm dependencies
```
npm install
```

Install bower dependencies
```
bower install
```

Set-up Laravel, after these commands, please change `.env` file for your own environment settings
```
sudo cp .env.example .env
sudo chmod -R 777 storage
sudo chmod -R 777 bootstrap/cache
php artisan key:generate
php artisan jwt:generate
```

### Database & Seeding

You need to create a Database e.g. `someline_starter` with Encoding `utf8mb4` and Collation `utf8mb4_unicode_ci`.

Change database config in `.env` file to the match the database that your just created.

After having database configuration setup, you can now do migrations and seeding.

```
php artisan migrate

php artisan db:seed
```

### Ready to go

Until this point, you should be able to visit the home page. 

For example, if you have set the domain: `http://someline-starter.app/`.

Just visit: http://someline-starter.app/

It should prompt you for login, use:

```
libern@someline.com
Abc12345
```

You are free to change the seeding account information from the file: `database/seeds/UsersTableSeeder.php`

You are done. Yeah!

Explore and start to build on top of it.

## Development Process and Flow

### Essential Knowledge

You will need to know, read and understand fowllowing before you can start build on top of these.

- [ ] [Laravel Docs](https://laravel.com/docs/5.2/)
- [ ] [Restful API Best Practise](http://blog.mwaysolutions.com/2014/06/05/10-best-practices-for-better-restful-api/)
- [ ] [dingo/api Guide](https://github.com/dingo/api/wiki)
- [ ] [Repository Pattern](https://bosnadev.com/2015/03/07/using-repository-pattern-in-laravel-5/?utm_source=prettus-l5-repository&utm_medium=readme&utm_campaign=prettus-l5-repository)
- [ ] [Repository Usage](https://github.com/andersao/l5-repository#usage)
- [ ] [Vue.js Guide](https://vuejs.org/guide/)

We recommend use [PHPStorm IDE](https://www.jetbrains.com/phpstorm/) to build and develop your projects.

#### Namespace

The dafault namespace for `app/` folder is `Someline`.

It is NOT recommended to change the namespace, if you are not familiar with namepsace of Someline Starter as the `Someline` namespace is used heavily within whole project. 

However, you can still change it if you know how what you are doing, because some namespaces required manually changing. 

To change namespace to your preference:
```
php artisan app:namespace YourApp
```

#### BaseClass

In order to ultise all features provided by Someline Starter, you should extended the Class from BaseClass (if there has one), e.g. `BasePresenter`, `BaseController`, etc. 

#### Models

All models are located under `app/Models/` folder.

`User` Model under folder `app/Models/Foundation/` is created by default with primary key `user_id`, you should not change this class heavily because it is used almost everywhere within whole project. You can use global function `auth_user()` to access currently logged in user.

Every model should extend `Someline/Models/BaseModel` which has a observer `Someline/Observers/BaseModelObserver` that you can ultilise all model events within the Model, e.g. `onCreating`, `onCreated`, `onUpdating`, `onDeleting`, etc.

When creating new model, you should do it using command to auto generate realted Repository classes.

```
php artisan make:entity Post
```

#### Web Http

All Web related files are located under `app/Http/` folder.

Web Routes are defined in file `app/Http/routes.php`

Web Controllers are defined in folder `app/Http/Controllers/`

#### Restful API

All API related files are located under `app/Api/` folder.

API Routes are defined in file `app/Api/routes.php`

API Controllers are defined in folder `app/Api/Controllers/`

When you create APIs, you need to test them before you can use it. You should test all APIs using Unit Tests provided or create new Unit Tests. Not recommended to test using Browser or Postman, etc. 

#### Repository Pattern

All repository related files are located under `app/` with specific types as parent folders.

Repositories: `app/Repositories/`

Repositories Eloquent: `app/Repositories/Eloquent/`

Repositories Interface: `app/Repositories/Interfaces/`

Repositories Criteria: `app/Repositories/Criteria/`

Presenters: `app/Presenters/`

Transformers: `app/Transformers/`

Validators: `app/Validators/`

#### Resouces

Angulr Styles and Scripts: `resources/assets/angulr/`

Angulr with Blade views: `resources/views/angulr/`

Vuejs: `resources/assets/js/vue/`

Less styles: `resources/assets/less/app.less`

When made changes in scripts, styles, you will need to run the command.

In development, run:
```
npm run-script dev
```

In production, run:
```
npm run-script prod
```

When you changed theme files, run:
```
npm run-script theme
```

#### API and Unit Tests

Unit Tests: `tests/`

API Unit Tests: `tests/Api/`

#### Debug and Clockwork

View all requests and request information from file `storage/clockwork.sqlite`

#### Database

##### We recommend to use migrations for database structure and seeding. 

Directly changing from database or not follow migrations is strongly NOT recommended.

##### Flow of creating database migrations:

1. Create a migration file (Auto generated when use `php artisan make:entity`), under folder `database/migrations/`

2. Add essential columns to migration file:

You are recommended to use `tablename_id` format as primary incremental key, for example, for table `posts`, you need to use `post_id`, and when this become a foreign key, you should keep the same name in other table `post_id`.
```
$table->increments('post_id');
```

The following columns are always required by `BaseModel`:
```
$table->unsignedInteger('user_id')->index();

$table->unsignedInteger('created_by')->nullable();
$table->timestamp('created_at')->nullable();
$table->ipAddress('created_ip')->nullable();
$table->unsignedInteger('updated_by')->nullable();
$table->timestamp('updated_at')->nullable();
$table->ipAddress('updated_ip')->nullable();
```

And remove timestamps():
```
// $table->timestamps();
```

3. Add factory support, under file `database/factories/ModelFactory.php`

4. Create seeding support, under folder `database/seeds/`

##### Refresh Database Migrations and Seeding

When you added or changed to migration files or seedings, or you just simply want to refresh everything in database:

```
php artisan db:refresh --seed
```


## License

The Someline Starter framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
