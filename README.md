
# Getting Started with APIMATIC Calculator

## Introduction

Simple calculator API hosted on APIMATIC

## Install the Package

Run the following command to install the package and automatically add the dependency to your composer.json file:

```bash
composer require "muhamza/calculator-package-v-1-php-sdk:1.0.5"
```

Or add it to the composer.json file manually as given below:

```json
"require": {
    "muhamza/calculator-package-v-1-php-sdk": "1.0.5"
}
```

You can also view the package at:
https://packagist.org/packages/muhamza/calculator-package-v-1-php-sdk#1.0.5

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/MuHamza30/calculator-package-v-1-php-php-sdk/tree/1.0.5/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | `Environment` | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| timeout | `int` | Timeout for API calls in seconds.<br>*Default*: `0` |
| enableRetries | `bool` | Whether to enable retries and backoff feature.<br>*Default*: `false` |
| numberOfRetries | `int` | The number of retries to make.<br>*Default*: `0` |
| retryInterval | `float` | The retry time interval between the endpoint calls.<br>*Default*: `1` |
| backOffFactor | `float` | Exponential backoff factor to increase interval between retries.<br>*Default*: `2` |
| maximumRetryWaitTime | `int` | The maximum wait time in seconds for overall retrying requests.<br>*Default*: `0` |
| retryOnTimeout | `bool` | Whether to retry on request timeout.<br>*Default*: `true` |
| httpStatusCodesToRetry | `array` | Http status codes to retry against.<br>*Default*: `408, 413, 429, 500, 502, 503, 504, 521, 522, 524` |
| httpMethodsToRetry | `array` | Http methods to retry against.<br>*Default*: `'GET', 'PUT'` |
| proxyConfiguration | [`ProxyConfigurationBuilder`](https://www.github.com/MuHamza30/calculator-package-v-1-php-php-sdk/tree/1.0.5/doc/proxy-configuration-builder.md) | Represents the proxy configurations for API calls |

The API client can be initialized as follows:

```php
$client = APIMATICCalculatorClientBuilder::init()
    ->environment(Environment::PRODUCTION)
    ->build();
```

## List of APIs

* [Simple Calculator](https://www.github.com/MuHamza30/calculator-package-v-1-php-php-sdk/tree/1.0.5/doc/controllers/simple-calculator.md)

## SDK Infrastructure

### Configuration

* [ProxyConfigurationBuilder](https://www.github.com/MuHamza30/calculator-package-v-1-php-php-sdk/tree/1.0.5/doc/proxy-configuration-builder.md)

### HTTP

* [HttpRequest](https://www.github.com/MuHamza30/calculator-package-v-1-php-php-sdk/tree/1.0.5/doc/http-request.md)
* [HttpResponse](https://www.github.com/MuHamza30/calculator-package-v-1-php-php-sdk/tree/1.0.5/doc/http-response.md)

### Utilities

* [ApiException](https://www.github.com/MuHamza30/calculator-package-v-1-php-php-sdk/tree/1.0.5/doc/api-exception.md)

