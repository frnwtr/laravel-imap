# laravel-imap

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Total Downloads][ico-downloads]][link-downloads]
[![Software License][ico-license]](LICENSE.md)

## Install

1. In your terminal via composer:

``` bash
composer require zalazdi/laravel-imap
```

2. Add this provider to your config/app.php :
```
Zalazdi\LaravelImap\Providers\LaravelServiceProvider::class,
```

3. Publish config file 
```
php artisan vendor:publish --provider="Zalazdi\LaravelImap\Providers\LaravelServiceProvider"
``` 
then Define host, username, password, etc in your ``` config/imap.php ```.




## Usage

Example usage: 

```php
use Zalazdi\LaravelImap\Client;
use Zalazdi\LaravelImap\Mailbox;

// ...

$client = new Client();
$client->connect();

$mailboxes = $client->getFolders();
foreach($mailboxes as $mailbox) {
    dump($mailbox->getMessages());
}
```

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Security

If you discover any security related issues, please email zalazdi@gmail.com instead of using the issue tracker.

## Credits

- [Zalazdi](http://github.com/zalazdi)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/zalazdi/laravel-imap.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/zalazdi/laravel-imap/master.svg?style=flat-square
[ico-scrutinizer]: https://img.shields.io/scrutinizer/coverage/g/zalazdi/laravel-imap.svg?style=flat-square
[ico-code-quality]: https://img.shields.io/scrutinizer/g/zalazdi/laravel-imap.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/zalazdi/laravel-imap.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/zalazdi/laravel-imap
[link-travis]: https://travis-ci.org/zalazdi/laravel-imap
[link-scrutinizer]: https://scrutinizer-ci.com/g/zalazdi/laravel-imap/code-structure
[link-code-quality]: https://scrutinizer-ci.com/g/zalazdi/laravel-imap
[link-downloads]: https://packagist.org/packages/zalazdi/laravel-imap
[link-author]: https://github.com/zalazdi
