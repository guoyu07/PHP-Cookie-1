# PHP Cookie library

[![Latest Stable Version](https://poser.pugx.org/josantonius/Cookie/v/stable)](https://packagist.org/packages/josantonius/Cookie) [![Latest Unstable Version](https://poser.pugx.org/josantonius/Cookie/v/unstable)](https://packagist.org/packages/josantonius/Cookie) [![License](https://poser.pugx.org/josantonius/Cookie/license)](LICENSE) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/e51e4c06b0b54ce493454d4f895a3ef3)](https://www.codacy.com/app/Josantonius/PHP-Cookie?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Josantonius/PHP-Cookie&amp;utm_campaign=Badge_Grade) [![Total Downloads](https://poser.pugx.org/josantonius/Cookie/downloads)](https://packagist.org/packages/josantonius/Cookie) [![Travis](https://travis-ci.org/Josantonius/PHP-Cookie.svg)](https://travis-ci.org/Josantonius/PHP-Cookie) [![PSR2](https://img.shields.io/badge/PSR-2-1abc9c.svg)](http://www.php-fig.org/psr/psr-2/) [![PSR4](https://img.shields.io/badge/PSR-4-9b59b6.svg)](http://www.php-fig.org/psr/psr-4/) [![CodeCov](https://codecov.io/gh/Josantonius/PHP-Cookie/branch/master/graph/badge.svg)](https://codecov.io/gh/Josantonius/PHP-Cookie)

[English version](README.md)

Biblioteca PHP para el manejo de cookies.

---

- [Requisitos](#requisitos)
- [Instalación](#instalación)
- [Métodos disponibles](#métodos-disponibles)
- [Cómo empezar](#cómo-empezar)
- [Uso](#uso)
- [Tests](#tests)
- [Tareas pendientes](#-tareas-pendientes)
- [Contribuir](#contribuir)
- [Repositorio](#repositorio)
- [Licencia](#licencia)
- [Copyright](#copyright)

---

## Requisitos

Esta clase es soportada por versiones de **PHP 5.6** o superiores y es compatible con versiones de **HHVM 3.0** o superiores.

## Instalación 

La mejor forma de instalar esta extensión es a través de [Composer](http://getcomposer.org/download/).

Para instalar **PHP Cookie library**, simplemente escribe:

    $ composer require Josantonius/Cookie

El comando anterior sólo instalará los archivos necesarios, si prefieres **descargar todo el código fuente** puedes utilizar:

    $ composer require Josantonius/Cookie --prefer-source

También puedes **clonar el repositorio** completo con Git:

	$ git clone https://github.com/Josantonius/PHP-Cookie.git

O **instalarlo manualmente**:

[Descargar Cookie.php](https://raw.githubusercontent.com/Josantonius/PHP-Cookie/master/src/Cookie.php):

    $ wget https://raw.githubusercontent.com/Josantonius/PHP-Cookie/master/src/Cookie.php

## Métodos disponibles

Métodos disponibles en esta biblioteca:

### - Crear cookie:

```php
Cookie::set($key, $value, $time);
```

| Atributo | Descripción | Tipo | Requerido | Predeterminado
| --- | --- | --- | --- | --- |
| $key | Nombre de la cookie. | string | Sí | |
| $value | Valores a guardar. | string | Sí | |
| $time | Tiempo de expiración en días. | string | No | 365 |

**# Return** (boolean)

### - Obtener valor de cookie:

```php
Cookie::get($key);
```

| Atributo | Descripción | Tipo | Requerido | Predeterminado
| --- | --- | --- | --- | --- |
| $key | Nombre de la cookie. | string | No | '' |

**# Return** (mixed|false) → devuelve el valor de la cookie, todas las cookies o falso

### - Extraer valor de cookie eliminarla:

```php
Cookie::pull($key);
```

| Atributo | Descripción | Tipo | Requerido | Predeterminado
| --- | --- | --- | --- | --- |
| $key | Nombre de la cookie. | string | Sí | |

**# Return** (string|false) → valor de la cookie o falso si no existe

### - Eliminar cookie:

```php
Cookie::destroy($key);
```

| Atributo | Descripción | Tipo | Requerido | Predeterminado
| --- | --- | --- | --- | --- |
| $key | Nombre de la cookie a eliminar. Si no se indica ninguna se eliminarán todas las cookies. | string | No | '' |

**# Return** (boolean)

## Cómo empezar

Para utilizar esta clase con `Composer`:

```php
require __DIR__ . '/vendor/autoload.php';

use Josantonius\Cookie\Cookie;
```

Si la instalaste `manualmente`, utiliza:

```php
require_once __DIR__ . '/Cookie.php';

use Josantonius\Cookie\Cookie;
```

## Uso

Ejemplo de uso para esta biblioteca:

### - Agregar cookie:

```php
Cookie::set('cookie_name', 'value', 365);
```

### - Obtener valor de cookie:

```php
Cookie::get('cookie_name');
```

### - Obtener todas las cookies:

```php
Cookie::get();
```

### - Extraer y eliminar cookie:

```php
Cookie::pull('cookie_name');
```

### - Eliminar una cookie:

```php
Cookie::destroy('cookie_name');
```

### - Eliminar todas las cookies:

```php
Cookie::destroy();
```

## Tests 

Para ejecutar las [pruebas](tests) necesitarás [Composer](http://getcomposer.org/download/) y seguir los siguientes pasos:

    $ git clone https://github.com/Josantonius/PHP-Cookie.git
    
    $ cd PHP-Cookie

    $ composer install

Ejecutar pruebas unitarias con [PHPUnit](https://phpunit.de/):

    $ composer phpunit

Ejecutar pruebas de estándares de código [PSR2](http://www.php-fig.org/psr/psr-2/) con [PHPCS](https://github.com/squizlabs/PHP_CodeSniffer):

    $ composer phpcs

Ejecutar todas las pruebas anteriores:

    $ composer tests

## ☑ Tareas pendientes

- [x] Completar tests
- [x] Mejorar la documentación

## Contribuir

1. Comprobar si hay incidencias abiertas o abrir una nueva para iniciar una discusión en torno a un fallo o función.
1. Bifurca la rama del repositorio en GitHub para iniciar la operación de ajuste.
1. Escribe una o más pruebas para la nueva característica o expón el error.
1. Haz cambios en el código para implementar la característica o reparar el fallo.
1. Envía pull request para fusionar los cambios y que sean publicados.

Esto está pensado para proyectos grandes y de larga duración.

## Repositorio

Los archivos de este repositorio se crearon y subieron automáticamente con [Reposgit Creator](https://github.com/Josantonius/BASH-Reposgit).

## Licencia

Este proyecto está licenciado bajo **licencia MIT**. Consulta el archivo [LICENSE](LICENSE) para más información.

## Copyright

2016 - 2017 Josantonius, [josantonius.com](https://josantonius.com/)

Si te ha resultado útil, házmelo saber :wink:

Puedes contactarme en [Twitter](https://twitter.com/Josantonius) o a través de mi [correo electrónico](mailto:hello@josantonius.com).