# NfseEvento

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tipo_evento** | **string** | Código do tipo de evento. Exemplos:  * &#x60;101101&#x60; - Cancelamento de NFS-e  * &#x60;101103&#x60; - Solicitação de análise fiscal para cancelamento de NFS-e  * &#x60;105102&#x60; - Cancelamento de NFS-e por substituição  * &#x60;105104&#x60; - Cancelamento de NFS-e deferido por análise fiscal  * &#x60;105105&#x60; - Cancelamento de NFS-e indeferido por análise fiscal  * &#x60;305101&#x60; - Cancelamento de NFS-e por ofício | [optional]
**descricao** | **string** | Descrição do tipo de evento. | [optional]
**numero_pedido** | **int** | Número do pedido de registro do evento. | [optional]
**data_hora** | **\DateTime** | Data e hora do registro do evento no Sistema Nacional NFS-e. | [optional]
**autor_cpf_cnpj** | **string** | CNPJ ou CPF do autor do evento. Vazio quando o evento é registrado  pelo Fisco sem identificação de CNPJ ou CPF. | [optional]
**xml** | **string** | XML do evento. | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
