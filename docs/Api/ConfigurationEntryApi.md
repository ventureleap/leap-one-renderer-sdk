# VentureLeap\RendererService\ConfigurationEntryApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteConfigurationEntryItem**](ConfigurationEntryApi.md#deleteconfigurationentryitem) | **DELETE** /renderer/configuration_entries/{id} | Removes the ConfigurationEntry resource.
[**getConfigurationEntryCollection**](ConfigurationEntryApi.md#getconfigurationentrycollection) | **GET** /renderer/configuration_entries | Retrieves the collection of ConfigurationEntry resources.
[**getConfigurationEntryItem**](ConfigurationEntryApi.md#getconfigurationentryitem) | **GET** /renderer/configuration_entries/{id} | Retrieves a ConfigurationEntry resource.
[**postConfigurationEntryCollection**](ConfigurationEntryApi.md#postconfigurationentrycollection) | **POST** /renderer/configuration_entries | Creates a ConfigurationEntry resource.
[**putConfigurationEntryItem**](ConfigurationEntryApi.md#putconfigurationentryitem) | **PUT** /renderer/configuration_entries/{id} | Replaces the ConfigurationEntry resource.

# **deleteConfigurationEntryItem**
> deleteConfigurationEntryItem($id)

Removes the ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteConfigurationEntryItem($id);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->deleteConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConfigurationEntryCollection**
> \VentureLeap\RendererService\Model\InlineResponse200 getConfigurationEntryCollection($key, $sub_key, $value, $application_id, $page)

Retrieves the collection of ConfigurationEntry resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$key = "key_example"; // string | 
$sub_key = "sub_key_example"; // string | 
$value = "value_example"; // string | 
$application_id = "application_id_example"; // string | 
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->getConfigurationEntryCollection($key, $sub_key, $value, $application_id, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->getConfigurationEntryCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**|  | [optional]
 **sub_key** | **string**|  | [optional]
 **value** | **string**|  | [optional]
 **application_id** | **string**|  | [optional]
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**\VentureLeap\RendererService\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getConfigurationEntryItem**
> \VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationRead getConfigurationEntryItem($id)

Retrieves a ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getConfigurationEntryItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->getConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postConfigurationEntryCollection**
> \VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationRead postConfigurationEntryCollection($body)

Creates a ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationWrite | The new ConfigurationEntry resource

try {
    $result = $apiInstance->postConfigurationEntryCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->postConfigurationEntryCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationWrite**](../Model/ConfigurationEntryJsonldConfigurationWrite.md)| The new ConfigurationEntry resource | [optional]

### Return type

[**\VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putConfigurationEntryItem**
> \VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationRead putConfigurationEntryItem($id, $body)

Replaces the ConfigurationEntry resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\ConfigurationEntryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationWrite(); // \VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationWrite | The updated ConfigurationEntry resource

try {
    $result = $apiInstance->putConfigurationEntryItem($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConfigurationEntryApi->putConfigurationEntryItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **body** | [**\VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationWrite**](../Model/ConfigurationEntryJsonldConfigurationWrite.md)| The updated ConfigurationEntry resource | [optional]

### Return type

[**\VentureLeap\RendererService\Model\ConfigurationEntryJsonldConfigurationRead**](../Model/ConfigurationEntryJsonldConfigurationRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

