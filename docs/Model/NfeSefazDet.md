# # NfeSefazDet

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**n_item** | **int** | Número do item do NF. |
**prod** | [**\ACBrAPI\Model\NfeSefazProd**](NfeSefazProd.md) |  |
**imposto** | [**\ACBrAPI\Model\NfeSefazImposto**](NfeSefazImposto.md) |  |
**imposto_devol** | [**\ACBrAPI\Model\NfeSefazImpostoDevol**](NfeSefazImpostoDevol.md) |  | [optional]
**inf_ad_prod** | **string** | Informações adicionais do produto (norma referenciada, informações complementares, etc). | [optional]
**obs_item** | [**\ACBrAPI\Model\NfeSefazObsItem**](NfeSefazObsItem.md) |  | [optional]
**v_item** | **float** | Valor total do Item, correspondente à sua participação no total da nota. A soma dos itens deverá corresponder ao total da nota. | [optional]
**dfe_referenciado** | [**\ACBrAPI\Model\NfeSefazDFeReferenciado**](NfeSefazDFeReferenciado.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
