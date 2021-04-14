# VentureLeap\RendererService\RenderApi

All URIs are relative to */*

Method | HTTP request | Description
------------- | ------------- | -------------
[**postRenderCollection**](RenderApi.md#postrendercollection) | **POST** /renderer/renders | Creates a Render resource.

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

