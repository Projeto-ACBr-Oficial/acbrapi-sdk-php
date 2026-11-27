# NfeEventoConciliacaoPagamento

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**indicador** | **int** | Indicador da forma de pagamento (tag &#x60;indPag&#x60;):  * 0 - Pagamento à vista  * 1 - Pagamento a prazo | [optional]
**meio** | **string** | Meio de pagamento, com 2 dígitos (tag &#x60;tPag&#x60;), na mesma tabela do grupo &#x60;pag&#x60; da NF-e. |
**descricao** | **string** | Descrição do meio de pagamento (tag &#x60;xPag&#x60;). | [optional]
**valor** | **float** | Valor do pagamento (tag &#x60;vPag&#x60;). |
**data** | **\DateTime** | Data do pagamento (tag &#x60;dPag&#x60;). |
**cnpj_transacional** | **string** | CNPJ do estabelecimento onde o pagamento foi processado, quando diferente do emitente (tag &#x60;CNPJPag&#x60;). Informe junto com &#x60;uf_transacional&#x60;.    *Quando não informado e houver &#x60;cnpj_instituicao&#x60;, &#x60;bandeira&#x60; ou &#x60;autorizacao&#x60;, a API usa o CNPJ e a UF do emitente, como exige o leiaute do evento.* | [optional]
**uf_transacional** | **string** | UF do estabelecimento onde o pagamento foi processado (tag &#x60;UFPag&#x60;). | [optional]
**cnpj_instituicao** | **string** | CNPJ da instituição financeira, de pagamento, adquirente ou subadquirente (tag &#x60;CNPJIF&#x60;). | [optional]
**bandeira** | **string** | Bandeira da operadora de cartão, com 2 dígitos (tag &#x60;tBand&#x60;). | [optional]
**autorizacao** | **string** | Número de autorização da operação com cartão, PIX, boleto ou outro pagamento eletrônico (tag &#x60;cAut&#x60;). | [optional]
**cnpj_recebedor** | **string** | CNPJ do estabelecimento beneficiário do pagamento (tag &#x60;CNPJReceb&#x60;). | [optional]
**uf_recebedor** | **string** | UF do estabelecimento beneficiário do pagamento (tag &#x60;UFReceb&#x60;). | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
