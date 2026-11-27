# NfeEventoComprovanteEntrega

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**data_entrega** | **\DateTime** | Data e hora do final da entrega (tag &#x60;dhEntrega&#x60;). |
**documento** | **string** | Número do documento de identificação da pessoa que recebeu a mercadoria e assinou o comprovante (tag &#x60;nDoc&#x60;). |
**nome** | **string** | Nome da pessoa que recebeu a mercadoria e assinou o comprovante (tag &#x60;xNome&#x60;). |
**latitude** | **float** | Latitude do ponto de entrega, em graus decimais (tag &#x60;latGPS&#x60;). | [optional]
**longitude** | **float** | Longitude do ponto de entrega, em graus decimais (tag &#x60;longGPS&#x60;). | [optional]
**imagem** | **string** | Imagem capturada na entrega (foto, assinatura etc.), em Base64.    A API calcula o hash (tag &#x60;hashComprovante&#x60;) a partir da chave de acesso e desta imagem. Informe a imagem **ou** o &#x60;hash&#x60;. | [optional]
**hash** | **string** | Hash SHA-1, em Base64, da concatenação da chave de acesso com o Base64 da imagem capturada na entrega (tag &#x60;hashComprovante&#x60;).    Informe o &#x60;hash&#x60; **ou** a &#x60;imagem&#x60;. | [optional]
**data_hash** | **\DateTime** | Data e hora da geração do hash (tag &#x60;dhHashComprovante&#x60;).    *Caso não seja informada, será utilizada a data e hora atual.* | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
