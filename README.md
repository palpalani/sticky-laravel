# Lime Light CRM Client for Laravel 8/9

[![Latest Stable Version](https://poser.pugx.org/kevinem/lime-light-crm-laravel/v/stable?format=flat-square)](https://packagist.org/packages/kevinem/lime-light-crm-laravel)
[![License](https://poser.pugx.org/kevinem/lime-light-crm-laravel/license?format=flat-square)](https://packagist.org/packages/kevinem/lime-light-crm-laravel)
[![GitHub Code Style Action Status](https://img.shields.io/github/workflow/status/palpalani/lime-light-crm-laravel/Fix%20PHP%20code%20style%20issues?label=code%20style)](https://github.com/palpalani/lime-light-crm-laravel/actions?query=workflow%3A"Fix+PHP+code+style+issues"+branch%3Apatch-1)

## Installation

You can install the package via composer:

```
composer require kevinem/lime-light-crm-laravel
```

## Documentation

https://secure.na1.echosign.com/public/docs/restapi/v5

## Configuration

After installing the package, register the `KevinEm\LimeLightCRMLaravel\LimeLightCRMLaravelServiceProvider`
in your `config/app.php` configuration file:

```php
'providers' => [
    // Other service providers...

    KevinEm\LimeLightCRMLaravel\LimeLightCRMLaravelServiceProvider::class,
],

```
Also, you can add the `LimeLightCRMLaravel` facade to the `aliases` array in your `config/app.php` configuration file:

```php
'aliases' => [
    // Other facades...
    
    'LimeLightCRM' => KevinEm\LimeLightCRMLaravel\Facades\LimeLightCRMLaravel::class,
],
```

Publish the config using the following command:

```php
$ php artisan vendor:publish
```

## Example Usage

```php
LimeLightCRM::membership()->validateCredentials();

LimeLightCRM::membership()->viewCustomer(['customer_id' => 86]);

LimeLightCRM::transaction()->newProspect([
    'firstName' => 'John',
    'lastName' => 'Doe',
    'email' => 'jdoe@gmail.com'
]);
```

## Testing

```bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Security Vulnerabilities

Please review [our security policy](../../security/policy) on how to report security vulnerabilities.

## Credits

- [palPalani](https://github.com/palpalani)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.