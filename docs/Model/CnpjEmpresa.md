# # CnpjEmpresa

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **string** | Número de inscrição do CNPJ. | [optional]
**razao_social** | **string** | Nome empresarial da pessoa jurídica. | [optional]
**nome_fantasia** | **string** | Corresponde ao nome fantasia. | [optional]
**data_inicio_atividade** | **\DateTime** | Data de início da atividade. | [optional]
**matriz** | **bool** | Indicador de matriz/filial:  * &#x60;true&#x60; - É matriz  * &#x60;false&#x60; - É filial | [optional]
**natureza_juridica** | [**\ACBrAPI\Model\CnpjNaturezaJuridica**](CnpjNaturezaJuridica.md) |  | [optional]
**capital_social** | **float** | Capital social da empresa. | [optional]
**porte** | [**\ACBrAPI\Model\CnpjPorteEmpresa**](CnpjPorteEmpresa.md) |  | [optional]
**ente_federativo_responsavel** | **string** | O ente federativo responsável é preenchido para os casos de órgãos e  entidades do grupo de natureza jurídica 1XXX. Para as demais naturezas,  este atributo fica em branco. | [optional]
**situacao_cadastral** | [**\ACBrAPI\Model\CnpjSituacaoCadastral**](CnpjSituacaoCadastral.md) |  | [optional]
**motivo_situacao_cadastral** | [**\ACBrAPI\Model\CnpjMotivoSituacaoCadastral**](CnpjMotivoSituacaoCadastral.md) |  | [optional]
**nome_da_cidade_no_exterior** | **string** | Nome da cidade no exterior. | [optional]
**pais** | [**\ACBrAPI\Model\CnpjPais**](CnpjPais.md) |  | [optional]
**atividade_principal** | [**\ACBrAPI\Model\CnpjCnae**](CnpjCnae.md) |  | [optional]
**atividades_secundarias** | [**\ACBrAPI\Model\CnpjCnaeSecundario[]**](CnpjCnaeSecundario.md) |  | [optional]
**endereco** | [**\ACBrAPI\Model\CnpjEndereco**](CnpjEndereco.md) |  | [optional]
**telefones** | [**\ACBrAPI\Model\CnpjTelefone[]**](CnpjTelefone.md) |  | [optional]
**email** | **string** | E-mail do contribuinte. | [optional]
**situacao_especial** | [**\ACBrAPI\Model\CnpjSituacaoEspecial**](CnpjSituacaoEspecial.md) |  | [optional]
**simples** | [**\ACBrAPI\Model\CnpjOpcaoSimples**](CnpjOpcaoSimples.md) |  | [optional]
**simei** | [**\ACBrAPI\Model\CnpjOpcaoSimei**](CnpjOpcaoSimei.md) |  | [optional]
**socios** | [**\ACBrAPI\Model\CnpjSocio[]**](CnpjSocio.md) |  | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
