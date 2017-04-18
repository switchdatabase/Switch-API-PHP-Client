# Swagger\Client\DBOperationsApi

All URIs are relative to *http://tr02.switchapi.com/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addPost**](DBOperationsApi.md#addPost) | **POST** /Add | Add is used for adding a data object to the list created at Switch DB.
[**listPost**](DBOperationsApi.md#listPost) | **POST** /List | It&#39;s used for listing a data added before.
[**setDelete**](DBOperationsApi.md#setDelete) | **DELETE** /Set | It&#39;s used for deleting a data added before at Switch DB.
[**setPost**](DBOperationsApi.md#setPost) | **POST** /Set | It&#39;s used for updating a data object that is already added to Switch DB.


# **addPost**
> \Swagger\Client\Model\AddResponse addPost($api_key, $access_token, $list, $body)

Add is used for adding a data object to the list created at Switch DB.

You can choose the list that will be added tha data set to with List parameter that will be sent to Header. It's equal to INSERT query at the relational databases model. The data set that will be added to the database is transmited at request body. For versions upper than v1.2.1, if the data sent is an array, all items in the array are added one by one, so they are added as a whole.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\DBOperationsApi();
$api_key = "api_key_example"; // string | Your Switch API Key.
$access_token = "access_token_example"; // string | Your Access Token.
$list = "list_example"; // string | Your data list name.
$body = "body_example"; // string | Your new value JSON.

try {
    $result = $api_instance->addPost($api_key, $access_token, $list, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DBOperationsApi->addPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**| Your Switch API Key. |
 **access_token** | **string**| Your Access Token. |
 **list** | **string**| Your data list name. |
 **body** | **string**| Your new value JSON. |

### Return type

[**\Swagger\Client\Model\AddResponse**](../Model/AddResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **listPost**
> listPost($api_key, $access_token, $list, $body)

It's used for listing a data added before.

List parameter sent remarks the list that will be do listing work on at Header. It's equal to SELECT query at relational databases.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\DBOperationsApi();
$api_key = "api_key_example"; // string | Your Switch API Key.
$access_token = "access_token_example"; // string | Your Access Token.
$list = "list_example"; // string | Your data list name.
$body = new \Swagger\Client\Model\Body(); // \Swagger\Client\Model\Body | Your Switch DB Query.

try {
    $api_instance->listPost($api_key, $access_token, $list, $body);
} catch (Exception $e) {
    echo 'Exception when calling DBOperationsApi->listPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**| Your Switch API Key. |
 **access_token** | **string**| Your Access Token. |
 **list** | **string**| Your data list name. |
 **body** | [**\Swagger\Client\Model\Body**](../Model/\Swagger\Client\Model\Body.md)| Your Switch DB Query. |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setDelete**
> \Swagger\Client\Model\SetResponse setDelete($api_key, $access_token, $list, $list_item_id)

It's used for deleting a data added before at Switch DB.

List parameter sent remarks the list that will be deleted data from at Header and ListItemId parameter remarks the ID consisted by Switch DB for the data that will be deleted. It's equal to DELETE query at relational databases.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\DBOperationsApi();
$api_key = "api_key_example"; // string | Your Switch API Key.
$access_token = "access_token_example"; // string | Your Access Token.
$list = "list_example"; // string | Your data list name.
$list_item_id = "list_item_id_example"; // string | Your list item id.

try {
    $result = $api_instance->setDelete($api_key, $access_token, $list, $list_item_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DBOperationsApi->setDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**| Your Switch API Key. |
 **access_token** | **string**| Your Access Token. |
 **list** | **string**| Your data list name. |
 **list_item_id** | **string**| Your list item id. |

### Return type

[**\Swagger\Client\Model\SetResponse**](../Model/SetResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **setPost**
> \Swagger\Client\Model\SetResponse setPost($api_key, $access_token, $list, $list_item_id, $body)

It's used for updating a data object that is already added to Switch DB.

In order to UPDATE a object, Listname and ListItemId parameters should be sent in the Header of the REQUEST as \"List\", \"ListItemId\", respectively, as shown in the example below. It's equal to UPDATE query at relational databases. The data set that will be edited is transmited to the database at request body.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\DBOperationsApi();
$api_key = "api_key_example"; // string | Your Switch API Key.
$access_token = "access_token_example"; // string | Your Access Token.
$list = "list_example"; // string | Your data list name.
$list_item_id = "list_item_id_example"; // string | Your list item id.
$body = "body_example"; // string | Your new value JSON.

try {
    $result = $api_instance->setPost($api_key, $access_token, $list, $list_item_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DBOperationsApi->setPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_key** | **string**| Your Switch API Key. |
 **access_token** | **string**| Your Access Token. |
 **list** | **string**| Your data list name. |
 **list_item_id** | **string**| Your list item id. |
 **body** | **string**| Your new value JSON. |

### Return type

[**\Swagger\Client\Model\SetResponse**](../Model/SetResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

