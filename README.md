# php-api-router
PHP API Router

## Support

Supports:

- GET
...PUT

## Use

Make sure include path is set to the location where you put the script.

```php
include('Router.php');
```

### Get,Post,Put,Patch,Delete

```php
Router::get('/endpoint',function() {
  // todo
});
```

### All methods

```php
Router::all('/endpoint',function() {
  // todo
});
```
