# MdfePedidoEvento

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tipo_evento** | **string** | Código do evento (tag &#x60;tpEvento&#x60;):  * &#x60;110116&#x60; - Pagamento da Operação de Transporte (grupo &#x60;pagamento_operacao&#x60;)  * &#x60;110118&#x60; - Alteração do Pagamento do Serviço (grupo &#x60;alteracao_pagamento&#x60;) |
**pagamento_operacao** | [**\ACBrAPI\Model\MdfeEventoPagamentoOperacao**](MdfeEventoPagamentoOperacao.md) |  | [optional]
**alteracao_pagamento** | [**\ACBrAPI\Model\MdfeEventoAlteracaoPagamento**](MdfeEventoAlteracaoPagamento.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
