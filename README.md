<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

### Created for [Laravel 6](https://laravel.com)


##### Install  
`composer require muetzeofficial/laravel-settings`

##### Publish
`php artisan vendor:publish --provider="MuetzeOfficial\Settings\SettingsServiceProvider"`

##### Migrate
`php artisan migrate`


#### Usage
With the setting() helper, we can get and set options:
```
// Get setting
setting('someKey');

// Set setting
setting(['someKey' => 'someValue']);

// Check the option exists
setting_exists('someKey');
```

If you want to check if an option exists, you can use the facade:
```
use MuetzeOfficial\Settings\SettingFacade as Setting;

Setting::set(['someKey'=>'someValue']);

Setting::set([
    'someKey'=>'someValue',
    'anotherKey'=>'anotherValue',
]);

Setting::get('someKey');
```
### Blade
```
@setting('someKey')
```
### Console
It is also possible to set options within the console:
```
php artisan setting:set {someKey} {someValue}
```
