# VisWiz\SDK\ImagesApi

All URIs are relative to *https://api.viswiz.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createImage**](ImagesApi.md#createImage) | **POST** /builds/{buildID}/images | Create an image
[**getImages**](ImagesApi.md#getImages) | **GET** /builds/{buildID}/images | Get images for a build


# **createImage**
> \VisWiz\SDK\Model\Image createImage($buildID, $name, $image)

Create an image

Upload a new image for a build. This endpoint accepts only one PNG image per request.  This request requires a `Content-Type: multipart/form-data` HTTP header.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VisWiz\SDK\Api\ImagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$buildID = "buildID_example"; // string | The requested build ID
$name = "name_example"; // string | The name of the image
$image = "/path/to/file.txt"; // \SplFileObject | The contents of the image

try {
    $result = $apiInstance->createImage($buildID, $name, $image);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImagesApi->createImage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | **string**| The requested build ID |
 **name** | **string**| The name of the image |
 **image** | **\SplFileObject**| The contents of the image |

### Return type

[**\VisWiz\SDK\Model\Image**](../Model/Image.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getImages**
> \VisWiz\SDK\Model\Images getImages($buildID)

Get images for a build

Get a list of all images for a build.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VisWiz\SDK\Api\ImagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$buildID = "buildID_example"; // string | The requested build ID

try {
    $result = $apiInstance->getImages($buildID);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImagesApi->getImages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | **string**| The requested build ID |

### Return type

[**\VisWiz\SDK\Model\Images**](../Model/Images.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

