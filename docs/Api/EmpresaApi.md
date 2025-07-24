# ACBrAPI\EmpresaApi

Todas as URIs relativas a https://api.nuvemfiscal.com.br, exceto se a operação definir outra URI base.

| Método | Endpoint | Descrição |
| ------------- | ------------- | ------------- |
| [**alterarConfigCte()**](EmpresaApi.md#alterarConfigCte) | **PUT** /empresas/{cpf_cnpj}/cte | Alterar configuração de CT-e |
| [**alterarConfigCteOs()**](EmpresaApi.md#alterarConfigCteOs) | **PUT** /empresas/{cpf_cnpj}/cteos | Alterar configuração de CT-e OS |
| [**alterarConfigDce()**](EmpresaApi.md#alterarConfigDce) | **PUT** /empresas/{cpf_cnpj}/dce | Alterar configuração de DC-e |
| [**alterarConfigDistribuicaoNfe()**](EmpresaApi.md#alterarConfigDistribuicaoNfe) | **PUT** /empresas/{cpf_cnpj}/distnfe | Alterar configuração de Distribuição de NF-e |
| [**alterarConfigMdfe()**](EmpresaApi.md#alterarConfigMdfe) | **PUT** /empresas/{cpf_cnpj}/mdfe | Alterar configuração de MDF-e |
| [**alterarConfigNfce()**](EmpresaApi.md#alterarConfigNfce) | **PUT** /empresas/{cpf_cnpj}/nfce | Alterar configuração de NFC-e |
| [**alterarConfigNfcom()**](EmpresaApi.md#alterarConfigNfcom) | **PUT** /empresas/{cpf_cnpj}/nfcom | Alterar configuração de NFCom |
| [**alterarConfigNfe()**](EmpresaApi.md#alterarConfigNfe) | **PUT** /empresas/{cpf_cnpj}/nfe | Alterar configuração de NF-e |
| [**alterarConfigNfse()**](EmpresaApi.md#alterarConfigNfse) | **PUT** /empresas/{cpf_cnpj}/nfse | Alterar configuração de NFS-e |
| [**atualizarEmpresa()**](EmpresaApi.md#atualizarEmpresa) | **PUT** /empresas/{cpf_cnpj} | Alterar empresa |
| [**baixarLogotipoEmpresa()**](EmpresaApi.md#baixarLogotipoEmpresa) | **GET** /empresas/{cpf_cnpj}/logotipo | Baixar logotipo |
| [**cadastrarCertificadoEmpresa()**](EmpresaApi.md#cadastrarCertificadoEmpresa) | **PUT** /empresas/{cpf_cnpj}/certificado | Cadastrar certificado |
| [**consultarCertificadoEmpresa()**](EmpresaApi.md#consultarCertificadoEmpresa) | **GET** /empresas/{cpf_cnpj}/certificado | Consultar certificado |
| [**consultarConfigCte()**](EmpresaApi.md#consultarConfigCte) | **GET** /empresas/{cpf_cnpj}/cte | Consultar configuração de CT-e |
| [**consultarConfigCteOs()**](EmpresaApi.md#consultarConfigCteOs) | **GET** /empresas/{cpf_cnpj}/cteos | Consultar configuração de CT-e OS |
| [**consultarConfigDce()**](EmpresaApi.md#consultarConfigDce) | **GET** /empresas/{cpf_cnpj}/dce | Consultar configuração de DC-e |
| [**consultarConfigDistribuicaoNfe()**](EmpresaApi.md#consultarConfigDistribuicaoNfe) | **GET** /empresas/{cpf_cnpj}/distnfe | Consultar configuração de Distribuição de NF-e |
| [**consultarConfigMdfe()**](EmpresaApi.md#consultarConfigMdfe) | **GET** /empresas/{cpf_cnpj}/mdfe | Consultar configuração de MDF-e |
| [**consultarConfigNfce()**](EmpresaApi.md#consultarConfigNfce) | **GET** /empresas/{cpf_cnpj}/nfce | Consultar configuração de NFC-e |
| [**consultarConfigNfcom()**](EmpresaApi.md#consultarConfigNfcom) | **GET** /empresas/{cpf_cnpj}/nfcom | Consultar configuração de NFCom |
| [**consultarConfigNfe()**](EmpresaApi.md#consultarConfigNfe) | **GET** /empresas/{cpf_cnpj}/nfe | Consultar configuração de NF-e |
| [**consultarConfigNfse()**](EmpresaApi.md#consultarConfigNfse) | **GET** /empresas/{cpf_cnpj}/nfse | Consultar configuração de NFS-e |
| [**consultarEmpresa()**](EmpresaApi.md#consultarEmpresa) | **GET** /empresas/{cpf_cnpj} | Consultar empresa |
| [**criarEmpresa()**](EmpresaApi.md#criarEmpresa) | **POST** /empresas | Cadastrar empresa |
| [**enviarCertificadoEmpresa()**](EmpresaApi.md#enviarCertificadoEmpresa) | **PUT** /empresas/{cpf_cnpj}/certificado/upload | Upload de certificado |
| [**enviarLogotipoEmpresa()**](EmpresaApi.md#enviarLogotipoEmpresa) | **PUT** /empresas/{cpf_cnpj}/logotipo | Enviar logotipo |
| [**excluirCertificadoEmpresa()**](EmpresaApi.md#excluirCertificadoEmpresa) | **DELETE** /empresas/{cpf_cnpj}/certificado | Deletar certificado |
| [**excluirEmpresa()**](EmpresaApi.md#excluirEmpresa) | **DELETE** /empresas/{cpf_cnpj} | Deletar empresa |
| [**excluirLogotipoEmpresa()**](EmpresaApi.md#excluirLogotipoEmpresa) | **DELETE** /empresas/{cpf_cnpj}/logotipo | Deletar logotipo |
| [**listarEmpresas()**](EmpresaApi.md#listarEmpresas) | **GET** /empresas | Listar empresas |


## `alterarConfigCte()`

```php
alterarConfigCte($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaConfigCte
```

Alterar configuração de CT-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaConfigCte(); // \ACBrAPI\Model\EmpresaConfigCte

try {
    $result = $apiInstance->alterarConfigCte($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->alterarConfigCte: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaConfigCte**](../Model/EmpresaConfigCte.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigCte**](../Model/EmpresaConfigCte.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `alterarConfigCteOs()`

```php
alterarConfigCteOs($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaConfigCteOs
```

Alterar configuração de CT-e OS

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaConfigCteOs(); // \ACBrAPI\Model\EmpresaConfigCteOs

try {
    $result = $apiInstance->alterarConfigCteOs($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->alterarConfigCteOs: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaConfigCteOs**](../Model/EmpresaConfigCteOs.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigCteOs**](../Model/EmpresaConfigCteOs.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `alterarConfigDce()`

```php
alterarConfigDce($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaConfigDce
```

Alterar configuração de DC-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaConfigDce(); // \ACBrAPI\Model\EmpresaConfigDce

try {
    $result = $apiInstance->alterarConfigDce($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->alterarConfigDce: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaConfigDce**](../Model/EmpresaConfigDce.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigDce**](../Model/EmpresaConfigDce.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `alterarConfigDistribuicaoNfe()`

```php
alterarConfigDistribuicaoNfe($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaConfigDistribuicaoNfe
```

Alterar configuração de Distribuição de NF-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaConfigDistribuicaoNfe(); // \ACBrAPI\Model\EmpresaConfigDistribuicaoNfe

try {
    $result = $apiInstance->alterarConfigDistribuicaoNfe($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->alterarConfigDistribuicaoNfe: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaConfigDistribuicaoNfe**](../Model/EmpresaConfigDistribuicaoNfe.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigDistribuicaoNfe**](../Model/EmpresaConfigDistribuicaoNfe.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `alterarConfigMdfe()`

```php
alterarConfigMdfe($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaConfigMdfe
```

Alterar configuração de MDF-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaConfigMdfe(); // \ACBrAPI\Model\EmpresaConfigMdfe

try {
    $result = $apiInstance->alterarConfigMdfe($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->alterarConfigMdfe: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaConfigMdfe**](../Model/EmpresaConfigMdfe.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigMdfe**](../Model/EmpresaConfigMdfe.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `alterarConfigNfce()`

```php
alterarConfigNfce($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaConfigNfce
```

Alterar configuração de NFC-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaConfigNfce(); // \ACBrAPI\Model\EmpresaConfigNfce

try {
    $result = $apiInstance->alterarConfigNfce($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->alterarConfigNfce: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaConfigNfce**](../Model/EmpresaConfigNfce.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigNfce**](../Model/EmpresaConfigNfce.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `alterarConfigNfcom()`

```php
alterarConfigNfcom($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaConfigNfcom
```

Alterar configuração de NFCom

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaConfigNfcom(); // \ACBrAPI\Model\EmpresaConfigNfcom

try {
    $result = $apiInstance->alterarConfigNfcom($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->alterarConfigNfcom: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaConfigNfcom**](../Model/EmpresaConfigNfcom.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigNfcom**](../Model/EmpresaConfigNfcom.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `alterarConfigNfe()`

```php
alterarConfigNfe($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaConfigNfe
```

Alterar configuração de NF-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaConfigNfe(); // \ACBrAPI\Model\EmpresaConfigNfe

try {
    $result = $apiInstance->alterarConfigNfe($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->alterarConfigNfe: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaConfigNfe**](../Model/EmpresaConfigNfe.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigNfe**](../Model/EmpresaConfigNfe.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `alterarConfigNfse()`

```php
alterarConfigNfse($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaConfigNfse
```

Alterar configuração de NFS-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaConfigNfse(); // \ACBrAPI\Model\EmpresaConfigNfse

try {
    $result = $apiInstance->alterarConfigNfse($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->alterarConfigNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaConfigNfse**](../Model/EmpresaConfigNfse.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigNfse**](../Model/EmpresaConfigNfse.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `atualizarEmpresa()`

```php
atualizarEmpresa($cpf_cnpj, $body): \ACBrAPI\Model\Empresa
```

Alterar empresa

Altera o cadastro de uma empresa (emitente/prestador) que esteja associada a sua conta.  Nesse método, por tratar-se de um PUT, caso algum campo não seja informado, o valor dele será apagado.

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\Empresa(); // \ACBrAPI\Model\Empresa

try {
    $result = $apiInstance->atualizarEmpresa($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->atualizarEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\Empresa**](../Model/Empresa.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\Empresa**](../Model/Empresa.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `baixarLogotipoEmpresa()`

```php
baixarLogotipoEmpresa($cpf_cnpj): \SplFileObject
```

Baixar logotipo

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->baixarLogotipoEmpresa($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->baixarLogotipoEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

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

## `cadastrarCertificadoEmpresa()`

```php
cadastrarCertificadoEmpresa($cpf_cnpj, $body): \ACBrAPI\Model\EmpresaCertificado
```

Cadastrar certificado

Cadastre ou atualize um certificado digital e vincule a sua empresa, para que possa iniciar a emissão de notas.  * No parâmetro `certificado`, envie o binário do certificado digital (.pfx ou .p12) codificado em **base64**.

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$body = new \ACBrAPI\Model\EmpresaPedidoCadastroCertificado(); // \ACBrAPI\Model\EmpresaPedidoCadastroCertificado

try {
    $result = $apiInstance->cadastrarCertificadoEmpresa($cpf_cnpj, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->cadastrarCertificadoEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **body** | [**\ACBrAPI\Model\EmpresaPedidoCadastroCertificado**](../Model/EmpresaPedidoCadastroCertificado.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaCertificado**](../Model/EmpresaCertificado.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarCertificadoEmpresa()`

```php
consultarCertificadoEmpresa($cpf_cnpj): \ACBrAPI\Model\EmpresaCertificado
```

Consultar certificado

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarCertificadoEmpresa($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarCertificadoEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaCertificado**](../Model/EmpresaCertificado.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarConfigCte()`

```php
consultarConfigCte($cpf_cnpj): \ACBrAPI\Model\EmpresaConfigCte
```

Consultar configuração de CT-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarConfigCte($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarConfigCte: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigCte**](../Model/EmpresaConfigCte.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarConfigCteOs()`

```php
consultarConfigCteOs($cpf_cnpj): \ACBrAPI\Model\EmpresaConfigCteOs
```

Consultar configuração de CT-e OS

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarConfigCteOs($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarConfigCteOs: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigCteOs**](../Model/EmpresaConfigCteOs.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarConfigDce()`

```php
consultarConfigDce($cpf_cnpj): \ACBrAPI\Model\EmpresaConfigDce
```

Consultar configuração de DC-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarConfigDce($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarConfigDce: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigDce**](../Model/EmpresaConfigDce.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarConfigDistribuicaoNfe()`

```php
consultarConfigDistribuicaoNfe($cpf_cnpj): \ACBrAPI\Model\EmpresaConfigDistribuicaoNfe
```

Consultar configuração de Distribuição de NF-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarConfigDistribuicaoNfe($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarConfigDistribuicaoNfe: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigDistribuicaoNfe**](../Model/EmpresaConfigDistribuicaoNfe.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarConfigMdfe()`

```php
consultarConfigMdfe($cpf_cnpj): \ACBrAPI\Model\EmpresaConfigMdfe
```

Consultar configuração de MDF-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarConfigMdfe($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarConfigMdfe: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigMdfe**](../Model/EmpresaConfigMdfe.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarConfigNfce()`

```php
consultarConfigNfce($cpf_cnpj): \ACBrAPI\Model\EmpresaConfigNfce
```

Consultar configuração de NFC-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarConfigNfce($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarConfigNfce: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigNfce**](../Model/EmpresaConfigNfce.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarConfigNfcom()`

```php
consultarConfigNfcom($cpf_cnpj): \ACBrAPI\Model\EmpresaConfigNfcom
```

Consultar configuração de NFCom

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarConfigNfcom($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarConfigNfcom: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigNfcom**](../Model/EmpresaConfigNfcom.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarConfigNfe()`

```php
consultarConfigNfe($cpf_cnpj): \ACBrAPI\Model\EmpresaConfigNfe
```

Consultar configuração de NF-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarConfigNfe($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarConfigNfe: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigNfe**](../Model/EmpresaConfigNfe.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarConfigNfse()`

```php
consultarConfigNfse($cpf_cnpj): \ACBrAPI\Model\EmpresaConfigNfse
```

Consultar configuração de NFS-e

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarConfigNfse($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarConfigNfse: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaConfigNfse**](../Model/EmpresaConfigNfse.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `consultarEmpresa()`

```php
consultarEmpresa($cpf_cnpj): \ACBrAPI\Model\Empresa
```

Consultar empresa

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $result = $apiInstance->consultarEmpresa($cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->consultarEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

[**\ACBrAPI\Model\Empresa**](../Model/Empresa.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `criarEmpresa()`

```php
criarEmpresa($body): \ACBrAPI\Model\Empresa
```

Cadastrar empresa

Cadastre uma nova empresa (emitente ou prestador) à sua conta.

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ACBrAPI\Model\Empresa(); // \ACBrAPI\Model\Empresa

try {
    $result = $apiInstance->criarEmpresa($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->criarEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **body** | [**\ACBrAPI\Model\Empresa**](../Model/Empresa.md)|  | |

### Tipo do retorno

[**\ACBrAPI\Model\Empresa**](../Model/Empresa.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `enviarCertificadoEmpresa()`

```php
enviarCertificadoEmpresa($cpf_cnpj, $input): \ACBrAPI\Model\EmpresaCertificado
```

Upload de certificado

Cadastre ou atualize um certificado digital e vincule a sua empresa, para que possa iniciar a emissão de notas.  * Utilize o `content-type` igual a `multipart/form-data`.  * No parâmetro `file`, envie o binário do arquivo (.pfx ou .p12) do certificado digital.  * No parâmetro `password`, envie a senha do certificado.

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$input = "/path/to/file.txt"; // \SplFileObject

try {
    $result = $apiInstance->enviarCertificadoEmpresa($cpf_cnpj, $input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->enviarCertificadoEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **input** | **\SplFileObject****\SplFileObject**|  | [optional] |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaCertificado**](../Model/EmpresaCertificado.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `enviarLogotipoEmpresa()`

```php
enviarLogotipoEmpresa($cpf_cnpj, $input)
```

Enviar logotipo

Cadastre ou atualize um logotipo e vincule a sua empresa.    **Restrições:**  * Tipos de mídia (MIME) suportados: `image/png` e `image/jpeg`  * Tamanho máximo do arquivo: 200 KB    **Cenários de uso:**  * Quero que minhas notas sejam impressas com esse logotipo.  * Quero trocar o logotipo utilizado em minhas impressões.

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.
$input = "/path/to/file.txt"; // \SplFileObject

try {
    $apiInstance->enviarLogotipoEmpresa($cpf_cnpj, $input);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->enviarLogotipoEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |
| **input** | **\SplFileObject****\SplFileObject**|  | [optional] |

### Tipo do retorno

void (empty response body)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: `multipart/form-data`
- **Accept**: Not defined

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `excluirCertificadoEmpresa()`

```php
excluirCertificadoEmpresa($cpf_cnpj)
```

Deletar certificado

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $apiInstance->excluirCertificadoEmpresa($cpf_cnpj);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->excluirCertificadoEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

void (empty response body)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `excluirEmpresa()`

```php
excluirEmpresa($cpf_cnpj)
```

Deletar empresa

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $apiInstance->excluirEmpresa($cpf_cnpj);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->excluirEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

void (empty response body)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `excluirLogotipoEmpresa()`

```php
excluirLogotipoEmpresa($cpf_cnpj)
```

Deletar logotipo

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$cpf_cnpj = 'cpf_cnpj_example'; // string | CPF ou CNPJ da empresa.  Utilize o valor sem máscara.

try {
    $apiInstance->excluirLogotipoEmpresa($cpf_cnpj);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->excluirLogotipoEmpresa: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **cpf_cnpj** | **string**| CPF ou CNPJ da empresa.  Utilize o valor sem máscara. | |

### Tipo do retorno

void (empty response body)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)

## `listarEmpresas()`

```php
listarEmpresas($top, $skip, $inlinecount, $cpf_cnpj): \ACBrAPI\Model\EmpresaListagem
```

Listar empresas

Retorna a lista das empresas associadas à sua conta. As empresas são retornadas ordenadas pela data da criação, com as mais recentes aparecendo primeiro.

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


$apiInstance = new ACBrAPI\Api\EmpresaApi(
    // Se quiser usar um client http customizado, passe um client que implemente `GuzzleHttp\ClientInterface`.
    // Isso é opcional, `GuzzleHttp\Client` será usado por padrão.
    new GuzzleHttp\Client(),
    $config
);
$top = 10; // int | Limite no número de objetos a serem retornados pela API, entre 1 e 100.
$skip = 0; // int | Quantidade de objetos que serão ignorados antes da lista começar a ser retornada.
$inlinecount = false; // bool | Inclui no JSON de resposta, na propriedade `@count`, o número total de registros que o filtro retornaria, independente dos filtros de paginação.
$cpf_cnpj = 'cpf_cnpj_example'; // string | Filtrar pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*.

try {
    $result = $apiInstance->listarEmpresas($top, $skip, $inlinecount, $cpf_cnpj);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmpresaApi->listarEmpresas: ', $e->getMessage(), PHP_EOL;
}
```

### Parâmetros

| Nome | Tipo | Descrição  | Notas |
| ------------- | ------------- | ------------- | ------------- |
| **top** | **int**| Limite no número de objetos a serem retornados pela API, entre 1 e 100. | [optional] [default to 10] |
| **skip** | **int**| Quantidade de objetos que serão ignorados antes da lista começar a ser retornada. | [optional] [default to 0] |
| **inlinecount** | **bool**| Inclui no JSON de resposta, na propriedade &#x60;@count&#x60;, o número total de registros que o filtro retornaria, independente dos filtros de paginação. | [optional] [default to false] |
| **cpf_cnpj** | **string**| Filtrar pelo CPF ou CNPJ da empresa.    *Utilize o valor sem máscara*. | [optional] |

### Tipo do retorno

[**\ACBrAPI\Model\EmpresaListagem**](../Model/EmpresaListagem.md)

### Autorização

[jwt](../../README.md#jwt), [oauth2](../../README.md#oauth2)

### Headers HTTP da requisição

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Voltar ao topo]](#) [[Back to API list]](../../README.md#endpoints)
[[Voltar à lista de DTOs]](../../README.md#models)
[[Voltar ao README]](../../README.md)
