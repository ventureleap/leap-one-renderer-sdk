# VentureLeap\RendererService\TemplateApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteTemplateItem**](TemplateApi.md#deletetemplateitem) | **DELETE** /renderer/templates/{id} | Removes the Template resource.
[**getTemplateCollection**](TemplateApi.md#gettemplatecollection) | **GET** /renderer/templates | Retrieves the collection of Template resources.
[**getTemplateItem**](TemplateApi.md#gettemplateitem) | **GET** /renderer/templates/{id} | Retrieves a Template resource.
[**postTemplateCollection**](TemplateApi.md#posttemplatecollection) | **POST** /renderer/templates | Creates a Template resource.

# **deleteTemplateItem**
> deleteTemplateItem($id)

Removes the Template resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\TemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $apiInstance->deleteTemplateItem($id);
} catch (Exception $e) {
    echo 'Exception when calling TemplateApi->deleteTemplateItem: ', $e->getMessage(), PHP_EOL;
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

# **getTemplateCollection**
> \VentureLeap\RendererService\Model\InlineResponse2002 getTemplateCollection($properties, $custom_data, $file_name, $file_type, $template_key, $created_at_before, $created_at_strictly_before, $created_at_after, $created_at_strictly_after, $updated_at_before, $updated_at_strictly_before, $updated_at_after, $updated_at_strictly_after, $page)

Retrieves the collection of Template resources.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\TemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$properties = array("properties_example"); // string[] | Allows you to reduce the response to contain only the properties you need. If your desired property is nested, you can address it using nested arrays. Example: properties[]={propertyName}&properties[]={anotherPropertyName}&properties[{nestedPropertyParent}][]={nestedProperty}
$custom_data = "custom_data_example"; // string | 
$file_name = "file_name_example"; // string | 
$file_type = "file_type_example"; // string | 
$template_key = "template_key_example"; // string | 
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
    $result = $apiInstance->getTemplateCollection($properties, $custom_data, $file_name, $file_type, $template_key, $created_at_before, $created_at_strictly_before, $created_at_after, $created_at_strictly_after, $updated_at_before, $updated_at_strictly_before, $updated_at_after, $updated_at_strictly_after, $page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateApi->getTemplateCollection: ', $e->getMessage(), PHP_EOL;
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
 **template_key** | **string**|  | [optional]
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

[**\VentureLeap\RendererService\Model\InlineResponse2002**](../Model/InlineResponse2002.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTemplateItem**
> \VentureLeap\RendererService\Model\TemplateJsonldTemplateRead getTemplateItem($id)

Retrieves a Template resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\TemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->getTemplateItem($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateApi->getTemplateItem: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\VentureLeap\RendererService\Model\TemplateJsonldTemplateRead**](../Model/TemplateJsonldTemplateRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTemplateCollection**
> \VentureLeap\RendererService\Model\TemplateJsonldTemplateRead postTemplateCollection($file, $template_key)

Creates a Template resource.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = VentureLeap\RendererService\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new VentureLeap\RendererService\Api\TemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = "file_example"; // string | 
$template_key = "template_key_example"; // string | 

try {
    $result = $apiInstance->postTemplateCollection($file, $template_key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TemplateApi->postTemplateCollection: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **string****string**|  | [optional]
 **template_key** | **string**|  | [optional]

### Return type

[**\VentureLeap\RendererService\Model\TemplateJsonldTemplateRead**](../Model/TemplateJsonldTemplateRead.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/ld+json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

