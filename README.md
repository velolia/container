# Velolia Container
Velolia Container is a lightweight and efficient dependency injection (DI) container for PHP, designed to make it easier to manage object dependencies within your applications. Inspired by modern PHP DI principles, Velolia Container aims to streamline dependency management, enhance code modularity.

# Basic Usage
Create a Container Instance

To start using Velolia Container, you need to create an instance of the container:

```php
use Velolia\Container\Container;

$container = new Container();

$container->singleton('logger', function () {
    return new Logger();
});

$container->singleton('logger', fn () => new Logger());

$container->make('logger');

```

OR
```php
use Velolia\Container\Container;

$container = new Container();

$container->singleton(Router::class, $this);

$container->make(Router::class);

```
