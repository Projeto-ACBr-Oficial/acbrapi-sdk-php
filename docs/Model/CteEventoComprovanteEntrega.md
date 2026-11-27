# CteEventoComprovanteEntrega

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**data_entrega** | **\DateTime** | Data e hora da conclusão da entrega (tag &#x60;dhEntrega&#x60;). |
**documento_recebedor** | **string** | Número do documento de identificação da pessoa que recebeu a entrega (tag &#x60;nDoc&#x60;). |
**nome_recebedor** | **string** | Nome da pessoa que recebeu a entrega (tag &#x60;xNome&#x60;). |
**latitude** | **float** | Latitude do ponto de entrega, em graus decimais. Informe junto com a &#x60;longitude&#x60;. | [optional]
**longitude** | **float** | Longitude do ponto de entrega, em graus decimais. Informe junto com a &#x60;latitude&#x60;. | [optional]
**imagem** | **string** | Imagem capturada na entrega (assinatura, digital, foto etc.), em Base64. A API calcula o hash (tag &#x60;hashEntrega&#x60;) a partir dela.  Informe a &#x60;imagem&#x60; ou o &#x60;hash&#x60;: um dos dois é obrigatório. | [optional]
**hash** | **string** | Hash já calculado da entrega: SHA-1, em Base64, da chave de acesso do CT-e concatenada com o Base64 da imagem. | [optional]
**data_hash** | **\DateTime** | Data e hora de geração do hash (tag &#x60;dhHashEntrega&#x60;). Se não for informada, a API usa a data e hora do envio. | [optional]
**chaves_nfe** | **string[]** | Chaves de acesso das NF-e entregues ao destinatário (grupo &#x60;infEntrega&#x60;). Informe apenas para CT-e com tipo de serviço normal. | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
