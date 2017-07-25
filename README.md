# laravel-imap

## Install

1. In your terminal via composer:

``` bash
composer require Frnwtr/laravel-imap
```

2. Add this provider to your config/app.php :
```
Frnwtr\LaravelImap\Providers\LaravelServiceProvider::class,
```

3. Publish config file 
```
php artisan vendor:publish --provider="Frnwtr\LaravelImap\Providers\LaravelServiceProvider"
``` 
then Define host, username, password, etc in your ``` config/imap.php ```.




## Usage

Example usage: 

```php
use Frnwtr\LaravelImap\Client;
use Frnwtr\LaravelImap\Mailbox;

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

If you discover any security related issues, please email walter.franchetti@gmail.com instead of using the issue tracker.

## Credits

- [Frnwtr](http://github.com/Frnwtr)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[link-author]: https://github.com/Frnwtr
