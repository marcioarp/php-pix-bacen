# ParametrosConsultaCob

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**inicio** | [**\DateTime**](\DateTime.md) | Data inicial utilizada na consulta. Respeita RFC 3339. | 
**fim** | [**\DateTime**](\DateTime.md) | Data de fim utilizada na consulta. Respeita RFC 3339. | 
**cpf** | **string** | Filtro pelo CPF do devedor. Não pode ser utilizado ao mesmo tempo que o CNPJ. | [optional] 
**cnpj** | **string** | Filtro pelo CNPJ do devedor. Não pode ser utilizado ao mesmo tempo que o CPF. | [optional] 
**location_presente** | **bool** | Filtro pela existência de location vinculada. | [optional] 
**status** | **string** | Filtro pelo status das cobranças. | [optional] 
**paginacao** | [**\Swagger\Client\Model\Paginacao**](Paginacao.md) |  | 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

