# NfcomPedidoEvento

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tipo_evento** | **string** | Código do evento (tag &#x60;tpEvento&#x60;):  * &#x60;110300&#x60; - Vinculação do Pagamento (grupo &#x60;vinculacao_pagamento&#x60;)  * &#x60;110301&#x60; - Cancelamento da Vinculação do Pagamento (grupo &#x60;cancelamento_evento&#x60;) |
**vinculacao_pagamento** | [**\ACBrAPI\Model\NfcomEventoVinculacaoPagamento**](NfcomEventoVinculacaoPagamento.md) |  | [optional]
**cancelamento_evento** | [**\ACBrAPI\Model\NfcomEventoCancelamento**](NfcomEventoCancelamento.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
