# CtePedidoEvento

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tipo_evento** | **string** | Código do evento (tag &#x60;tpEvento&#x60;):  * &#x60;110160&#x60; - Registro Multimodal (grupo &#x60;registro_multimodal&#x60;)  * &#x60;110180&#x60; - Comprovante de Entrega do CT-e (grupo &#x60;comprovante_entrega&#x60;)  * &#x60;110181&#x60; - Cancelamento do Comprovante de Entrega do CT-e (grupo &#x60;cancelamento_evento&#x60;)  * &#x60;110190&#x60; - Insucesso na Entrega do CT-e (grupo &#x60;insucesso_entrega&#x60;)  * &#x60;110191&#x60; - Cancelamento do Insucesso de Entrega do CT-e (grupo &#x60;cancelamento_evento&#x60;) |
**cancelamento_evento** | [**\ACBrAPI\Model\CteEventoCancelamento**](CteEventoCancelamento.md) |  | [optional]
**insucesso_entrega** | [**\ACBrAPI\Model\CteEventoInsucessoEntrega**](CteEventoInsucessoEntrega.md) |  | [optional]
**comprovante_entrega** | [**\ACBrAPI\Model\CteEventoComprovanteEntrega**](CteEventoComprovanteEntrega.md) |  | [optional]
**registro_multimodal** | [**\ACBrAPI\Model\CteEventoRegistroMultimodal**](CteEventoRegistroMultimodal.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
