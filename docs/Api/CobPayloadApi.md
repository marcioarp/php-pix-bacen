# Swagger\Client\CobPayloadApi

All URIs are relative to *https://pix.example.com/api/v2/*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cobvPixUrlAcessTokenGet**](CobPayloadApi.md#cobvpixurlacesstokenget) | **GET** /cobv/{pixUrlAcessToken} | Recuperar o payload JSON que representa a cobrança com vencimento.
[**pixUrlAcessTokenGet**](CobPayloadApi.md#pixurlacesstokenget) | **GET** /{pixUrlAcessToken} | Recuperar o payload JSON que representa a cobrança imediata.

# **cobvPixUrlAcessTokenGet**
> \Swagger\Client\Model\CobVPayload cobvPixUrlAcessTokenGet($pix_url_acess_token, $cod_mun, $dpp)

Recuperar o payload JSON que representa a cobrança com vencimento.

## Endpoint (location) que serve um payload que representa uma cobrança com vencimento.  No momento que o usuário devedor efetua a leitura de um QR Code dinâmico gerado pelo recebedor, esta URL será acessada e seu conteúdo consiste em uma estrutura JWS. As informações sobre a segurança no acesso às urls encontram-se no Manual de Segurança do Pix disponível em nesse __[link](https://www.bcb.gov.br/estabilidadefinanceira/comunicacaodados)__.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CobPayloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pix_url_acess_token = "pix_url_acess_token_example"; // string | 
$cod_mun = "cod_mun_example"; // string | Código baseado na Tabela de Códigos de Municípios do IBGE que apresenta a lista dos municípios brasileiros associados a um código composto de 7 dígitos, sendo os dois primeiros referentes ao código da Unidade da Federação.
$dpp = new \DateTime("2013-10-20"); // \DateTime | Data de pagamento pretendida

try {
    $result = $apiInstance->cobvPixUrlAcessTokenGet($pix_url_acess_token, $cod_mun, $dpp);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobPayloadApi->cobvPixUrlAcessTokenGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pix_url_acess_token** | **string**|  |
 **cod_mun** | **string**| Código baseado na Tabela de Códigos de Municípios do IBGE que apresenta a lista dos municípios brasileiros associados a um código composto de 7 dígitos, sendo os dois primeiros referentes ao código da Unidade da Federação. | [optional]
 **dpp** | **\DateTime**| Data de pagamento pretendida | [optional]

### Return type

[**\Swagger\Client\Model\CobVPayload**](../Model/CobVPayload.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/jose

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **pixUrlAcessTokenGet**
> \Swagger\Client\Model\CobPayload pixUrlAcessTokenGet($pix_url_acess_token)

Recuperar o payload JSON que representa a cobrança imediata.

## Endpoint (location) que serve um payload que representa uma cobrança imediata.  No momento que o usuário devedor efetua a leitura de um QR Code dinâmico gerado pelo recebedor, esta URL será acessada e seu conteúdo consiste em uma estrutura JWS. As informações sobre a segurança no acesso às urls encontram-se no Manual de Segurança do Pix disponível em nesse __[link](https://www.bcb.gov.br/estabilidadefinanceira/comunicacaodados)__.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\CobPayloadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$pix_url_acess_token = "pix_url_acess_token_example"; // string | 

try {
    $result = $apiInstance->pixUrlAcessTokenGet($pix_url_acess_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CobPayloadApi->pixUrlAcessTokenGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pix_url_acess_token** | **string**|  |

### Return type

[**\Swagger\Client\Model\CobPayload**](../Model/CobPayload.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/jose

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

