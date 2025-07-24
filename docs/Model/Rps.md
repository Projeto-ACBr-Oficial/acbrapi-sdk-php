# # Rps

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**rps** | [**\ACBrAPI\Model\RpsDados**](RpsDados.md) |  | [optional]
**competencia** | **\DateTime** |  | [optional]
**natureza_tributacao** | **int** | Natureza da tributação  1 - Simples Nacional;  2 - Fixo;  3 - Depósito em juízo;  4 - Exigibilidade suspensa por decisão judicial;  5 - Exigibilidade suspensa por procedimento administrativo;  6 - Isenção parcial. | [optional]
**prestador** | [**\ACBrAPI\Model\RpsDadosPrestador**](RpsDadosPrestador.md) |  | [optional]
**tomador** | [**\ACBrAPI\Model\RpsDadosTomador**](RpsDadosTomador.md) |  | [optional]
**intermediario** | [**\ACBrAPI\Model\RpsDadosIntermediario**](RpsDadosIntermediario.md) |  | [optional]
**construcao_civil** | [**\ACBrAPI\Model\RpsDadosConstrucaoCivil**](RpsDadosConstrucaoCivil.md) |  | [optional]
**servicos** | [**\ACBrAPI\Model\RpsDadosServico[]**](RpsDadosServico.md) |  |
**outras_informacoes** | **string** | Informações adicionais ao documento. | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
