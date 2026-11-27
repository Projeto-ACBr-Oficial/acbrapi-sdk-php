# NfeEventoAtorInteressado

## Propriedades

Nome | Tipo | Descrição | Comentários
------------ | ------------- | ------------- | -------------
**cpf_cnpj** | **string** | CNPJ ou CPF do transportador autorizado a baixar o XML da NF-e (tag &#x60;autXML&#x60;). |
**permite_autorizar_terceiros** | **bool** | Permite que o transportador autorizado neste evento autorize outros transportadores (subcontratados ou redespacho) a baixar a NF-e (tag &#x60;tpAutorizacao&#x60; &#x3D; 1).    Com &#x60;true&#x60;, a API inclui o texto fixo de condição de uso (tag &#x60;xCondUso&#x60;). Padrão: &#x60;false&#x60;. | [optional]

[[Voltar à lista de DTOs]](../../README.md#models) [[Voltar à lista de API]](../../README.md#endpoints) [[Voltar ao README]](../../README.md)
