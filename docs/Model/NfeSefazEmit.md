# NfeSefazEmit

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **string** | Número do CNPJ do emitente.    ***Obrigatório caso o emitente seja pessoa jurídica***. | [optional]
**cpf** | **string** | Número do CPF do emitente.    ***Obrigatório caso o emitente seja pessoa física***. | [optional]
**x_nome** | **string** | Razão Social ou Nome do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**x_fant** | **string** | Nome fantasia.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**ender_emit** | [**\ACBrAPI\Model\NfeSefazEnderEmi**](NfeSefazEnderEmi.md) |  | [optional]
**ie** | **string** | Inscrição Estadual do Emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**iest** | **string** | Inscricao Estadual do Substituto Tributário.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**im** | **string** | Inscrição Municipal.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**cnae** | **string** | CNAE Fiscal.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**crt** | **int** | Código de Regime Tributário.  Este campo será obrigatoriamente preenchido com:  * 1 - Simples Nacional  * 2 - Simples Nacional - excesso de sublimite de receita bruta  * 3 - Regime Normal  * 4 - Simples Nacional - Microempreendedor individual - MEI    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**tp_regime_ibscbs** | **int** | Tipo de Regime de Apuração do IBS e da CBS:  * 1 - Contribuinte do Simples Nacional (CRT&#x3D;1 ou 2) com opção pelo regime regular do IBS e da CBS  * 2 - Contribuinte do Regime Normal (CRT&#x3D;3) com opção pendente pelo CRT&#x3D;\&quot;1-Simples Nacional\&quot; sem regime regular do IBS e da CBS  * 3 - Contribuinte do Regime Normal (CRT&#x3D;3) com opção pendente pelo CRT&#x3D;\&quot;2-Simples Nacional, excesso sublimite de receita bruta\&quot; sem regime regular do IBS e da CBS  * 4 - Contribuinte do Regime Normal (CRT&#x3D;3) com opção pendente pelo Simples Nacional (CRT&#x3D;1 ou 2), com regime regular do IBS e da CBS | [optional]
**isuf_emit** | **string** | Inscrição do emitente na Suframa. | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
