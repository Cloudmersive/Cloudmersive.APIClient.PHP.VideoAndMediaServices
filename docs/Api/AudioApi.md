# Swagger\Client\AudioApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**audioConvertToAac**](AudioApi.md#audioConvertToAac) | **POST** /video/convert/to/aac | Convert Audio File to AAC format.
[**audioConvertToM4a**](AudioApi.md#audioConvertToM4a) | **POST** /video/convert/to/m4a | Convert Audio File to M4A format.
[**audioConvertToMp3**](AudioApi.md#audioConvertToMp3) | **POST** /video/convert/to/mp3 | Convert Audio File to MP3 format.
[**audioConvertToWav**](AudioApi.md#audioConvertToWav) | **POST** /video/convert/to/wav | Convert Audio File to WAV format.


# **audioConvertToAac**
> string audioConvertToAac($input_file, $file_url, $bit_rate)

Convert Audio File to AAC format.

Automatically detect audio file format and convert it to AAC format. Supports many input audio formats, including AAC, FLAC, M4A, MP2, MP3, OGG, WMA, and WAV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\AudioApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of an audio file being used for conversion. Use this option for files larger than 2GB.
$bit_rate = 56; // int | Optional; Specify the desired bitrate of the converted audio file in kilobytes per second (kB/s). Value may be between 48 and 1,411. By default, the optimal bitrate will be chosen automatically.

try {
    $result = $apiInstance->audioConvertToAac($input_file, $file_url, $bit_rate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AudioApi->audioConvertToAac: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of an audio file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **bit_rate** | **int**| Optional; Specify the desired bitrate of the converted audio file in kilobytes per second (kB/s). Value may be between 48 and 1,411. By default, the optimal bitrate will be chosen automatically. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **audioConvertToM4a**
> string audioConvertToM4a($input_file, $file_url, $bit_rate)

Convert Audio File to M4A format.

Automatically detect audio file format and convert it to M4A format. Supports many input audio formats, including AAC, FLAC, M4A, MP2, MP3, OGG, WMA, and WAV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\AudioApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of an audio file being used for conversion. Use this option for files larger than 2GB.
$bit_rate = 56; // int | Optional; Specify the desired bitrate of the converted audio file in kilobytes per second (kB/s). Value may be between 48 and 1,411. By default, the optimal bitrate will be chosen automatically.

try {
    $result = $apiInstance->audioConvertToM4a($input_file, $file_url, $bit_rate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AudioApi->audioConvertToM4a: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of an audio file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **bit_rate** | **int**| Optional; Specify the desired bitrate of the converted audio file in kilobytes per second (kB/s). Value may be between 48 and 1,411. By default, the optimal bitrate will be chosen automatically. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **audioConvertToMp3**
> string audioConvertToMp3($input_file, $file_url, $bit_rate)

Convert Audio File to MP3 format.

Automatically detect audio file format and convert it to MP3 format. Supports many input audio formats, including AAC, FLAC, M4A, MP2, MP3, OGG, WMA, and WAV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\AudioApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of an audio file being used for conversion. Use this option for files larger than 2GB.
$bit_rate = 56; // int | Optional; Specify the desired bitrate of the converted audio file in kilobytes per second (kB/s). Value may be between 48 and 1,411. By default, the optimal bitrate will be chosen automatically.

try {
    $result = $apiInstance->audioConvertToMp3($input_file, $file_url, $bit_rate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AudioApi->audioConvertToMp3: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of an audio file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **bit_rate** | **int**| Optional; Specify the desired bitrate of the converted audio file in kilobytes per second (kB/s). Value may be between 48 and 1,411. By default, the optimal bitrate will be chosen automatically. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **audioConvertToWav**
> string audioConvertToWav($input_file, $file_url, $sample_rate)

Convert Audio File to WAV format.

Automatically detect audio file format and convert it to WAV format. Supports many input audio formats, including AAC, FLAC, M4A, MP2, MP3, OGG, WMA, and WAV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\AudioApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of an audio file being used for conversion. Use this option for files larger than 2GB.
$sample_rate = 8.14; // float | Optional; Specify the desired sample rate of the converted audio file in kHz. Value may be between 8 and 96. Standard for audio CDs is 44.1, while DVD audio standard is 48. By default, the optimal sample rate will be chosen automatically.

try {
    $result = $apiInstance->audioConvertToWav($input_file, $file_url, $sample_rate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AudioApi->audioConvertToWav: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of an audio file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **sample_rate** | **float**| Optional; Specify the desired sample rate of the converted audio file in kHz. Value may be between 8 and 96. Standard for audio CDs is 44.1, while DVD audio standard is 48. By default, the optimal sample rate will be chosen automatically. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

