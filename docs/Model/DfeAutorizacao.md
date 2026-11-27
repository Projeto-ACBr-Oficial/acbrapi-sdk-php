# DfeAutorizacao

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**digest_value** | **string** | Digest Value do DF-e processado. Utilizado para conferir a integridade do DF-e original. | [optional]
**alertas** | [**\ACBrAPI\Model\DfeAlerta[]**](DfeAlerta.md) | Lista de mensagens (alertas) da SEFAZ retornadas no protocolo de autorização.    A partir da NT 2026.002 o protocolo da NF-e/NFC-e pode trazer até 5 pares  cMsg/xMsg, por exemplo quando o uso é autorizado com alerta (&#x60;codigo_status&#x60; 120).  Os campos &#x60;codigo_mensagem&#x60; e &#x60;mensagem&#x60; continuam trazendo apenas o primeiro par.    Omitido quando o protocolo não traz mensagens. | [optional]
**id** | **string** | ID único gerado pela API para este evento. | [optional]
**ambiente** | **string** | Identificação do ambiente. | [optional]
**status** | **string** | Status do Evento. | [optional]
**autor** | [**\ACBrAPI\Model\DfeAutorEvento**](DfeAutorEvento.md) |  | [optional]
**chave_acesso** | **string** | Chave de Acesso do documento vinculado ao evento. | [optional]
**data_evento** | **\DateTime** | Data e hora do Evento. | [optional]
**numero_sequencial** | **int** | Sequencial do evento para o mesmo tipo de evento. | [optional]
**data_recebimento** | **\DateTime** | Data e hora do recebimento do Evento pela SEFAZ. | [optional]
**codigo_status** | **int** | Código do status de registro do Evento. | [optional]
**motivo_status** | **string** | Descrição literal do status do registro do Evento. | [optional]
**numero_protocolo** | **string** | Número do Protocolo de registro do Evento. | [optional]
**codigo_mensagem** | **int** | Código da Mensagem. | [optional]
**mensagem** | **string** | Mensagem da SEFAZ para o emissor ou, na inutilização, aviso da API (ex.: serviço  de inutilização desativado pela SEFAZ na UF do emitente). | [optional]
**tipo_evento** | **string** |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
