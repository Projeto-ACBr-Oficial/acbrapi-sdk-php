# DocAjusteBC

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tp_ajuste_bc** | **int** | Tipo de Ajuste. |
**x_tp_ajuste_bc** | **string** | Descrição do ajuste quando o tipo informado exige detalhamento. | [optional]
**v_tot_doc** | **float** | Valor monetário total do documento informado (R$). |
**v_ajuste_aplic** | **float** | Valor monetário efetivamente utilizado para ajuste de base(s) de cálculo do valor do serviço da NFS-e que está sendo emitida (R$). |
**dt_emi_doc** | **\DateTime** | Data da emissão do documento dedutível. Ano, mês e dia (AAAA-MM-DD). | [optional]
**dt_comp_doc** | **\DateTime** | Data da competência do documento dedutível. Ano, mês e dia (AAAA-MM-DD). | [optional]
**d_fe_nacional** | [**\ACBrAPI\Model\RTCListaDocDFe**](RTCListaDocDFe.md) |  | [optional]
**doc_fiscal_outro** | [**\ACBrAPI\Model\RTCListaDocFiscalOutro**](RTCListaDocFiscalOutro.md) |  | [optional]
**doc_outro** | [**\ACBrAPI\Model\RTCListaDocOutro**](RTCListaDocOutro.md) |  | [optional]
**fornec** | [**\ACBrAPI\Model\InfoFornecDocDedRed**](InfoFornecDocDedRed.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
