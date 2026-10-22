# RTCInfoTributosAbrasf

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**c_loc_incid_ibscbs** | **string** | Código do município de incidência do IBS/CBS (tabela do IBGE).    Caso não seja informado, é determinado pelo local da operação (LC 214/25, art. 11), conforme o indicador da operação (&#x60;cIndOp&#x60;). Não confundir com o município de incidência do ISSQN (&#x60;tribMun.cLocIncid&#x60;). | [optional]
**v_bc** | **float** | Valor da base de cálculo (BC) do IBS/CBS (R$). | [optional]
**fed** | [**\ACBrAPI\Model\RTCInfoTributosAbrasfFed**](RTCInfoTributosAbrasfFed.md) |  | [optional]
**uf** | [**\ACBrAPI\Model\RTCInfoTributosAbrasfUF**](RTCInfoTributosAbrasfUF.md) |  | [optional]
**mun** | [**\ACBrAPI\Model\RTCInfoTributosAbrasfMun**](RTCInfoTributosAbrasfMun.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
