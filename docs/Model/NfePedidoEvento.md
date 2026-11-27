# NfePedidoEvento

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tipo_evento** | **string** | Código do evento (tag &#x60;tpEvento&#x60;):  * &#x60;110001&#x60; - Cancelamento de Evento (grupo &#x60;cancelamento_evento&#x60;)  * &#x60;110130&#x60; - Comprovante de Entrega da NF-e (grupo &#x60;comprovante_entrega&#x60;)  * &#x60;110131&#x60; - Cancelamento do Comprovante de Entrega da NF-e (grupo &#x60;cancelamento_evento&#x60;)  * &#x60;110150&#x60; - Ator Interessado na NF-e (grupo &#x60;ator_interessado&#x60;)  * &#x60;110192&#x60; - Insucesso na Entrega da NF-e (grupo &#x60;insucesso_entrega&#x60;)  * &#x60;110193&#x60; - Cancelamento do Insucesso na Entrega da NF-e (grupo &#x60;cancelamento_evento&#x60;)  * &#x60;110300&#x60; - Vinculação de Pagamento (grupo &#x60;vinculacao_pagamento&#x60;)  * &#x60;110750&#x60; - Conciliação Financeira, ECONF (grupo &#x60;conciliacao_financeira&#x60;)  * &#x60;110751&#x60; - Cancelamento da Conciliação Financeira (grupo &#x60;cancelamento_evento&#x60;)  * &#x60;111500&#x60; - Pedido de Prorrogação do ICMS, 1º prazo (grupo &#x60;prorrogacao_icms&#x60;)  * &#x60;111501&#x60; - Pedido de Prorrogação do ICMS, 2º prazo (grupo &#x60;prorrogacao_icms&#x60;)  * &#x60;111502&#x60; - Cancelamento do Pedido de Prorrogação, 1º prazo (grupo &#x60;cancelamento_evento&#x60;)  * &#x60;111503&#x60; - Cancelamento do Pedido de Prorrogação, 2º prazo (grupo &#x60;cancelamento_evento&#x60;)  * &#x60;112110&#x60; - Informação de efetivo pagamento integral para liberar crédito presumido do adquirente (sem grupo)  * &#x60;112120&#x60; - Importação em ALC/ZFM não convertida em isenção (grupo &#x60;importacao_zfm_nao_convertida&#x60;)  * &#x60;112130&#x60; - Perecimento, perda, roubo ou furto durante o transporte contratado pelo fornecedor (grupo &#x60;perecimento_fornecedor&#x60;)  * &#x60;112140&#x60; - Fornecimento não realizado com pagamento antecipado (grupo &#x60;fornecimento_nao_realizado&#x60;)  * &#x60;112150&#x60; - Atualização da Data de Previsão de Entrega (grupo &#x60;atualizacao_previsao_entrega&#x60;) |
**cancelamento_evento** | [**\ACBrAPI\Model\NfeEventoCancelamento**](NfeEventoCancelamento.md) |  | [optional]
**importacao_zfm_nao_convertida** | [**\ACBrAPI\Model\NfeEventoItens**](NfeEventoItens.md) |  | [optional]
**perecimento_fornecedor** | [**\ACBrAPI\Model\NfeEventoItens**](NfeEventoItens.md) |  | [optional]
**fornecimento_nao_realizado** | [**\ACBrAPI\Model\NfeEventoItens**](NfeEventoItens.md) |  | [optional]
**atualizacao_previsao_entrega** | [**\ACBrAPI\Model\NfeEventoPrevisaoEntrega**](NfeEventoPrevisaoEntrega.md) |  | [optional]
**insucesso_entrega** | [**\ACBrAPI\Model\NfeEventoInsucessoEntrega**](NfeEventoInsucessoEntrega.md) |  | [optional]
**prorrogacao_icms** | [**\ACBrAPI\Model\NfeEventoProrrogacao**](NfeEventoProrrogacao.md) |  | [optional]
**comprovante_entrega** | [**\ACBrAPI\Model\NfeEventoComprovanteEntrega**](NfeEventoComprovanteEntrega.md) |  | [optional]
**ator_interessado** | [**\ACBrAPI\Model\NfeEventoAtorInteressado**](NfeEventoAtorInteressado.md) |  | [optional]
**vinculacao_pagamento** | [**\ACBrAPI\Model\NfeEventoVinculacaoPagamento**](NfeEventoVinculacaoPagamento.md) |  | [optional]
**conciliacao_financeira** | [**\ACBrAPI\Model\NfeEventoConciliacao**](NfeEventoConciliacao.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
