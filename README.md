# Unofficial EmailLabs&trade; mail driver for Laravel
  Simple package to integrate Laravel Email with [EmailLabs&trade;](http://emaillabs.io) 
  based on https://github.com/beryldev/laravel-emaillabs package.


## Installation

Require this package with composer:

```
composer require dct24/emaillabs-laravel
```

After updating composer, add the EmailLabsServiceProvider to the providers array in config/app.php
> If you use Laravel Debugbar with enabled email collector, make sure you load EmailLabsServiceProvider before Debugbar ServiceProvider.



In Laravel 5.5 and above, the package will autoregister the service provider. 


For Laravel 5.4 or below you must install this service provider to `config/app.php`:

```
Dct24\EmailLabs\EmailLabsServiceProvider::class,
```

Copy the package config to your local config with the publish command:

```
php artisan vendor:publish --provider="Dct24\EmailLabs\EmailLabsServiceProvider" --tag=config
```

## Configuration

After install add to your .env file requred parameters.

### App Key

```
EL_APP=your_emaillabs_app_key
```

### Secret Key

```
EL_SECRET=your_emaillabs_secret_key
```

### SMTP account name

```
EL_SMTP=your_emaillabs_smtp_account_name
```

Now you can use `emaillabs` mail driver

```
MAIL_DRIVER=emaillabs
```

## License

The Laravel EmailLabs Integration is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
