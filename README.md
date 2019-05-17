# PHP Router
PHP API Router

## Support

Supports:

- GET
- PUT
- POST
- DELETE
- PATCH

for custom values, use all.

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

### Other Functions

All code in the 'set' route executes before any other routes.  This is a good place for CORS policys and/or authorization 

```php
Router::set('/',function() {
		// todo
});
```

### Get routes

```php
$routes = Router::getInstance()->routes;
```

### Route Parsing Example

To process routes and run their functions, use a foreach loop, make sure you are accessing the singleton for the Router class or this will not work.

```php
foreach(Router::getInstance()->routes as $key => $value) {
	echo $value['name'];
}
```
