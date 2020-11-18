# Swagger\Client\PixApi

All URIs are relative to *https://pix.example.com/api/v2/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pixE2eidDevolucaoIdGet**](PixApi.md#pixe2eiddevolucaoidget) | **GET** /pix/{e2eid}/devolucao/{id} | Consultar devolução.
[**pixE2eidDevolucaoIdPut**](PixApi.md#pixe2eiddevolucaoidput) | **PUT** /pix/{e2eid}/devolucao/{id} | Solicitar devolução.
[**pixE2eidGet**](PixApi.md#pixe2eidget) | **GET** /pix/{e2eid} | Consultar Pix.
[**pixGet**](PixApi.md#pixget) | **GET** /pix | Consultar Pix recebidos.

# **pixE2eidDevolucaoIdGet**
> \Swagger\Client\Model\Devolucao pixE2eidDevolucaoIdGet($e2eid, $id)

Consultar devolução.

Endpoint para consultar uma devolução através de um End To End ID do Pix e do ID da devolução

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$e2eid = new \Swagger\Client\Model\EndToEndId(); // \Swagger\Client\Model\EndToEndId | 
$id = new \Swagger\Client\Model\DevolucaoId(); // \Swagger\Client\Model\DevolucaoId | 

try {
    $result = $apiInstance->pixE2eidDevolucaoIdGet($e2eid, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PixApi->pixE2eidDevolucaoIdGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **e2eid** | [**\Swagger\Client\Model\EndToEndId**](../Model/.md)|  |
 **id** | [**\Swagger\Client\Model\DevolucaoId**](../Model/.md)|  |

### Return type

[**\Swagger\Client\Model\Devolucao**](../Model/Devolucao.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **pixE2eidDevolucaoIdPut**
> \Swagger\Client\Model\Devolucao pixE2eidDevolucaoIdPut($body, $e2eid, $id)

Solicitar devolução.

Endpoint para solicitar uma devolução através de um e2eid do Pix e do ID da devolução. O motivo que será atribuído à PACS.004 será \"Devolução solicitada pelo usuário recebedor do pagamento original\" cuja sigla é \"MD06\" de acordo com a aba RTReason da PACS.004 que consta no Catálogo de Mensagens do Pix.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DevolucaoSolicitada(); // \Swagger\Client\Model\DevolucaoSolicitada | Dados para pedido de devolução.
$e2eid = new \Swagger\Client\Model\EndToEndId(); // \Swagger\Client\Model\EndToEndId | 
$id = new \Swagger\Client\Model\DevolucaoId(); // \Swagger\Client\Model\DevolucaoId | 

try {
    $result = $apiInstance->pixE2eidDevolucaoIdPut($body, $e2eid, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PixApi->pixE2eidDevolucaoIdPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DevolucaoSolicitada**](../Model/DevolucaoSolicitada.md)| Dados para pedido de devolução. |
 **e2eid** | [**\Swagger\Client\Model\EndToEndId**](../Model/.md)|  |
 **id** | [**\Swagger\Client\Model\DevolucaoId**](../Model/.md)|  |

### Return type

[**\Swagger\Client\Model\Devolucao**](../Model/Devolucao.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **pixE2eidGet**
> \Swagger\Client\Model\Pix pixE2eidGet($e2eid)

Consultar Pix.

Endpoint para consultar um Pix através de um e2eid.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$e2eid = new \Swagger\Client\Model\EndToEndId(); // \Swagger\Client\Model\EndToEndId | 

try {
    $result = $apiInstance->pixE2eidGet($e2eid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PixApi->pixE2eidGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **e2eid** | [**\Swagger\Client\Model\EndToEndId**](../Model/.md)|  |

### Return type

[**\Swagger\Client\Model\Pix**](../Model/Pix.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **pixGet**
> \Swagger\Client\Model\PixConsultados pixGet($inicio, $fim, $txid, $tx_id_presente, $devolucao_presente, $cpf, $cnpj, $paginacao_pagina_atual, $paginacao_itens_por_pagina)

Consultar Pix recebidos.

Endpoint para consultar Pix recebidos

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure OAuth2 access token for authorization: OAuth2
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');

$apiInstance = new Swagger\Client\Api\PixApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inicio = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$fim = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | 
$txid = new \Swagger\Client\Model\TxId(); // \Swagger\Client\Model\TxId | 
$tx_id_presente = true; // bool | 
$devolucao_presente = true; // bool | 
$cpf = "cpf_example"; // string | 
$cnpj = "cnpj_example"; // string | 
$paginacao_pagina_atual = 0; // int | 
$paginacao_itens_por_pagina = 100; // int | 

try {
    $result = $apiInstance->pixGet($inicio, $fim, $txid, $tx_id_presente, $devolucao_presente, $cpf, $cnpj, $paginacao_pagina_atual, $paginacao_itens_por_pagina);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PixApi->pixGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inicio** | **\DateTime**|  |
 **fim** | **\DateTime**|  |
 **txid** | [**\Swagger\Client\Model\TxId**](../Model/.md)|  | [optional]
 **tx_id_presente** | **bool**|  | [optional]
 **devolucao_presente** | **bool**|  | [optional]
 **cpf** | **string**|  | [optional]
 **cnpj** | **string**|  | [optional]
 **paginacao_pagina_atual** | **int**|  | [optional] [default to 0]
 **paginacao_itens_por_pagina** | **int**|  | [optional] [default to 100]

### Return type

[**\Swagger\Client\Model\PixConsultados**](../Model/PixConsultados.md)

### Authorization

[OAuth2](../../README.md#OAuth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

