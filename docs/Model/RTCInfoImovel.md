# RTCInfoImovel

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_mun** | **string** | Código do município do endereço do imóvel (Tabela do IBGE).  *Disponível a partir da NT 009 (leiaute 009.1.01).* | [optional]
**g_locacao** | [**\ACBrAPI\Model\RTCLocacaoImovel**](RTCLocacaoImovel.md) |  | [optional]
**g_unid_imob** | [**\ACBrAPI\Model\RTCUnidadesImobiliarias[]**](RTCUnidadesImobiliarias.md) |  | [optional]
**insc_imob_fisc** | **string** | &#x60;Deprecated&#x60;    **Propriedade depreciada** a partir da NT 009 (leiaute 009.1.01).    *Utilize &#x60;IBSCBS.imovel.gUnidImob[].inscImobFisc&#x60;*.  Inscrição imobiliária fiscal (código fornecido pela Prefeitura Municipal para a identificação da obra ou para fins de recolhimento do IPTU). | [optional]
**c_cib** | **string** | &#x60;Deprecated&#x60;    **Propriedade depreciada** a partir da NT 009 (leiaute 009.1.01).    *Utilize &#x60;IBSCBS.imovel.gUnidImob[].cCIB&#x60;*.  Código do Cadastro Imobiliário Brasileiro - CIB. | [optional]
**end** | [**\ACBrAPI\Model\EnderObraEvento**](EnderObraEvento.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
