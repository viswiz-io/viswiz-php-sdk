# VisWiz\SDK\BuildsApi

All URIs are relative to *https://api.viswiz.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createBuild**](BuildsApi.md#createBuild) | **POST** /projects/{projectID}/builds | Create a build
[**finishBuild**](BuildsApi.md#finishBuild) | **POST** /builds/{buildID}/finish | Finish a build
[**getBuildResults**](BuildsApi.md#getBuildResults) | **GET** /builds/{buildID}/results | Get results for a build
[**getBuilds**](BuildsApi.md#getBuilds) | **GET** /projects/{projectID}/builds | Get builds for a project


# **createBuild**
> \VisWiz\SDK\Model\Build createBuild($projectID, $body)

Create a build

Create a new build for a project.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VisWiz\SDK\Api\BuildsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$projectID = "projectID_example"; // string | The requested project ID
$body = new \VisWiz\SDK\Model\Body2(); // \VisWiz\SDK\Model\Body2 | 

try {
    $result = $apiInstance->createBuild($projectID, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BuildsApi->createBuild: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectID** | **string**| The requested project ID |
 **body** | [**\VisWiz\SDK\Model\Body2**](../Model/Body2.md)|  |

### Return type

[**\VisWiz\SDK\Model\Build**](../Model/Build.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **finishBuild**
> finishBuild($buildID)

Finish a build

Finish a build when all images have been created. This triggers the actual build comparison to execute.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VisWiz\SDK\Api\BuildsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$buildID = "buildID_example"; // string | The requested build ID

try {
    $apiInstance->finishBuild($buildID);
} catch (Exception $e) {
    echo 'Exception when calling BuildsApi->finishBuild: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | **string**| The requested build ID |

### Return type

void (empty response body)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBuildResults**
> \VisWiz\SDK\Model\BuildResults getBuildResults($buildID)

Get results for a build

Get the results for a build which has been compared to another build.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VisWiz\SDK\Api\BuildsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$buildID = "buildID_example"; // string | The requested build ID

try {
    $result = $apiInstance->getBuildResults($buildID);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BuildsApi->getBuildResults: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **buildID** | **string**| The requested build ID |

### Return type

[**\VisWiz\SDK\Model\BuildResults**](../Model/BuildResults.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getBuilds**
> \VisWiz\SDK\Model\Builds getBuilds($projectID)

Get builds for a project

Get a list of all the builds for a project.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VisWiz\SDK\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VisWiz\SDK\Api\BuildsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$projectID = "projectID_example"; // string | The requested project ID

try {
    $result = $apiInstance->getBuilds($projectID);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BuildsApi->getBuilds: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectID** | **string**| The requested project ID |

### Return type

[**\VisWiz\SDK\Model\Builds**](../Model/Builds.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

