# Request logging

This Laravel package contains middleware to log requests and there responses including all parameters. 

## Installation

You can install using [composer](https://getcomposer.org/) 

```
composer require michelmelo/laravel-request-logging
```

Next step is to add the middleware in your app/Http/Kernel.php file.

Add the request logging to all routes:
```
protected $middleware = [
    ...
    \MichelMelo\RequestLogging\LogRequest::class,
    ...
];
```

Or you only for specific route(group)s.
```
protected $routeMiddleware = [
    ...
    'logRequest' => \MichelMelo\RequestLogging\LogRequest::class,
    ...
];
```

Finally, although optionally, you can publish the configuration file:

```
php artisan vendor:publish --provider="MichelMelo\RequestLogging\RequestLoggingServiceProvider"
```

