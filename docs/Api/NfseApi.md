# ACBrAPI\NfseApi

Todas as URIs relativas a https://prod.acbr.api.br, exceto se a operação definir outra URI base.

| Método | Endpoint | Descrição |
| ------------- | ------------- | ------------- |
| [**baixarPdfNfse()**](NfseApi.md#baixarPdfNfse) | **GET** /nfse/{id}/pdf | Baixar PDF do DANFSE |
| [**baixarXmlCancelamentoNfse()**](NfseApi.md#baixarXmlCancelamentoNfse) | **GET** /nfse/{Id}/cancelamento/xml | Baixar XML do evento de cancelamento |
| [**baixarXmlDps()**](NfseApi.md#baixarXmlDps) | **GET** /nfse/{id}/xml/dps | Baixar XML da DPS |
| [**baixarXmlNfse()**](NfseApi.md#baixarXmlNfse) | **GET** /nfse/{id}/xml | Baixar XML da NFS-e processada |
| [**cancelarNfse()**](NfseApi.md#cancelarNfse) | **POST** /nfse/{id}/cancelamento | Cancelar uma NFS-e autorizada |
| [**cidadesAtendidas()**](NfseApi.md#cidadesAtendidas) | **GET** /nfse/cidades | Cidades atendidas |
| [**consultarCancelamentoNfse()**](NfseApi.md#consultarCancelamentoNfse) | **GET** /nfse/{id}/cancelamento | Consultar o cancelamento da NFS-e |
| [**consultarLoteNfse()**](NfseApi.md#consultarLoteNfse) | **GET** /nfse/lotes/{id} | Consultar lote de NFS-e |
| [**consultarMetadados()**](NfseApi.md#consultarMetadados) | **GET** /nfse/cidades/{codigo_ibge} | Consultar metadados |
| [**consultarNfse()**](NfseApi.md#consultarNfse) | **GET** /nfse/{id} | Consultar NFS-e |
| [**emitirLoteNfse()**](NfseApi.md#emitirLoteNfse) | **POST** /nfse/lotes | Emitir lote de NFS-e |
| [**emitirLoteNfseDps()**](NfseApi.md#emitirLoteNfseDps) | **POST** /nfse/dps/lotes | Emitir lote de NFS-e |
| [**emitirNfse()**](NfseApi.md#emitirNfse) | **POST** /nfse | Emitir NFS-e |
| [**emitirNfseDps()**](NfseApi.md#emitirNfseDps) | **POST** /nfse/dps | Emitir NFS-e |
| [**listarLotesNfse()**](NfseApi.md#listarLotesNfse) | **GET** /nfse/lotes | Listar lotes de NFS-e |
| [**listarNfse()**](NfseApi.md#listarNfse) | **GET** /nfse | Listar NFS-e |
| [**sincronizarNfse()**](NfseApi.md#sincronizarNfse) | **POST** /nfse/{id}/sincronizar | Sincroniza dados na NFS-e a partir da Prefeitura |


## `baixarPdfNfse()`

```php
baixarPdfNfse($id, $logotipo, $mensagem_rodape): \SplFileObject
```

Baixar PDF do DANFSE

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID único da NFS-e gerado pela API.
$logotipo = false; // bool | Imprime o documento com logotipo, desde que esteja cadastrado na empresa.
$mensagem_rodape = 'mensagem_rodape_example'; // string | Imprime mensagem no rodapé do documento.    O caractere `|` (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * `\"esquerda\"`  * `\"esquerda|centro\"`  * `\"esquerda|centro|direita\"`  * `\"|centro\"`, `\"|centro|\"`  * `\"|centro|direita\"`  * `\"||direita\"`  * `\"esquerda||direita\"`    Default: `\"\"`

try {
    $result = $apiInstance->baixarPdfNfse($id, $logotipo, $mensagem_rodape);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->baixarPdfNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID único da NFS-e gerado pela API. | |
| **logotipo** | **bool**| Imprime o documento com logotipo, desde que esteja cadastrado na empresa. | [optional] [default to false] |
| **mensagem_rodape** | **string**| Imprime mensagem no rodapé do documento.    O caractere &#x60;|&#x60; (pipe) poderá ser utilizado para definir a quantidade e o alinhamento das mensagens.    **Exemplos de Uso:**  * &#x60;\&quot;esquerda\&quot;&#x60;  * &#x60;\&quot;esquerda|centro\&quot;&#x60;  * &#x60;\&quot;esquerda|centro|direita\&quot;&#x60;  * &#x60;\&quot;|centro\&quot;&#x60;, &#x60;\&quot;|centro|\&quot;&#x60;  * &#x60;\&quot;|centro|direita\&quot;&#x60;  * &#x60;\&quot;||direita\&quot;&#x60;  * &#x60;\&quot;esquerda||direita\&quot;&#x60;    Default: &#x60;\&quot;\&quot;&#x60; | [optional] |

### Tipo do retorno

**\SplFileObject**

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `baixarXmlCancelamentoNfse()`

```php
baixarXmlCancelamentoNfse($id): \SplFileObject
```

Baixar XML do evento de cancelamento

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID único da NFS-e gerado pela API.

try {
    $result = $apiInstance->baixarXmlCancelamentoNfse($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->baixarXmlCancelamentoNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID único da NFS-e gerado pela API. | |

### Tipo do retorno

**\SplFileObject**

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `baixarXmlDps()`

```php
baixarXmlDps($id): \SplFileObject
```

Baixar XML da DPS

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID único da NFS-e gerado pela API.

try {
    $result = $apiInstance->baixarXmlDps($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->baixarXmlDps: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID único da NFS-e gerado pela API. | |

### Tipo do retorno

**\SplFileObject**

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `baixarXmlNfse()`

```php
baixarXmlNfse($id): \SplFileObject
```

Baixar XML da NFS-e processada

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID único da NFS-e gerado pela API.

try {
    $result = $apiInstance->baixarXmlNfse($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->baixarXmlNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID único da NFS-e gerado pela API. | |

### Tipo do retorno

**\SplFileObject**

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `*/*`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `cancelarNfse()`

```php
cancelarNfse($id, $body): \ACBrAPI\Model\NfseCancelamento
```

Cancelar uma NFS-e autorizada

**Informações adicionais**:  - Cota: <a href=\"/docs/limites#dfe-eventos\">dfe-eventos</a>  - Consumo: 1 unidade por requisição.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID único da NFS-e gerado pela API.
$body = new \ACBrAPI\Model\NfsePedidoCancelamento(); // \ACBrAPI\Model\NfsePedidoCancelamento

try {
    $result = $apiInstance->cancelarNfse($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->cancelarNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID único da NFS-e gerado pela API. | |
| **body** | [**\ACBrAPI\Model\NfsePedidoCancelamento**](../Model/NfsePedidoCancelamento.md)|  | [optional] |

### Tipo do retorno

[**\ACBrAPI\Model\NfseCancelamento**](../Model/NfseCancelamento.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `cidadesAtendidas()`

```php
cidadesAtendidas(): \ACBrAPI\Model\NfseCidadesAtendidas
```

Cidades atendidas

Fornece uma relação completa de todos os municípios atendidos pela API.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->cidadesAtendidas();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->cidadesAtendidas: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

Este endpoint não usa parâmetros.

### Tipo do retorno

[**\ACBrAPI\Model\NfseCidadesAtendidas**](../Model/NfseCidadesAtendidas.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarCancelamentoNfse()`

```php
consultarCancelamentoNfse($id): \ACBrAPI\Model\NfseCancelamento
```

Consultar o cancelamento da NFS-e

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID único da NFS-e gerado pela API.

try {
    $result = $apiInstance->consultarCancelamentoNfse($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->consultarCancelamentoNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID único da NFS-e gerado pela API. | |

### Tipo do retorno

[**\ACBrAPI\Model\NfseCancelamento**](../Model/NfseCancelamento.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarLoteNfse()`

```php
consultarLoteNfse($id): \ACBrAPI\Model\RpsLote
```

Consultar lote de NFS-e

Consulta os detalhes de um lote já existente. Forneça o ID único obtido de uma requisição de emissão ou de listagem de lotes e a API irá retornar as informações do lote correspondente.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID único do lote gerado pela API.

try {
    $result = $apiInstance->consultarLoteNfse($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->consultarLoteNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID único do lote gerado pela API. | |

### Tipo do retorno

[**\ACBrAPI\Model\RpsLote**](../Model/RpsLote.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarMetadados()`

```php
consultarMetadados($codigo_ibge): \ACBrAPI\Model\NfseCidadeMetadados
```

Consultar metadados

Consulta a disponibilidade de emissão e alguns metadados de um município.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$codigo_ibge = 'codigo_ibge_example'; // string | Código IBGE do município.

try {
    $result = $apiInstance->consultarMetadados($codigo_ibge);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->consultarMetadados: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **codigo_ibge** | **string**| Código IBGE do município. | |

### Tipo do retorno

[**\ACBrAPI\Model\NfseCidadeMetadados**](../Model/NfseCidadeMetadados.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarNfse()`

```php
consultarNfse($id): \ACBrAPI\Model\Nfse
```

Consultar NFS-e

Consulta os detalhes de uma NFS-e já existente. Forneça o ID único obtido de uma requisição de criação ou de listagem de notas e a API irá retornar as informações da nota correspondente.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID único da NFS-e gerado pela API.

try {
    $result = $apiInstance->consultarNfse($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->consultarNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID único da NFS-e gerado pela API. | |

### Tipo do retorno

[**\ACBrAPI\Model\Nfse**](../Model/Nfse.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `emitirLoteNfse()`

```php
emitirLoteNfse($body): \ACBrAPI\Model\RpsLote
```

Emitir lote de NFS-e

**Informações adicionais**:  - Cota: <a href=\"/docs/limites#dfe-eventos\">dfe-eventos</a>  - Consumo: 1 unidade por NFS-e.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ACBrAPI\Model\RpsPedidoEmissaoLote(); // \ACBrAPI\Model\RpsPedidoEmissaoLote

try {
    $result = $apiInstance->emitirLoteNfse($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->emitirLoteNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **body** | [**\ACBrAPI\Model\RpsPedidoEmissaoLote**](../Model/RpsPedidoEmissaoLote.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\RpsLote**](../Model/RpsLote.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `emitirLoteNfseDps()`

```php
emitirLoteNfseDps($body): \ACBrAPI\Model\RpsLote
```

Emitir lote de NFS-e

**Informações adicionais**:  - Cota: <a href=\"/docs/limites#dfe-eventos\">dfe-eventos</a>  - Consumo: 1 unidade por NFS-e.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ACBrAPI\Model\NfseLoteDpsPedidoEmissao(); // \ACBrAPI\Model\NfseLoteDpsPedidoEmissao

try {
    $result = $apiInstance->emitirLoteNfseDps($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->emitirLoteNfseDps: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **body** | [**\ACBrAPI\Model\NfseLoteDpsPedidoEmissao**](../Model/NfseLoteDpsPedidoEmissao.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\RpsLote**](../Model/RpsLote.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `emitirNfse()`

```php
emitirNfse($body): \ACBrAPI\Model\Nfse
```

Emitir NFS-e

**Informações adicionais**:  - Cota: <a href=\"/docs/limites#dfe-eventos\">dfe-eventos</a>  - Consumo: 1 unidade por requisição.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ACBrAPI\Model\NfsePedidoEmissao(); // \ACBrAPI\Model\NfsePedidoEmissao

try {
    $result = $apiInstance->emitirNfse($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->emitirNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **body** | [**\ACBrAPI\Model\NfsePedidoEmissao**](../Model/NfsePedidoEmissao.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\Nfse**](../Model/Nfse.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `emitirNfseDps()`

```php
emitirNfseDps($body): \ACBrAPI\Model\Nfse
```

Emitir NFS-e

**Informações adicionais**:  - Cota: <a href=\"/docs/limites#dfe-eventos\">dfe-eventos</a>  - Consumo: 1 unidade por requisição.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ACBrAPI\Model\NfseDpsPedidoEmissao(); // \ACBrAPI\Model\NfseDpsPedidoEmissao

try {
    $result = $apiInstance->emitirNfseDps($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->emitirNfseDps: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **body** | [**\ACBrAPI\Model\NfseDpsPedidoEmissao**](../Model/NfseDpsPedidoEmissao.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\Nfse**](../Model/Nfse.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `listarLotesNfse()`

```php
listarLotesNfse($cpf_cnpj, $ambiente, $top, $skip, $inlinecount, $referencia): \ACBrAPI\Model\RpsLoteListagem
```

Listar lotes de NFS-e

Retorna a lista dos lotes de acordo com os critérios de busca utilizados. Os lotes são retornados ordenados pela data da criação, com os mais recentes aparecendo primeiro.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | Filtrar pelo CPF ou CNPJ do emitente.  Utilize o valor sem máscara.
$ambiente = 'ambiente_example'; // string | Identificação do Ambiente.    Valores aceitos: homologacao, producao
$top = 10; // int | Limite no número de objetos a serem retornados pela API, entre 1 e 100.
$skip = 0; // int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada.
$inlinecount = false; // bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação.
$referencia = 'referencia_example'; // string

try {
    $result = $apiInstance->listarLotesNfse($cpf_cnpj, $ambiente, $top, $skip, $inlinecount, $referencia);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->listarLotesNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| Filtrar pelo CPF ou CNPJ do emitente.  Utilize o valor sem máscara. | |
| **ambiente** | **string**| Identificação do Ambiente.    Valores aceitos: homologacao, producao | |
| **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10] |
| **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0] |
| **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to false] |
| **referencia** | **string**|  | [optional] |

### Tipo do retorno

[**\ACBrAPI\Model\RpsLoteListagem**](../Model/RpsLoteListagem.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `listarNfse()`

```php
listarNfse($cpf_cnpj, $ambiente, $top, $skip, $inlinecount, $referencia, $chave, $serie): \ACBrAPI\Model\NfseListagem
```

Listar NFS-e

Retorna a lista de notas de acordo com os critérios de busca utilizados. As notas são retornadas ordenadas pela data da criação, com as mais recentes aparecendo primeiro.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara.
$ambiente = 'ambiente_example'; // string | Identificação do Ambiente.    Valores aceitos: homologacao, producao
$top = 10; // int | Limite no número de objetos a serem retornados pela API, entre 1 e 100.
$skip = 0; // int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada.
$inlinecount = false; // bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação.
$referencia = 'referencia_example'; // string | Seu identificador único para o documento.
$chave = 'chave_example'; // string | Chave de acesso do DF-e.
$serie = 'serie_example'; // string | Série do DF-e.

try {
    $result = $apiInstance->listarNfse($cpf_cnpj, $ambiente, $top, $skip, $inlinecount, $referencia, $chave, $serie);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->listarNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| Filtrar pelo CPF ou CNPJ do emitente.    Utilize o valor sem máscara. | |
| **ambiente** | **string**| Identificação do Ambiente.    Valores aceitos: homologacao, producao | |
| **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10] |
| **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0] |
| **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to false] |
| **referencia** | **string**| Seu identificador único para o documento. | [optional] |
| **chave** | **string**| Chave de acesso do DF-e. | [optional] |
| **serie** | **string**| Série do DF-e. | [optional] |

### Tipo do retorno

[**\ACBrAPI\Model\NfseListagem**](../Model/NfseListagem.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `sincronizarNfse()`

```php
sincronizarNfse($id, $body): \ACBrAPI\Model\NfseSincronizacao
```

Sincroniza dados na NFS-e a partir da Prefeitura

Realiza a sincronização dos dados a partir da consulta da situação atual da NFS-e na prefeitura.    **Cenários de uso**:  * Sincronizar uma nota que se encontra com o status `processando` na API, mas está autorizada na prefeitura;  * Sincronizar uma nota que se encontra com o status `erro` na API, mas está autorizada na prefeitura (útil em casos de erros de transmissão, como instabilidades e timeouts);  * Sincronizar uma nota que se encontra com o status `autorizada`na API, mas está cancelada na prefeitura.    **Informações adicionais**:  - Cota: <a href=\"/docs/limites#dfe-eventos\">dfe-eventos</a>  - Consumo: 1 unidade por evento sincronizado ou requisição.

### Exemplo

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configurar authorização via API key: jwt
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ACBrAPI\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

// Configurar access token OAuth2 para autorização: oauth2
$config = ACBrAPI\Configuration::getDefaultConfiguration()->setAccessToken('SEU_ACCESS_TOKEN');


$apiInstance = new ACBrAPI\Api\NfseApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | ID único da NFS-e gerado pela API.
$body = new \ACBrAPI\Model\NfsePedidoSincronizacao(); // \ACBrAPI\Model\NfsePedidoSincronizacao

try {
    $result = $apiInstance->sincronizarNfse($id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NfseApi->sincronizarNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| ID único da NFS-e gerado pela API. | |
| **body** | [**\ACBrAPI\Model\NfsePedidoSincronizacao**](../Model/NfsePedidoSincronizacao.md)|  | [optional] |

### Tipo do retorno

[**\ACBrAPI\Model\NfseSincronizacao**](../Model/NfseSincronizacao.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)
