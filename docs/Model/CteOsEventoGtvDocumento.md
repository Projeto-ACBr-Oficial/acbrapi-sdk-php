# CteOsEventoGtvDocumento

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**numero** | **string** | Número da GTV (tag &#x60;nDoc&#x60;). |
**id** | **string** | Identificador para diferenciar GTV de mesmo número: número da AIDF ou identificador interno da empresa (tag &#x60;id&#x60;). |
**serie** | **string** | Série (tag &#x60;serie&#x60;). | [optional]
**subserie** | **string** | Subsérie (tag &#x60;subserie&#x60;). | [optional]
**data_emissao** | **\DateTime** | Data de emissão (tag &#x60;dEmi&#x60;). |
**digito_verificador** | **string** | Dígito verificador (tag &#x60;nDV&#x60;). |
**quantidade_volumes** | **float** | Quantidade de volumes ou malotes (tag &#x60;qCarga&#x60;). |
**especies** | [**\ACBrAPI\Model\CteOsEventoGtvEspecie[]**](CteOsEventoGtvEspecie.md) | Espécies transportadas (grupo &#x60;infEspecie&#x60;). |
**remetente** | [**\ACBrAPI\Model\CteOsEventoGtvParticipante**](CteOsEventoGtvParticipante.md) |  |
**destinatario** | [**\ACBrAPI\Model\CteOsEventoGtvParticipante**](CteOsEventoGtvParticipante.md) |  |
**placa** | **string** | Placa do veículo (tag &#x60;placa&#x60;). | [optional]
**uf_veiculo** | **string** | UF em que o veículo está licenciado (tag &#x60;UF&#x60;). | [optional]
**rntrc** | **string** | RNTRC do transportador: 8 dígitos ou &#x60;ISENTO&#x60; (tag &#x60;RNTRC&#x60;). | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
