# MdfeEventoPagamentoOperacao

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**qtd_viagens** | **int** | Quantidade total de viagens realizadas com o pagamento do frete (tag &#x60;qtdViagens&#x60;). |
**nro_viagem** | **int** | Número de referência da viagem do MDF-e referenciado (tag &#x60;nroViagem&#x60;). |
**pagamentos** | [**\ACBrAPI\Model\MdfeSefazInfPag[]**](MdfeSefazInfPag.md) | Informações do pagamento do frete (tag &#x60;infPag&#x60;), no mesmo formato do grupo &#x60;infPag&#x60; da emissão do MDF-e rodoviário. O campo &#x60;indAltoDesemp&#x60; não é utilizado no evento. |

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
