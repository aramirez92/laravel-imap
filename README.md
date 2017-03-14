# laravel-imap

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Total Downloads][ico-downloads]][link-downloads]
[![Software License][ico-license]](LICENSE.md)

## Install

1. Via Composer

``` bash
composer require aramirez92/laravel-imap
```

2. Copy `vendor\aramirez92\laravel-imap\config\imap.php` to `config\imap.php`. Edit to change host, username, password.


3. Add this line to `config\app.php` into providers section:
```
Aramirez92\LaravelImap\Providers\LaravelServiceProvider::class,
```

## Usage

Example usage: 

```php
use Aramirez92\LaravelImap\Client;
use Aramirez92\LaravelImap\Mailbox;

// ...

$client = new Client();
$client->connect();

$mailboxes = $client->getMailboxes();
foreach($mailboxes as $mailbox) {
    dump($mailbox->getMessages());
}
```

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Security

If you discover any security related issues, please email devops92@gmail.com instead of using the issue tracker.

## Credits

- [aramirez92](http://github.com/aramirez92)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/aramirez92/laravel-imap.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/aramirez92/laravel-imap/master.svg?style=flat-square
[ico-scrutinizer]: https://img.shields.io/scrutinizer/coverage/g/aramirez92/laravel-imap.svg?style=flat-square
[ico-code-quality]: https://img.shields.io/scrutinizer/g/aramirez92/laravel-imap.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/aramirez92/laravel-imap.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/aramirez92/laravel-imap
[link-travis]: https://travis-ci.org/aramirez92/laravel-imap
[link-scrutinizer]: https://scrutinizer-ci.com/g/aramirez92/laravel-imap/code-structure
[link-code-quality]: https://scrutinizer-ci.com/g/aramirez92/laravel-imap
[link-downloads]: https://packagist.org/packages/aramirez92/laravel-imap
[link-author]: https://github.com/aramirez92
