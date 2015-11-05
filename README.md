# E-goi API PHP INTEGRATION

PHP API for integrates E-goi multichannel marketing automation
For usage access E-GOI site in http://www.e-goi.com/en/resources/api/

## Requirements

PHP VERSION
- PHP 5.3 or higher
- ext-curl
- ext-json

FOLLOW PACKAGES:
- zendframework/zend-json
- zendframework/zendrest
- zendframework/zend-soap
- zendframework/zend-xmlrpc

## To install

You can clone this repositorie:

``` git clone https://github.com/twbs/bootstrap.git. ```


You can get it from [Composer](More information? http://getcomposer.org/)

```  composer require hat-framework/e-goi ```

or add this to your composer.json, and ```composer update``` 

```  
{
    "require": {
        "hat-framework/e-goi": "0.1.0"
    }
}
```

You can download files (but remember, in this case, you shoud install or download zendframework dependencies)

``` https://github.com/hat-framework/e-goi/archive/v0.3.4.zip ```

## Usage

```php
require_once './vendor/autoload.php';

$apikey = "<e-goi api key>";

$arguments = array(
    "apikey" => $apikey
);

// $api = EgoiApiFactory::getApi(Protocol::Soap);
// $api = EgoiApiFactory::getApi(Protocol::Rest);
$api = EgoiApiFactory::getApi(Protocol::XmlRpc);
$result = $api->getUserData($arguments);
print_r($result);
```


## Credits

this package is based on https://github.com/alexndreazevedo/egoi-api-php.
But the alexndreazevedo user  doesn't updated e-goi api to 0.3.4 so
i used their base code to update e-goi api to newest version