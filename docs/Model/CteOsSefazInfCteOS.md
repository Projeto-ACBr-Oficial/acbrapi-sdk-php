# # CteOsSefazInfCteOS

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**versao** | **string** | Versão do leiaute.  Ex: \&quot;4.00\&quot;. |
**id** | **string** | Identificador da tag a ser assinada.  Informar a chave de acesso do CT-e OS e precedida do literal \&quot;CTe\&quot;.    *Geramos automaticamente quando nenhum valor é informado.* | [optional]
**ide** | [**\ACBrAPI\Model\CteOsSefazIdeOS**](CteOsSefazIdeOS.md) |  |
**compl** | [**\ACBrAPI\Model\CteOsSefazComplOS**](CteOsSefazComplOS.md) |  | [optional]
**emit** | [**\ACBrAPI\Model\CteOsSefazEmitOS**](CteOsSefazEmitOS.md) |  |
**toma** | [**\ACBrAPI\Model\CteOsSefazTomaOS**](CteOsSefazTomaOS.md) |  | [optional]
**v_prest** | [**\ACBrAPI\Model\CteOsSefazVPrestOS**](CteOsSefazVPrestOS.md) |  |
**imp** | [**\ACBrAPI\Model\CteOsSefazInfCteImpOS**](CteOsSefazInfCteImpOS.md) |  |
**pgto_vinc** | [**\ACBrAPI\Model\CteOsSefazPgtoVincOS**](CteOsSefazPgtoVincOS.md) |  | [optional]
**inf_cte_norm** | [**\ACBrAPI\Model\CteOsSefazInfCTeNormOS**](CteOsSefazInfCTeNormOS.md) |  | [optional]
**inf_cte_comp** | [**\ACBrAPI\Model\CteOsSefazInfCteCompOS[]**](CteOsSefazInfCteCompOS.md) |  | [optional]
**aut_xml** | [**\ACBrAPI\Model\CteOsSefazAutXMLOS[]**](CteOsSefazAutXMLOS.md) |  | [optional]
**inf_resp_tec** | [**\ACBrAPI\Model\CteOsSefazRespTecOS**](CteOsSefazRespTecOS.md) |  | [optional]
**tp_pag_ant** | **int** | Tipo Pagamento ou Pagamento Antecipado.  Informar:  * 1 - Pagamento Antecipado  * 3 - Fornecimento com pagamento realizado anteriormente  Este campo é opcional e apenas deve ser informado quando pagamento que ocorre antes da prestação do serviço e na DFe de fornecimento associada a esses pagamentos, demais hipóteses de prestação de serviço sem antecipação não devem preencher. | [optional]
**g_pag_antecipado** | [**\ACBrAPI\Model\CteOsSefazGPagAntecipadoOS**](CteOsSefazGPagAntecipadoOS.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
