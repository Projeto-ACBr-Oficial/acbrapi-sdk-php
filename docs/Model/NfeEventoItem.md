# NfeEventoItem

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**numero_item** | **int** | Número do item na NF-e referenciada (atributo &#x60;nItem&#x60; do grupo &#x60;det&#x60;). |
**valor_ibs** | **float** | Valor do IBS do item correspondente à quantidade informada (tag &#x60;vIBS&#x60;). |
**valor_cbs** | **float** | Valor da CBS do item correspondente à quantidade informada (tag &#x60;vCBS&#x60;). |
**quantidade** | **float** | Quantidade objeto do evento (tags &#x60;qtde&#x60;, &#x60;qPerecimento&#x60; ou &#x60;qNaoFornecida&#x60;, conforme o evento). |
**unidade** | **string** | Unidade da quantidade informada (tags &#x60;unidade&#x60;, &#x60;uPerecimento&#x60; ou &#x60;uNaoFornecida&#x60;, conforme o evento). |
**valor_credito_ibs** | **float** | Valor do crédito de IBS referente às aquisições a ser estornado, correspondente à quantidade informada.    *Obrigatório apenas no evento &#x60;112130&#x60; (Perecimento, perda, roubo ou furto durante o transporte contratado pelo fornecedor)*. | [optional]
**valor_credito_cbs** | **float** | Valor do crédito de CBS referente às aquisições a ser estornado, correspondente à quantidade informada.    *Obrigatório apenas no evento &#x60;112130&#x60; (Perecimento, perda, roubo ou furto durante o transporte contratado pelo fornecedor)*. | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
