# Swagger\Client\CobVApi

All URIs are relative to *https://pix.example.com/api/v2/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cobvGet**](CobVApi.md#cobvget) | **GET** /cobv | Consultar lista de cobranças com vencimento.
[**cobvTxidGet**](CobVApi.md#cobvtxidget) | **GET** /cobv/{txid} | Consultar cobrança com vencimento.
[**cobvTxidPatch**](CobVApi.md#cobvtxidpatch) | **PATCH** /cobv/{txid} | Revisar cobrança com vencimento.
[**cobvTxidPut**](CobVApi.md#cobvtxidput) | **PUT** /cobv/{txid} | Criar cobrança com vencimento.

# **cobvGet**
> \Swagger\Client\Model\CobsVConsultadas cobvGet($inicio, $fim, $cpf, $cnpj, $location_presente, $status, $lote_cob_v_id, $paginacao_pagina_atual, $paginacao_itens_por_pagina)

Consultar lista de cobranças com vencimento.

Endpoint para consultar cobranças com vencimento através de parâmetros como início, fim, cpf, cnpj e status.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CobVApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inicio = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$fim = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$cpf = "cpf_example"; // string | 
$cnpj = "cnpj_example"; // string | 
$location_presente = true; // bool | 
$status = "status_example"; // string | 
$lote_cob_v_id = 56; // int | 
$paginacao_pagina_atual = 0; // int | 
$paginacao_itens_por_pagina = 100; // int | 

try {
    $result = $apiInstance->cobvGet($inicio, $fim, $cpf, $cnpj, $location_presente, $status, $lote_cob_v_id, $paginacao_pagina_atual, $paginacao_itens_por_pagina);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobVApi->cobvGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inicio** | **\DateTime**|  |
 **fim** | **\DateTime**|  |
 **cpf** | **string**|  | [optional]
 **cnpj** | **string**|  | [optional]
 **location_presente** | **bool**|  | [optional]
 **status** | **string**|  | [optional]
 **lote_cob_v_id** | **int**|  | [optional]
 **paginacao_pagina_atual** | **int**|  | [optional] [default to 0]
 **paginacao_itens_por_pagina** | **int**|  | [optional] [default to 100]

### Return type

[**\Swagger\Client\Model\CobsVConsultadas**](../Model/CobsVConsultadas.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **cobvTxidGet**
> \Swagger\Client\Model\CobVCompleta cobvTxidGet($txid, $revisao)

Consultar cobrança com vencimento.

Endpoint para consultar uma cobrança com vencimento através de um determinado txid.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CobVApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$txid = new \Swagger\Client\Model\TxId(); // \Swagger\Client\Model\TxId | 
$revisao = new \Swagger\Client\Model\Revisao(); // \Swagger\Client\Model\Revisao | 

try {
    $result = $apiInstance->cobvTxidGet($txid, $revisao);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobVApi->cobvTxidGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **txid** | [**\Swagger\Client\Model\TxId**](../Model/.md)|  |
 **revisao** | [**\Swagger\Client\Model\Revisao**](../Model/.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\CobVCompleta**](../Model/CobVCompleta.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **cobvTxidPatch**
> \Swagger\Client\Model\CobVGerada cobvTxidPatch($body, $txid)

Revisar cobrança com vencimento.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CobVApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\CobVRevisada(); // \Swagger\Client\Model\CobVRevisada | Dados para geração da cobrança.
$txid = new \Swagger\Client\Model\TxId(); // \Swagger\Client\Model\TxId | 

try {
    $result = $apiInstance->cobvTxidPatch($body, $txid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobVApi->cobvTxidPatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CobVRevisada**](../Model/CobVRevisada.md)| Dados para geração da cobrança. |
 **txid** | [**\Swagger\Client\Model\TxId**](../Model/.md)|  |

### Return type

[**\Swagger\Client\Model\CobVGerada**](../Model/CobVGerada.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **cobvTxidPut**
> \Swagger\Client\Model\CobVGerada cobvTxidPut($body, $txid)

Criar cobrança com vencimento.

Endpoint para criar uma cobrança com vencimento.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CobVApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\CobVSolicitada(); // \Swagger\Client\Model\CobVSolicitada | Dados para geração da cobrança com vencimento.
$txid = new \Swagger\Client\Model\TxId(); // \Swagger\Client\Model\TxId | 

try {
    $result = $apiInstance->cobvTxidPut($body, $txid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobVApi->cobvTxidPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CobVSolicitada**](../Model/CobVSolicitada.md)| Dados para geração da cobrança com vencimento. |
 **txid** | [**\Swagger\Client\Model\TxId**](../Model/.md)|  |

### Return type

[**\Swagger\Client\Model\CobVGerada**](../Model/CobVGerada.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

