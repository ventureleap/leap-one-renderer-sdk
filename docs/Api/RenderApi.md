# VentureLeap\RendererService\RenderApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteRenderItem**](RenderApi.md#deleterenderitem) | **DELETE** /renderer/renders/{id} | Removes the Render resource.
[**getRenderCollection**](RenderApi.md#getrendercollection) | **GET** /renderer/renders | Retrieves the collection of Render resources.
[**getRenderItem**](RenderApi.md#getrenderitem) | **GET** /renderer/renders/{id} | Retrieves a Render resource.
[**postRenderCollection**](RenderApi.md#postrendercollection) | **POST** /renderer/renders | Creates a Render resource.
[**putRenderItem**](RenderApi.md#putrenderitem) | **PUT** /renderer/renders/{id} | Replaces the Render resource.

# **deleteRenderItem**
> deleteRenderItem($id)

Removes the Render resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\RenderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteRenderItem($id);
} catch (Exception $e) {
    echo 'Exception when calling RenderApi->deleteRenderItem: ', $e->getMessage(), PHP_EOL;
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

# **getRenderCollection**
> \VentureLeap\RendererService\Model\InlineResponse2001 getRenderCollection($properties, $custom_data, $file_name, $file_type, $created_at_before, $created_at_strictly_before, $created_at_after, $created_at_strictly_after, $updated_at_before, $updated_at_strictly_before, $updated_at_after, $updated_at_strictly_after, $page)

Retrieves the collection of Render resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\RenderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$properties = array("properties_example"); // string[] | Allows you to reduce the response to contain only the properties you need. If your desired property is nested, you can address it using nested arrays. Example: properties[]={propertyName}&properties[]={anotherPropertyName}&properties[{nestedPropertyParent}][]={nestedProperty}
$custom_data = "custom_data_example"; // string | 
$file_name = "file_name_example"; // string | 
$file_type = "file_type_example"; // string | 
$created_at_before = "created_at_before_example"; // string | 
$created_at_strictly_before = "created_at_strictly_before_example"; // string | 
$created_at_after = "created_at_after_example"; // string | 
$created_at_strictly_after = "created_at_strictly_after_example"; // string | 
$updated_at_before = "updated_at_before_example"; // string | 
$updated_at_strictly_before = "updated_at_strictly_before_example"; // string | 
$updated_at_after = "updated_at_after_example"; // string | 
$updated_at_strictly_after = "updated_at_strictly_after_example"; // string | 
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->getRenderCollection($properties, $custom_data, $file_name, $file_type, $created_at_before, $created_at_strictly_before, $created_at_after, $created_at_strictly_after, $updated_at_before, $updated_at_strictly_before, $updated_at_after, $updated_at_strictly_after, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RenderApi->getRenderCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **properties** | [**string[]**](../Model/string.md)| Allows you to reduce the response to contain only the properties you need. If your desired property is nested, you can address it using nested arrays. Example: properties[]&#x3D;{propertyName}&amp;properties[]&#x3D;{anotherPropertyName}&amp;properties[{nestedPropertyParent}][]&#x3D;{nestedProperty} | [optional]
 **custom_data** | **string**|  | [optional]
 **file_name** | **string**|  | [optional]
 **file_type** | **string**|  | [optional]
 **created_at_before** | **string**|  | [optional]
 **created_at_strictly_before** | **string**|  | [optional]
 **created_at_after** | **string**|  | [optional]
 **created_at_strictly_after** | **string**|  | [optional]
 **updated_at_before** | **string**|  | [optional]
 **updated_at_strictly_before** | **string**|  | [optional]
 **updated_at_after** | **string**|  | [optional]
 **updated_at_strictly_after** | **string**|  | [optional]
 **page** | **int**| The collection page number | [optional] [default to 1]

### Return type

[**\VentureLeap\RendererService\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getRenderItem**
> \VentureLeap\RendererService\Model\RenderJsonldRenderRead getRenderItem($id)

Retrieves a Render resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\RenderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getRenderItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RenderApi->getRenderItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\VentureLeap\RendererService\Model\RenderJsonldRenderRead**](../Model/RenderJsonldRenderRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postRenderCollection**
> \VentureLeap\RendererService\Model\RenderJsonldRenderRead postRenderCollection($body)

Creates a Render resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\RenderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \VentureLeap\RendererService\Model\RenderJsonldRenderWrite(); // \VentureLeap\RendererService\Model\RenderJsonldRenderWrite | The new Render resource

try {
    $result = $apiInstance->postRenderCollection($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RenderApi->postRenderCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\VentureLeap\RendererService\Model\RenderJsonldRenderWrite**](../Model/RenderJsonldRenderWrite.md)| The new Render resource | [optional]

### Return type

[**\VentureLeap\RendererService\Model\RenderJsonldRenderRead**](../Model/RenderJsonldRenderRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putRenderItem**
> \VentureLeap\RendererService\Model\RenderJsonldRenderRead putRenderItem($id, $body)

Replaces the Render resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\RenderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 
$body = new \VentureLeap\RendererService\Model\RenderJsonldRenderWrite(); // \VentureLeap\RendererService\Model\RenderJsonldRenderWrite | The updated Render resource

try {
    $result = $apiInstance->putRenderItem($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RenderApi->putRenderItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |
 **body** | [**\VentureLeap\RendererService\Model\RenderJsonldRenderWrite**](../Model/RenderJsonldRenderWrite.md)| The updated Render resource | [optional]

### Return type

[**\VentureLeap\RendererService\Model\RenderJsonldRenderRead**](../Model/RenderJsonldRenderRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/ld+json
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

