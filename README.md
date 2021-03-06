# OpenAPIClient-php

Classify Custom Image Recognition Service

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0.0
- Build package: org.openapitools.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage

### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```bash
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure API key authorization: x-api-key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');


$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$model_name = {"model_name":"\"Test model name\""}; // string | Set a name for your model

try {
    $apiInstance->createNewModel($model_name);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->createNewModel: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.classifyai.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**createNewModel**](docs/Api/DefaultApi.md#createnewmodel) | **PUT** /models | Create New Model
*DefaultApi* | [**deleteModel**](docs/Api/DefaultApi.md#deletemodel) | **DELETE** /models | Delete Model
*DefaultApi* | [**getModelsList**](docs/Api/DefaultApi.md#getmodelslist) | **GET** /models | Get Models List
*DefaultApi* | [**indexByImageUrl**](docs/Api/DefaultApi.md#indexbyimageurl) | **POST** /index_by_image_url | Index by Using Image URL
*DefaultApi* | [**indexImage**](docs/Api/DefaultApi.md#indeximage) | **POST** /index_image | Index Local Image
*DefaultApi* | [**tagImageByUrl**](docs/Api/DefaultApi.md#tagimagebyurl) | **GET** /predict_by_image_url | Tag Image by Using Image Url
*DefaultApi* | [**tagLocalImage**](docs/Api/DefaultApi.md#taglocalimage) | **POST** /predict | Predict by Image
*DefaultApi* | [**updateModel**](docs/Api/DefaultApi.md#updatemodel) | **POST** /models | Update Model


## Documentation For Models

 - [InlineObject](docs/Model/InlineObject.md)
 - [InlineObject1](docs/Model/InlineObject1.md)
 - [InlineObject2](docs/Model/InlineObject2.md)


## Documentation For Authorization



## x-api-key


- **Type**: API key
- **API key parameter name**: x-api-key
- **Location**: HTTP header



## Author

info@inoven.ai

