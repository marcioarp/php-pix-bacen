# Swagger\Client\PayloadLocationApi

All URIs are relative to *https://pix.example.com/api/v2/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**locGet**](PayloadLocationApi.md#locget) | **GET** /loc | Consultar locations cadastradas.
[**locIdGet**](PayloadLocationApi.md#locidget) | **GET** /loc/{id} | Recuperar location do payload.
[**locIdTxidDelete**](PayloadLocationApi.md#locidtxiddelete) | **DELETE** /loc/{id}/txid | Desvincular um txid de uma location.
[**locPost**](PayloadLocationApi.md#locpost) | **POST** /loc | Criar location do payload.

# **locGet**
> \Swagger\Client\Model\PayloadLocationConsultadas locGet($inicio, $fim, $tx_id_presente, $tipo_cob, $paginacao_pagina_atual, $paginacao_itens_por_pagina)

Consultar locations cadastradas.

Endpoint para consultar locations cadastradas

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PayloadLocationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inicio = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$fim = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$tx_id_presente = true; // bool | 
$tipo_cob = "tipo_cob_example"; // string | 
$paginacao_pagina_atual = 0; // int | 
$paginacao_itens_por_pagina = 100; // int | 

try {
    $result = $apiInstance->locGet($inicio, $fim, $tx_id_presente, $tipo_cob, $paginacao_pagina_atual, $paginacao_itens_por_pagina);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PayloadLocationApi->locGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inicio** | **\DateTime**|  |
 **fim** | **\DateTime**|  |
 **tx_id_presente** | **bool**|  | [optional]
 **tipo_cob** | **string**|  | [optional]
 **paginacao_pagina_atual** | **int**|  | [optional] [default to 0]
 **paginacao_itens_por_pagina** | **int**|  | [optional] [default to 100]

### Return type

[**\Swagger\Client\Model\PayloadLocationConsultadas**](../Model/PayloadLocationConsultadas.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **locIdGet**
> \Swagger\Client\Model\PayloadLocationCompleta locIdGet($id)

Recuperar location do payload.

Recupera a location do payload

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PayloadLocationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->locIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PayloadLocationApi->locIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Swagger\Client\Model\PayloadLocationCompleta**](../Model/PayloadLocationCompleta.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **locIdTxidDelete**
> \Swagger\Client\Model\PayloadLocation locIdTxidDelete($id)

Desvincular um txid de uma location.

Endpoint para desvinculo de um txid de uma location

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PayloadLocationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->locIdTxidDelete($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PayloadLocationApi->locIdTxidDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Swagger\Client\Model\PayloadLocation**](../Model/PayloadLocation.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **locPost**
> \Swagger\Client\Model\PayloadLocation locPost($body)

Criar location do payload.

Criar location do payload

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PayloadLocationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\PayloadLocationSolicitada(); // \Swagger\Client\Model\PayloadLocationSolicitada | Dados para geração da location.

try {
    $result = $apiInstance->locPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PayloadLocationApi->locPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\PayloadLocationSolicitada**](../Model/PayloadLocationSolicitada.md)| Dados para geração da location. |

### Return type

[**\Swagger\Client\Model\PayloadLocation**](../Model/PayloadLocation.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

