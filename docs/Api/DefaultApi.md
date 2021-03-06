# OpenAPI\Client\DefaultApi

All URIs are relative to *https://api.classifyai.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createNewModel**](DefaultApi.md#createNewModel) | **PUT** /models | Create New Model
[**deleteModel**](DefaultApi.md#deleteModel) | **DELETE** /models | Delete Model
[**getModelsList**](DefaultApi.md#getModelsList) | **GET** /models | Get Models List
[**indexByImageUrl**](DefaultApi.md#indexByImageUrl) | **POST** /index_by_image_url | Index by Using Image URL
[**indexImage**](DefaultApi.md#indexImage) | **POST** /index_image | Index Local Image
[**tagImageByUrl**](DefaultApi.md#tagImageByUrl) | **GET** /predict_by_image_url | Tag Image by Using Image Url
[**tagLocalImage**](DefaultApi.md#tagLocalImage) | **POST** /predict | Predict by Image
[**updateModel**](DefaultApi.md#updateModel) | **POST** /models | Update Model



## createNewModel

> createNewModel($model_name)

Create New Model

Create a new custom image recognition model

### Example

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

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_name** | **string**| Set a name for your model |

### Return type

void (empty response body)

### Authorization

[x-api-key](../../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## deleteModel

> deleteModel($model_id)

Delete Model

Delete Model

### Example

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
$model_id = 'model_id_example'; // string | You can find your model ids from Classify Dashboard.

try {
    $apiInstance->deleteModel($model_id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->deleteModel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | **string**| You can find your model ids from Classify Dashboard. |

### Return type

void (empty response body)

### Authorization

[x-api-key](../../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getModelsList

> string getModelsList()

Get Models List

Get the list of of models created

### Example

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

try {
    $result = $apiInstance->getModelsList();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->getModelsList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

This endpoint does not need any parameter.

### Return type

**string**

### Authorization

[x-api-key](../../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## indexByImageUrl

> indexByImageUrl($inline_object)

Index by Using Image URL

Index by Using Image URL

### Example

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
$inline_object = new \OpenAPI\Client\Model\InlineObject(); // \OpenAPI\Client\Model\InlineObject | 

try {
    $apiInstance->indexByImageUrl($inline_object);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->indexByImageUrl: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inline_object** | [**\OpenAPI\Client\Model\InlineObject**](../Model/InlineObject.md)|  |

### Return type

void (empty response body)

### Authorization

[x-api-key](../../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## indexImage

> string indexImage($model_id, $tag, $file)

Index Local Image

Index Local Image

### Example

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
$model_id = 'model_id_example'; // string | 
$tag = 'tag_example'; // string | 
$file = "/path/to/file.txt"; // \SplFileObject | 

try {
    $result = $apiInstance->indexImage($model_id, $tag, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->indexImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | **string**|  | [optional]
 **tag** | **string**|  | [optional]
 **file** | **\SplFileObject****\SplFileObject**|  | [optional]

### Return type

**string**

### Authorization

[x-api-key](../../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## tagImageByUrl

> tagImageByUrl($model_id, $image_url)

Tag Image by Using Image Url

Predict image tags by providing image url

### Example

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
$model_id = 'model_id_example'; // string | Type your trained model id to predict. You get your model's id from Classify Dashboard.
$image_url = 'image_url_example'; // string | Provide image url to predict

try {
    $apiInstance->tagImageByUrl($model_id, $image_url);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->tagImageByUrl: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_id** | **string**| Type your trained model id to predict. You get your model&#39;s id from Classify Dashboard. |
 **image_url** | **string**| Provide image url to predict |

### Return type

void (empty response body)

### Authorization

[x-api-key](../../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## tagLocalImage

> tagLocalImage($file, $model_id)

Predict by Image

Send a local image to tag

### Example

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
$file = "/path/to/file.txt"; // \SplFileObject | 
$model_id = 'model_id_example'; // string | 

try {
    $apiInstance->tagLocalImage($file, $model_id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->tagLocalImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **\SplFileObject****\SplFileObject**|  | [optional]
 **model_id** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[x-api-key](../../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## updateModel

> updateModel($model_name, $model_id)

Update Model

Update Model Name

### Example

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
$model_name = 'model_name_example'; // string | Model Name
$model_id = 'model_id_example'; // string | Model id to be renamed.

try {
    $apiInstance->updateModel($model_name, $model_id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->updateModel: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model_name** | **string**| Model Name |
 **model_id** | **string**| Model id to be renamed. |

### Return type

void (empty response body)

### Authorization

[x-api-key](../../README.md#x-api-key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

