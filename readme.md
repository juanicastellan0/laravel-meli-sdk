<p align="center">
<img src="https://avatars1.githubusercontent.com/u/49149236"/>
</p>

## MeliSdk: El API de Mercadolibre, facil.  

[![License](https://poser.pugx.org/tecnogo/laravel-meli-sdk/license)](https://packagist.org/packages/phpunit/phpunit)

### Requerimientos

 * PHP 7.2
 * ext-curl
 * ext-json

### Instalación

`composer require tecnogo/laravel-meli-sdk`

### Uso

```php

// Obtener bookmarks:

$bookmarks = \MeliSdk::bookmarks();

$bookmarks->each(function (\Tecnogo\MeliSdk\Entity\LoggedUser\Bookmark $bookmark) {
    $item = $bookmark->item();
    echo $item->title() . "\n";
    echo json_encode($item->attributes()->simplifiedMap());
});
```