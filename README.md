# SwaggerClient-php
A API Pix padroniza serviços oferecidos pelo PSP recebedor no contexto do arranjo Pix, como criação de cobrança, verificação de Pix recebidos, devolução e conciliação. Os serviços expostos pelo PSP recebedor permitem ao usuário recebedor estabelecer integração de sua automação com os serviços Pix do PSP.  # Evolução da API Pix As seguintes mudanças são esperadas e consideradas retro-compatíveis (_backwards-compatibility_):  - Adição de novos recursos na API Pix. - Adição de novos parâmetros opcionais a cobranças. - Adição de novos campos em respostas da API Pix. - Alteração da ordem de campos. - Adição de novos elementos em enumerações  Mudanças compatíveis não geram nova versão da API Pix. Clientes devem estar preparados para lidar com essas mudanças sem quebrar.  Mudanças incompatíveis geram nova versão da API Pix.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 2.1.2
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen
For more information, please visit [https://www.bcb.gov.br/estabilidadefinanceira/pagamentosinstantaneos](https://www.bcb.gov.br/estabilidadefinanceira/pagamentosinstantaneos)

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://pix.example.com/api/v2/*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CobApi* | [**cobGet**](docs/Api/CobApi.md#cobget) | **GET** /cob | Consultar lista de cobranças imediatas.
*CobApi* | [**cobPost**](docs/Api/CobApi.md#cobpost) | **POST** /cob | Criar cobrança imediata.
*CobApi* | [**cobTxidGet**](docs/Api/CobApi.md#cobtxidget) | **GET** /cob/{txid} | Consultar cobrança imediata.
*CobApi* | [**cobTxidPatch**](docs/Api/CobApi.md#cobtxidpatch) | **PATCH** /cob/{txid} | Revisar cobrança imediata.
*CobApi* | [**cobTxidPut**](docs/Api/CobApi.md#cobtxidput) | **PUT** /cob/{txid} | Criar cobrança imediata.
*CobPayloadApi* | [**cobvPixUrlAcessTokenGet**](docs/Api/CobPayloadApi.md#cobvpixurlacesstokenget) | **GET** /cobv/{pixUrlAcessToken} | Recuperar o payload JSON que representa a cobrança com vencimento.
*CobPayloadApi* | [**pixUrlAcessTokenGet**](docs/Api/CobPayloadApi.md#pixurlacesstokenget) | **GET** /{pixUrlAcessToken} | Recuperar o payload JSON que representa a cobrança imediata.
*CobVApi* | [**cobvGet**](docs/Api/CobVApi.md#cobvget) | **GET** /cobv | Consultar lista de cobranças com vencimento.
*CobVApi* | [**cobvTxidGet**](docs/Api/CobVApi.md#cobvtxidget) | **GET** /cobv/{txid} | Consultar cobrança com vencimento.
*CobVApi* | [**cobvTxidPatch**](docs/Api/CobVApi.md#cobvtxidpatch) | **PATCH** /cobv/{txid} | Revisar cobrança com vencimento.
*CobVApi* | [**cobvTxidPut**](docs/Api/CobVApi.md#cobvtxidput) | **PUT** /cobv/{txid} | Criar cobrança com vencimento.
*LoteCobVApi* | [**lotecobvGet**](docs/Api/LoteCobVApi.md#lotecobvget) | **GET** /lotecobv | Consultar lista de lotes de cobranças com vencimento.
*LoteCobVApi* | [**lotecobvIdGet**](docs/Api/LoteCobVApi.md#lotecobvidget) | **GET** /lotecobv/{id} | Consultar lote de cobranças com vencimento.
*LoteCobVApi* | [**lotecobvIdPut**](docs/Api/LoteCobVApi.md#lotecobvidput) | **PUT** /lotecobv/{id} | Criar lote de cobranças com vencimento.
*PayloadLocationApi* | [**locGet**](docs/Api/PayloadLocationApi.md#locget) | **GET** /loc | Consultar locations cadastradas.
*PayloadLocationApi* | [**locIdGet**](docs/Api/PayloadLocationApi.md#locidget) | **GET** /loc/{id} | Recuperar location do payload.
*PayloadLocationApi* | [**locIdTxidDelete**](docs/Api/PayloadLocationApi.md#locidtxiddelete) | **DELETE** /loc/{id}/txid | Desvincular um txid de uma location.
*PayloadLocationApi* | [**locPost**](docs/Api/PayloadLocationApi.md#locpost) | **POST** /loc | Criar location do payload.
*PixApi* | [**pixE2eidDevolucaoIdGet**](docs/Api/PixApi.md#pixe2eiddevolucaoidget) | **GET** /pix/{e2eid}/devolucao/{id} | Consultar devolução.
*PixApi* | [**pixE2eidDevolucaoIdPut**](docs/Api/PixApi.md#pixe2eiddevolucaoidput) | **PUT** /pix/{e2eid}/devolucao/{id} | Solicitar devolução.
*PixApi* | [**pixE2eidGet**](docs/Api/PixApi.md#pixe2eidget) | **GET** /pix/{e2eid} | Consultar Pix.
*PixApi* | [**pixGet**](docs/Api/PixApi.md#pixget) | **GET** /pix | Consultar Pix recebidos.
*WebhookApi* | [**webhookChaveDelete**](docs/Api/WebhookApi.md#webhookchavedelete) | **DELETE** /webhook/{chave} | Cancelar o webhook Pix.
*WebhookApi* | [**webhookChaveGet**](docs/Api/WebhookApi.md#webhookchaveget) | **GET** /webhook/{chave} | Exibir informações acerca do Webook Pix.
*WebhookApi* | [**webhookChavePut**](docs/Api/WebhookApi.md#webhookchaveput) | **PUT** /webhook/{chave} | Configurar o Webhook Pix.
*WebhookApi* | [**webhookGet**](docs/Api/WebhookApi.md#webhookget) | **GET** /webhook | Consultar webhooks cadastrados.

## Documentation For Models

 - [AbatimentoAplicado](docs/Model/AbatimentoAplicado.md)
 - [AllOfCobVValorDesconto](docs/Model/AllOfCobVValorDesconto.md)
 - [AllOfCobsConsultadasCobsItems](docs/Model/AllOfCobsConsultadasCobsItems.md)
 - [AllOfCobsVConsultadasCobsItems](docs/Model/AllOfCobsVConsultadasCobsItems.md)
 - [AllOfDadosDevedorDevedor](docs/Model/AllOfDadosDevedorDevedor.md)
 - [AllOfDadosRecebedorRecebedor](docs/Model/AllOfDadosRecebedorRecebedor.md)
 - [AllOfLotesCobVConsultadosLotesItems](docs/Model/AllOfLotesCobVConsultadosLotesItems.md)
 - [AllOfPayloadLocationConsultadasLocItems](docs/Model/AllOfPayloadLocationConsultadasLocItems.md)
 - [AllOfPixConsultadosPixItems](docs/Model/AllOfPixConsultadosPixItems.md)
 - [AllOfWebhooksConsultadosWebhooksItems](docs/Model/AllOfWebhooksConsultadosWebhooksItems.md)
 - [CobApresentacao](docs/Model/CobApresentacao.md)
 - [CobBase](docs/Model/CobBase.md)
 - [CobBaseInfoAdicionais](docs/Model/CobBaseInfoAdicionais.md)
 - [CobCompleta](docs/Model/CobCompleta.md)
 - [CobCriacao](docs/Model/CobCriacao.md)
 - [CobDataDeVencimento](docs/Model/CobDataDeVencimento.md)
 - [CobExpiracao](docs/Model/CobExpiracao.md)
 - [CobGerada](docs/Model/CobGerada.md)
 - [CobPayload](docs/Model/CobPayload.md)
 - [CobPayloadValor](docs/Model/CobPayloadValor.md)
 - [CobRevisada](docs/Model/CobRevisada.md)
 - [CobSolicitada](docs/Model/CobSolicitada.md)
 - [CobVCompleta](docs/Model/CobVCompleta.md)
 - [CobVGerada](docs/Model/CobVGerada.md)
 - [CobVPayload](docs/Model/CobVPayload.md)
 - [CobVPayloadValor](docs/Model/CobVPayloadValor.md)
 - [CobVRevisada](docs/Model/CobVRevisada.md)
 - [CobVSolicitada](docs/Model/CobVSolicitada.md)
 - [CobVValor](docs/Model/CobVValor.md)
 - [CobValor](docs/Model/CobValor.md)
 - [CobsConsultadas](docs/Model/CobsConsultadas.md)
 - [CobsVConsultadas](docs/Model/CobsVConsultadas.md)
 - [DadosComplementaresPessoa](docs/Model/DadosComplementaresPessoa.md)
 - [DadosDevedor](docs/Model/DadosDevedor.md)
 - [DadosRecebedor](docs/Model/DadosRecebedor.md)
 - [Devolucao](docs/Model/Devolucao.md)
 - [DevolucaoHorario](docs/Model/DevolucaoHorario.md)
 - [DevolucaoId](docs/Model/DevolucaoId.md)
 - [DevolucaoSolicitada](docs/Model/DevolucaoSolicitada.md)
 - [EndToEndId](docs/Model/EndToEndId.md)
 - [JuroAplicado](docs/Model/JuroAplicado.md)
 - [LoteCobVConsultado](docs/Model/LoteCobVConsultado.md)
 - [LoteCobVConsultadoCobsv](docs/Model/LoteCobVConsultadoCobsv.md)
 - [LoteCobVGerado](docs/Model/LoteCobVGerado.md)
 - [LotesCobVConsultados](docs/Model/LotesCobVConsultados.md)
 - [MultaAplicada](docs/Model/MultaAplicada.md)
 - [Paginacao](docs/Model/Paginacao.md)
 - [ParametrosConsultaCob](docs/Model/ParametrosConsultaCob.md)
 - [ParametrosConsultaLote](docs/Model/ParametrosConsultaLote.md)
 - [ParametrosConsultaPayloadLocation](docs/Model/ParametrosConsultaPayloadLocation.md)
 - [ParametrosConsultaPix](docs/Model/ParametrosConsultaPix.md)
 - [ParametrosConsultaWebhooks](docs/Model/ParametrosConsultaWebhooks.md)
 - [PayloadLocation](docs/Model/PayloadLocation.md)
 - [PayloadLocationCob](docs/Model/PayloadLocationCob.md)
 - [PayloadLocationCompleta](docs/Model/PayloadLocationCompleta.md)
 - [PayloadLocationConsultadas](docs/Model/PayloadLocationConsultadas.md)
 - [PayloadLocationId](docs/Model/PayloadLocationId.md)
 - [PayloadLocationSolicitada](docs/Model/PayloadLocationSolicitada.md)
 - [PessoaFisica](docs/Model/PessoaFisica.md)
 - [PessoaJuridica](docs/Model/PessoaJuridica.md)
 - [Pix](docs/Model/Pix.md)
 - [PixConsultados](docs/Model/PixConsultados.md)
 - [Revisao](docs/Model/Revisao.md)
 - [TxId](docs/Model/TxId.md)
 - [WebhookCompleto](docs/Model/WebhookCompleto.md)
 - [WebhookSolicitado](docs/Model/WebhookSolicitado.md)
 - [WebhooksConsultados](docs/Model/WebhooksConsultados.md)

## Documentation For Authorization


## OAuth2

- **Type**: OAuth
- **Flow**: application
- **Authorization URL**: 
- **Scopes**: 
 - ****: 


## Author

suporte.ti@bcb.gov.br
