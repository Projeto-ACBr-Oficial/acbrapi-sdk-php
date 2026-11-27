# CteSimpSefazEmitSimp

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cnpj** | **string** | CNPJ do emitente.  Informar zeros não significativos.    ***Obrigatório caso o emitente seja pessoa jurídica***. | [optional]
**cpf** | **string** | CPF do emitente.  Informar zeros não significativos.  Usar com série específica 920-969 para emitente pessoa física com inscrição estadual.    ***Obrigatório caso o emitente seja pessoa física***. | [optional]
**ie** | **string** | Inscrição Estadual do Emitente.  A IE do emitente somente ficará sem informação para o caso do Regime Especial da NFF (tpEmis&#x3D;3).    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**iest** | **string** | Inscrição Estadual do Substituto Tributário. | [optional]
**x_nome** | **string** | Razão social ou Nome do emitente.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**x_fant** | **string** | Nome fantasia.    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**ender_emit** | [**\ACBrAPI\Model\CteSimpSefazEndeEmiSimp**](CteSimpSefazEndeEmiSimp.md) |  | [optional]
**crt** | **int** | Código do Regime Tributário. Informar:  * 1 - Simples Nacional;  * 2 - Simples Nacional, excesso sublimite de receita bruta;  * 3 - Regime Normal;  * 4 - Simples Nacional - Microempreendedor Individual (MEI).    *Caso não seja informado, será utilizado o do cadastro da empresa.* | [optional]
**isuf_emit** | **string** | Inscrição do emitente da Suframa.  Informar o número do Cadastro do emitente na Suframa. Campo obrigatório nas operações que se beneficiam de incentivos fiscais existentes nas áreas sob controle da SUFRAMA com alíquota zero da CBS referente aos arts. 451 e 466 da LC 214/25. | [optional]
**tp_regime_ibscbs** | **int** | Tipo de Regime de Apuração do IBS e da CBS.  * 1 - Contribuinte do Simples Nacional (CRT&#x3D;1 ou 2) com opção pelo regime regular do IBS e da CBS  * 2 - Contribuinte do Regime Normal (CRT&#x3D;3) com opção pendente pelo CRT&#x3D;”1 - Simples Nacional” sem regime regular do IBS e da CBS  * 3 - Contribuinte do Regime Normal (CRT&#x3D;3) com opção pendente pelo CRT&#x3D;”2-Simples Nacional, excesso sublimite de receita bruta” sem regime regular do IBS e da CBS  * 4 - Contribuinte do Regime Normal (CRT&#x3D;3) com opção pendente pelo Simples Nacional (CRT&#x3D;1 ou 2), com regime regular do IBS e da CBS | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
