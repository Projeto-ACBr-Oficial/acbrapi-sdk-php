# RTCValoresBCImoveis

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tp_ajuste_bc_loc_imoveis** | **string** | Tipo de parcela não integrante da base de cálculo do IBS e da CBS  * 01 - Tributos inclusos no aluguel ou equivalente (Ex.: IPTU, Contribuição de melhoria) - apenas para NBS 1.1002.10.00 ou 1.1002.20.00  * 02 - Emolumento incluso no aluguel ou equivalente - apenas para NBS 1.1002.10.00 ou 1.1002.20.00  * 03 - Condomínio incluso no aluguel ou equivalente - apenas para NBS 1.1002.10.00 ou 1.1002.20.00  * 04 - Redutor Social - apenas para a NBS 1.1002.10.00  * 99 - Outras parcelas inclusas no aluguel ou equivalente |
**x_tp_ajuste_bc_loc_imoveis** | **string** | Descrição do tipo de parcela não integrante da base de cálculo do IBS e da CBS quando a opção for \&quot;99  &#x3D; Outras parcelas inclusas no aluguel ou equivalente\&quot;. | [optional]
**v_ajuste_bc_loc_imoveis** | **float** | Valor monetário utilizado para não inclusão na base de cálculo do IBS e da CBS da NFS-e que está sendo emitida (R$). (Informar o valor total da parcela não integrante da base de cálculo - IPTU, Condomínio, Redutor social, etc. -, não devendo ser inserido o valor proporcional do coproprietário). |

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
