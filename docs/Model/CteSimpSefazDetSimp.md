# CteSimpSefazDetSimp

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**n_item** | **int** | Número identificador do item agrupador da prestação. |
**c_mun_ini** | **string** | Código do Município de início da prestação.  Utilizar a tabela do IBGE. Informar 9999999 para operações com o exterior. |
**x_mun_ini** | **string** | Nome do Município do início da prestação.  Informar &#39;EXTERIOR&#39; para operações com o exterior. |
**c_mun_fim** | **string** | Código do Município de término da prestação.  Utilizar a tabela do IBGE. Informar 9999999 para operações com o exterior. |
**x_mun_fim** | **string** | Nome do Município do término da prestação.  Informar &#39;EXTERIOR&#39; para operações com o exterior. |
**v_prest** | **float** | Valorl da Prestação do Serviço. |
**v_prest_liq** | **float** | Valor Líquido da Prestação SEM tributos. | [optional]
**v_rec** | **float** | Valor a Receber. |
**comp** | [**\ACBrAPI\Model\CteSimpSefazCompSimp[]**](CteSimpSefazCompSimp.md) |  | [optional]
**ibscbs** | [**\ACBrAPI\Model\CteSimpSefazTribCTeSimp**](CteSimpSefazTribCTeSimp.md) |  | [optional]
**inf_nfe** | [**\ACBrAPI\Model\CteSimpSefazInfNFeSimp[]**](CteSimpSefazInfNFeSimp.md) |  | [optional]
**inf_doc_ant** | [**\ACBrAPI\Model\CteSimpSefazInfDocAntSimp[]**](CteSimpSefazInfDocAntSimp.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
