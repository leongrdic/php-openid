# php-openid
This project is a fork of [LightOpenID](https://github.com/iignatov/LightOpenID) that enables usage of the class from a backend environment (custom passing of return URI and query parameters received on the frontend side).

The only modification is made to the object constructor.

## Getting started
### Using Composer
You can install `php-openid` by running
```
php composer.phar require leongrdic/openid
```

### Not using Composer
You can simply require the `OpenID.php` file from the `src/` folder at the beginning of your script:
```php
require_once('OpenID.php');
```

## Example usage
```php
$openid = new \Le\OpenID($host, $return_uri, $query, $proxy);

if($openid->mode !== 'id_res' || !$openid->validate())
  die('authentication failed');

 $identity = $openid->identity;
```

## Disclaimer
I do not guarantee that this code is 100% secure and it should be used at your own responsibility.

If you find any errors or mistakes, open a ticket or create a pull request.

Please feel free to leave a comment and share your thoughts on this!
