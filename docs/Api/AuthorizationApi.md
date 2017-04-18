# Swagger\Client\AuthorizationApi

All URIs are relative to *http://tr02.switchapi.com/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**tokenGet**](AuthorizationApi.md#tokenGet) | **GET** /Token | Generate Access Token


# **tokenGet**
> string tokenGet($api_key, $signature, $expire)

Generate Access Token

For generating Access Token, you need API Key and API Secret parameters that are provided from the developer portal. At the request, API Key that will be sent by using header is generated as portal API Key and Signature parameter is generated as md5(APISecret + ExpireTimestamp) format. At Expire parameter, token's expire date and time information must be proper to ISO 8601 standarts and Unix Time format with msec information.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\AuthorizationApi();
$api_key = "api_key_example"; // string | Your Switch API Key.
$signature = "signature_example"; // string | Signature parameter is generated as md5(APISecret + ExpireTimestamp) format.
$expire = 789; // int | Expire parameter, token's expire date and time information must be proper to ISO 8601 standarts and Unix Time format with msec information.

try {
    $result = $api_instance->tokenGet($api_key, $signature, $expire);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthorizationApi->tokenGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**| Your Switch API Key. |
 **signature** | **string**| Signature parameter is generated as md5(APISecret + ExpireTimestamp) format. |
 **expire** | **int**| Expire parameter, token&#39;s expire date and time information must be proper to ISO 8601 standarts and Unix Time format with msec information. |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

