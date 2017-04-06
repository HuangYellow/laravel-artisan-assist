# Installation

As others package, use composer install this package. For example:

``` bash
$ composer require yellowhuang/laravel-artisan-assist
```

Secondly, you need to register service provider in `config/app.php`.

``` php
    'providers' => [
    ...
    /*
     * Package Service Providers...
     */
     Yellow\ArtisanAssist\ArtisanAssistServiceProvider::class,
    ...
```

Thirdly, Going to `app/Console/Kernel.php`, adding console command.

``` php
protected $commands = [
        \Yellow\ArtisanAssist\Commands\makeService::class,
        \Yellow\ArtisanAssist\Commands\makeRepository::class,
        \Yellow\ArtisanAssist\Commands\makeTransformer::class,
];


```

Finally, you can checkout `$ php artisan` and you can see 3 commands.

``` bash
  make:service           
  make:respository
  make:transformer
```
