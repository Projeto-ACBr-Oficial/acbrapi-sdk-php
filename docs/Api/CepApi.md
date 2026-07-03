# ACBrAPI\CepApi

Todas as URIs relativas a https://prod.acbr.api.br, exceto se a operação definir outra URI base.

| Método | Endpoint | Descrição |
| ------------- | ------------- | ------------- |
| [**consultarCep()**](CepApi.md#consultarCep) | **GET** /cep/{Cep} | Consultar endereço através do CEP |


## `consultarCep()`

```php
consultarCep($cep): \ACBrAPI\Model\CepEndereco
```

Consultar endereço através do CEP

**Informações adicionais**:  - Consumo: 0,1 unidade requisição.  - Em sandbox, a consulta é permitida somente para os seguintes CEP:    `18270000` Tatuí/SP    `01310300` São Paulo/SP    `22010000` Rio de Janeiro/RJ    `80020130` Curitiba/PR

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\CepApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cep = 'cep_example'; // string | CEP sem máscara.

try {
    $result = $apiInstance->consultarCep($cep);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CepApi->consultarCep: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cep** | **string**| CEP sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\CepEndereco**](../Model/CepEndereco.md)

### Autorização

[oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)
