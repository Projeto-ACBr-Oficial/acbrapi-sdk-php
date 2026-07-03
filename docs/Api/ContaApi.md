# ACBrAPI\ContaApi

Todas as URIs relativas a https://prod.acbr.api.br, exceto se a operação definir outra URI base.

| Método | Endpoint | Descrição |
| ------------- | ------------- | ------------- |
| [**consultarCotaConta()**](ContaApi.md#consultarCotaConta) | **GET** /conta/cotas/{nome} | Consultar o limite de uso e o consumo de uma cota específica. |
| [**consultarCotaPrePago()**](ContaApi.md#consultarCotaPrePago) | **GET** /conta/cotas/prepago | Consultar o resumo da cota de créditos pré-pagos. |
| [**listarCotasConta()**](ContaApi.md#listarCotasConta) | **GET** /conta/cotas | Consultar os limites de uso e consumo das cotas disponíveis, exceto a cota de créditos pré-pagos. |
| [**listarExtratoCreditosConta()**](ContaApi.md#listarExtratoCreditosConta) | **GET** /conta/extrato | Consultar o extrato de movimentação de créditos do tenant atual. |


## `consultarCotaConta()`

```php
consultarCotaConta($nome): \ACBrAPI\Model\ContaCota
```

Consultar o limite de uso e o consumo de uma cota específica.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\ContaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$nome = 'nome_example'; // string | Nome da cota a ser consultada.

try {
    $result = $apiInstance->consultarCotaConta($nome);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContaApi->consultarCotaConta: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **nome** | **string**| Nome da cota a ser consultada. | |

### Tipo do retorno

[**\ACBrAPI\Model\ContaCota**](../Model/ContaCota.md)

### Autorização

[oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarCotaPrePago()`

```php
consultarCotaPrePago(): \ACBrAPI\Model\ContaCotaPrePago
```

Consultar o resumo da cota de créditos pré-pagos.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\ContaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->consultarCotaPrePago();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContaApi->consultarCotaPrePago: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

Este endpoint não usa parâmetros.

### Tipo do retorno

[**\ACBrAPI\Model\ContaCotaPrePago**](../Model/ContaCotaPrePago.md)

### Autorização

[oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `listarCotasConta()`

```php
listarCotasConta(): \ACBrAPI\Model\ContaCotaListagem
```

Consultar os limites de uso e consumo das cotas disponíveis, exceto a cota de créditos pré-pagos.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\ContaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listarCotasConta();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContaApi->listarCotasConta: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

Este endpoint não usa parâmetros.

### Tipo do retorno

[**\ACBrAPI\Model\ContaCotaListagem**](../Model/ContaCotaListagem.md)

### Autorização

[oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `listarExtratoCreditosConta()`

```php
listarExtratoCreditosConta($data_inicial, $data_final, $top, $skip, $limit): \ACBrAPI\Model\ContaExtratoCreditoListagem
```

Consultar o extrato de movimentação de créditos do tenant atual.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\ContaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$data_inicial = 'data_inicial_example'; // string
$data_final = 'data_final_example'; // string
$top = 56; // int
$skip = 56; // int
$limit = 56; // int

try {
    $result = $apiInstance->listarExtratoCreditosConta($data_inicial, $data_final, $top, $skip, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContaApi->listarExtratoCreditosConta: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **data_inicial** | **string**|  | [optional] |
| **data_final** | **string**|  | [optional] |
| **top** | **int**|  | [optional] |
| **skip** | **int**|  | [optional] |
| **limit** | **int**|  | [optional] |

### Tipo do retorno

[**\ACBrAPI\Model\ContaExtratoCreditoListagem**](../Model/ContaExtratoCreditoListagem.md)

### Autorização

[oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)
