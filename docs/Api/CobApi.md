# Swagger\Client\CobApi

All URIs are relative to *https://pix.example.com/api/v2/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cobGet**](CobApi.md#cobget) | **GET** /cob | Consultar lista de cobranças imediatas.
[**cobPost**](CobApi.md#cobpost) | **POST** /cob | Criar cobrança imediata.
[**cobTxidGet**](CobApi.md#cobtxidget) | **GET** /cob/{txid} | Consultar cobrança imediata.
[**cobTxidPatch**](CobApi.md#cobtxidpatch) | **PATCH** /cob/{txid} | Revisar cobrança imediata.
[**cobTxidPut**](CobApi.md#cobtxidput) | **PUT** /cob/{txid} | Criar cobrança imediata.

# **cobGet**
> \Swagger\Client\Model\CobsConsultadas cobGet($inicio, $fim, $cpf, $cnpj, $location_presente, $status, $paginacao_pagina_atual, $paginacao_itens_por_pagina)

Consultar lista de cobranças imediatas.

Endpoint para consultar cobranças imediatas através de parâmetros como início, fim, cpf, cnpj e status.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CobApi(
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
$paginacao_pagina_atual = 0; // int | 
$paginacao_itens_por_pagina = 100; // int | 

try {
    $result = $apiInstance->cobGet($inicio, $fim, $cpf, $cnpj, $location_presente, $status, $paginacao_pagina_atual, $paginacao_itens_por_pagina);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobApi->cobGet: ', $e->getMessage(), PHP_EOL;
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
 **paginacao_pagina_atual** | **int**|  | [optional] [default to 0]
 **paginacao_itens_por_pagina** | **int**|  | [optional] [default to 100]

### Return type

[**\Swagger\Client\Model\CobsConsultadas**](../Model/CobsConsultadas.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **cobPost**
> \Swagger\Client\Model\CobGerada cobPost($body)

Criar cobrança imediata.

Endpoint para criar uma cobrança imediata, neste caso, o txid deve ser definido pelo PSP.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CobApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\CobSolicitada(); // \Swagger\Client\Model\CobSolicitada | Dados para geração da cobrança imediata.

try {
    $result = $apiInstance->cobPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobApi->cobPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CobSolicitada**](../Model/CobSolicitada.md)| Dados para geração da cobrança imediata. |

### Return type

[**\Swagger\Client\Model\CobGerada**](../Model/CobGerada.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **cobTxidGet**
> \Swagger\Client\Model\CobCompleta cobTxidGet($txid, $revisao)

Consultar cobrança imediata.

Endpoint para consultar uma cobrança através de um determinado txid.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CobApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$txid = new \Swagger\Client\Model\TxId(); // \Swagger\Client\Model\TxId | 
$revisao = new \Swagger\Client\Model\Revisao(); // \Swagger\Client\Model\Revisao | 

try {
    $result = $apiInstance->cobTxidGet($txid, $revisao);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobApi->cobTxidGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **txid** | [**\Swagger\Client\Model\TxId**](../Model/.md)|  |
 **revisao** | [**\Swagger\Client\Model\Revisao**](../Model/.md)|  | [optional]

### Return type

[**\Swagger\Client\Model\CobCompleta**](../Model/CobCompleta.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **cobTxidPatch**
> \Swagger\Client\Model\CobGerada cobTxidPatch($body, $txid)

Revisar cobrança imediata.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CobApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\CobRevisada(); // \Swagger\Client\Model\CobRevisada | Dados para geração da cobrança.
$txid = new \Swagger\Client\Model\TxId(); // \Swagger\Client\Model\TxId | 

try {
    $result = $apiInstance->cobTxidPatch($body, $txid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobApi->cobTxidPatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CobRevisada**](../Model/CobRevisada.md)| Dados para geração da cobrança. |
 **txid** | [**\Swagger\Client\Model\TxId**](../Model/.md)|  |

### Return type

[**\Swagger\Client\Model\CobGerada**](../Model/CobGerada.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **cobTxidPut**
> \Swagger\Client\Model\CobGerada cobTxidPut($body, $txid)

Criar cobrança imediata.

Endpoint para criar uma cobrança imediata.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\CobApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\CobSolicitada(); // \Swagger\Client\Model\CobSolicitada | Dados para geração da cobrança imediata.
$txid = new \Swagger\Client\Model\TxId(); // \Swagger\Client\Model\TxId | 

try {
    $result = $apiInstance->cobTxidPut($body, $txid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobApi->cobTxidPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CobSolicitada**](../Model/CobSolicitada.md)| Dados para geração da cobrança imediata. |
 **txid** | [**\Swagger\Client\Model\TxId**](../Model/.md)|  |

### Return type

[**\Swagger\Client\Model\CobGerada**](../Model/CobGerada.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

