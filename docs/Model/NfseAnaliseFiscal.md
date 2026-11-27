# NfseAnaliseFiscal

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**status** | **string** | Situação da solicitação:  * &#x60;em_analise&#x60; - evento registrado; o cancelamento aguarda a análise fiscal    do município  * &#x60;rejeitado&#x60; - o Sistema Nacional NFS-e recusou o evento (veja as mensagens) | [optional]
**codigo** | **int** | Código do motivo informado na solicitação. | [optional]
**motivo** | **string** | Motivo informado na solicitação. | [optional]
**data_hora** | **\DateTime** | Data e hora do processamento da solicitação. | [optional]
**mensagens** | [**\ACBrAPI\Model\NfseMensagemRetorno[]**](NfseMensagemRetorno.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
