# NfcomEventoVinculacaoPagamento

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**id_transacao** | **string** | Identificador da transação financeira, conforme o meio de pagamento (tag &#x60;idTransacao&#x60;). |
**meio_pagamento** | **string** | Código do meio de pagamento, com 2 dígitos (tag &#x60;tpMeioPgto&#x60;), conforme a Tabela Nacional de Códigos de Meios de Pagamento (Informe Técnico 2026.001 dos DF-e). |
**cnpj_recebedor** | **string** | CNPJ completo do recebedor do pagamento (tag &#x60;CNPJReceb&#x60;). |
**cnpj_base_psp** | **string** | CNPJ base (8 primeiras posições) da instituição financeira ou de pagamento (tag &#x60;CNPJBasePSP&#x60;). |

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
