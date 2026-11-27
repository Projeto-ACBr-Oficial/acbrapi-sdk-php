# CteEventoInsucessoEntrega

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**data_tentativa** | **\DateTime** | Data e hora da tentativa de entrega (tag &#x60;dhTentativaEntrega&#x60;). |
**numero_tentativa** | **int** | Número da tentativa de entrega (tag &#x60;nTentativa&#x60;). | [optional]
**motivo** | **int** | Motivo do insucesso (tag &#x60;tpMotivo&#x60;):  * &#x60;1&#x60; - Recebedor não encontrado  * &#x60;2&#x60; - Recusa do recebedor  * &#x60;3&#x60; - Endereço inexistente  * &#x60;4&#x60; - Outros (exige &#x60;justificativa&#x60;) |
**justificativa** | **string** | Justificativa do motivo do insucesso (tag &#x60;xJustMotivo&#x60;). Obrigatória quando o &#x60;motivo&#x60; for &#x60;4&#x60;. | [optional]
**latitude** | **float** | Latitude do ponto de entrega, em graus decimais. Informe junto com a &#x60;longitude&#x60;. | [optional]
**longitude** | **float** | Longitude do ponto de entrega, em graus decimais. Informe junto com a &#x60;latitude&#x60;. | [optional]
**imagem** | **string** | Imagem capturada na tentativa de entrega, em Base64. A API calcula o hash (tag &#x60;hashTentativaEntrega&#x60;) a partir dela.  Informe a &#x60;imagem&#x60; ou o &#x60;hash&#x60;, não os dois. Neste evento o hash é opcional. | [optional]
**hash** | **string** | Hash já calculado da tentativa de entrega: SHA-1, em Base64, da chave de acesso do CT-e concatenada com o Base64 da imagem. | [optional]
**data_hash** | **\DateTime** | Data e hora de geração do hash (tag &#x60;dhHashTentativaEntrega&#x60;). Se não for informada, a API usa a data e hora do envio. | [optional]
**chaves_nfe** | **string[]** | Chaves de acesso das NF-e que não foram entregues (grupo &#x60;infEntrega&#x60;). | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
