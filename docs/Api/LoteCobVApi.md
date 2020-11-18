# Swagger\Client\LoteCobVApi

All URIs are relative to *https://pix.example.com/api/v2/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**lotecobvGet**](LoteCobVApi.md#lotecobvget) | **GET** /lotecobv | Consultar lista de lotes de cobranças com vencimento.
[**lotecobvIdGet**](LoteCobVApi.md#lotecobvidget) | **GET** /lotecobv/{id} | Consultar lote de cobranças com vencimento.
[**lotecobvIdPut**](LoteCobVApi.md#lotecobvidput) | **PUT** /lotecobv/{id} | Criar lote de cobranças com vencimento.

# **lotecobvGet**
> \Swagger\Client\Model\LotesCobVConsultados lotecobvGet($inicio, $fim, $paginacao_pagina_atual, $paginacao_itens_por_pagina)

Consultar lista de lotes de cobranças com vencimento.

Endpoint para consultar lista de lotes de cobranças com vencimento.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\LoteCobVApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inicio = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$fim = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$paginacao_pagina_atual = 0; // int | 
$paginacao_itens_por_pagina = 100; // int | 

try {
    $result = $apiInstance->lotecobvGet($inicio, $fim, $paginacao_pagina_atual, $paginacao_itens_por_pagina);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoteCobVApi->lotecobvGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inicio** | **\DateTime**|  |
 **fim** | **\DateTime**|  |
 **paginacao_pagina_atual** | **int**|  | [optional] [default to 0]
 **paginacao_itens_por_pagina** | **int**|  | [optional] [default to 100]

### Return type

[**\Swagger\Client\Model\LotesCobVConsultados**](../Model/LotesCobVConsultados.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **lotecobvIdGet**
> \Swagger\Client\Model\LoteCobVConsultado lotecobvIdGet($id)

Consultar lote de cobranças com vencimento.

Endpoint para consultar um lote de cobranças com vencimento.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\LoteCobVApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | 

try {
    $result = $apiInstance->lotecobvIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoteCobVApi->lotecobvIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  |

### Return type

[**\Swagger\Client\Model\LoteCobVConsultado**](../Model/LoteCobVConsultado.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **lotecobvIdPut**
> lotecobvIdPut($body, $id)

Criar lote de cobranças com vencimento.

Endpoint para criar um lote de cobranças com vencimento.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\LoteCobVApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \stdClass; // object | Dados para geração de lote de cobranças com vencimento.
$id = "id_example"; // string | 

try {
    $apiInstance->lotecobvIdPut($body, $id);
} catch (Exception $e) {
    echo 'Exception when calling LoteCobVApi->lotecobvIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**object**](../Model/object.md)| Dados para geração de lote de cobranças com vencimento. |
 **id** | **string**|  |

### Return type

void (empty response body)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

