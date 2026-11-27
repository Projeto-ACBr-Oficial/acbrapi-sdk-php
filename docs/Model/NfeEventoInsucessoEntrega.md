# NfeEventoInsucessoEntrega

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**data_tentativa** | **\DateTime** | Data e hora do final da tentativa de entrega (tag &#x60;dhTentativaEntrega&#x60;). |
**numero_tentativa** | **int** | Número da tentativa de entrega que não teve sucesso (tag &#x60;nTentativa&#x60;). | [optional]
**motivo** | **int** | Motivo do insucesso (tag &#x60;tpMotivo&#x60;):  * 1 - Recebedor não encontrado  * 2 - Recusa do recebedor  * 3 - Endereço inexistente  * 4 - Outros (exige a &#x60;justificativa&#x60;) |
**justificativa** | **string** | Justificativa do motivo do insucesso (tag &#x60;xJustMotivo&#x60;). Obrigatória quando o &#x60;motivo&#x60; for &#x60;4&#x60;. | [optional]
**latitude** | **float** | Latitude do ponto da tentativa de entrega, em graus decimais (tag &#x60;latGPS&#x60;). | [optional]
**longitude** | **float** | Longitude do ponto da tentativa de entrega, em graus decimais (tag &#x60;longGPS&#x60;). | [optional]
**imagem** | **string** | Imagem capturada na tentativa de entrega, em Base64.    A API calcula o hash (tag &#x60;hashTentativaEntrega&#x60;) a partir da chave de acesso e desta imagem. Informe a imagem **ou** o &#x60;hash&#x60;. | [optional]
**hash** | **string** | Hash SHA-1, em Base64, da concatenação da chave de acesso com o Base64 da imagem capturada na tentativa de entrega (tag &#x60;hashTentativaEntrega&#x60;).    Informe o &#x60;hash&#x60; **ou** a &#x60;imagem&#x60;. | [optional]
**data_hash** | **\DateTime** | Data e hora da geração do hash (tag &#x60;dhHashTentativaEntrega&#x60;).    *Caso não seja informada, será utilizada a data e hora atual.* | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
