# RTCCobrancaCondominio

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**tp_cobranca** | **string** | Tipo da cobrança:  * 01 - Condomínio Ordinário  * 02 - Condomínio Privativo  * 03 - Fundo De Promoção E Propaganda (FPP)  * 04 - Impostos e Taxas  * 05 - Fundo de Reserva  * 99 - Outra Cobrança |
**x_tp_cobranca** | **string** | Descrição do tipo da cobrança.  Somente deve ser informado quando tpCobranca &#x3D; 99 (Outra Cobrança). | [optional]
**v_cobranca** | **float** | Valor da cobrança em R$.  O somatório dos valores informados em vCobranca resultará no valor da operação (vServ).  vCobranca &#x3D; ? vDetCobranca (quando informado). |
**g_det_cobranca** | [**\ACBrAPI\Model\RTCDetCobrancaCondominio[]**](RTCDetCobrancaCondominio.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
