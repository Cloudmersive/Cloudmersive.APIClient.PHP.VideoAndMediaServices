# Swagger\Client\VideoApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**videoConvertToGif**](VideoApi.md#videoConvertToGif) | **POST** /video/convert/to/gif | Convert Video to Animated GIF format.
[**videoConvertToMov**](VideoApi.md#videoConvertToMov) | **POST** /video/convert/to/mov | Convert Video to MOV format.
[**videoConvertToMp4**](VideoApi.md#videoConvertToMp4) | **POST** /video/convert/to/mp4 | Convert Video to MP4 format.
[**videoConvertToWebm**](VideoApi.md#videoConvertToWebm) | **POST** /video/convert/to/webm | Convert Video to WEBM format.
[**videoGetInfo**](VideoApi.md#videoGetInfo) | **POST** /video/convert/get-info | Get detailed information about a video or audio file


# **videoConvertToGif**
> string videoConvertToGif($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $extend_processing_time, $start_time, $time_span)

Convert Video to Animated GIF format.

Automatically detect video file format and convert it to animated GIF format. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Maximum output file size is 50GB. Default height is 250 pixels, while preserving the video's aspect ratio.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\VideoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB.
$max_width = 56; // int | Optional; Maximum width of the output video, up to the original video width. Defaults to 250 pixels.
$max_height = 56; // int | Optional; Maximum height of the output video, up to the original video width. Defaults to 250 pixels.
$preserve_aspect_ratio = true; // bool | Optional; If false, the original video's aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true.
$frame_rate = 56; // int | Optional; Specify the frame rate of the output video. Defaults to 24 frames per second.
$extend_processing_time = true; // bool | Optional; If true, will allow additional processing time for the video file conversion, using one API call per additional minute over the 5 minute default processing time, up to a maximum of 25 total minutes. This is generally necessary for files larger than 500 MB or longer than 30 minutes.
$start_time = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional; Specify the desired starting time of the GIF video in TimeSpan format.
$time_span = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional; Specify the desired length of the GIF video in TimeSpan format. Limit is 30 minutes.

try {
    $result = $apiInstance->videoConvertToGif($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $extend_processing_time, $start_time, $time_span);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoConvertToGif: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. |
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to 250 pixels. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to 250 pixels. | [optional]
 **preserve_aspect_ratio** | **bool**| Optional; If false, the original video&#39;s aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to 24 frames per second. | [optional]
 **extend_processing_time** | **bool**| Optional; If true, will allow additional processing time for the video file conversion, using one API call per additional minute over the 5 minute default processing time, up to a maximum of 25 total minutes. This is generally necessary for files larger than 500 MB or longer than 30 minutes. | [optional]
 **start_time** | **\DateTime**| Optional; Specify the desired starting time of the GIF video in TimeSpan format. | [optional]
 **time_span** | **\DateTime**| Optional; Specify the desired length of the GIF video in TimeSpan format. Limit is 30 minutes. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoConvertToMov**
> string videoConvertToMov($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality, $extend_processing_time)

Convert Video to MOV format.

Automatically detect video file format and convert it to MOV format. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Maximum output file size is 50GB.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\VideoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB.
$max_width = 56; // int | Optional; Maximum width of the output video, up to the original video width. Defaults to original video width.
$max_height = 56; // int | Optional; Maximum height of the output video, up to the original video width. Defaults to original video height.
$preserve_aspect_ratio = true; // bool | Optional; If false, the original video's aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true.
$frame_rate = 56; // int | Optional; Specify the frame rate of the output video. Defaults to original video frame rate.
$quality = 56; // int | Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50.
$extend_processing_time = true; // bool | Optional; If true, will allow additional processing time for the video file conversion, using one API call per additional minute over the 5 minute default processing time, up to a maximum of 25 total minutes. This is generally necessary for files larger than 500 MB or longer than 30 minutes.

try {
    $result = $apiInstance->videoConvertToMov($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality, $extend_processing_time);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoConvertToMov: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. |
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to original video width. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to original video height. | [optional]
 **preserve_aspect_ratio** | **bool**| Optional; If false, the original video&#39;s aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to original video frame rate. | [optional]
 **quality** | **int**| Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50. | [optional]
 **extend_processing_time** | **bool**| Optional; If true, will allow additional processing time for the video file conversion, using one API call per additional minute over the 5 minute default processing time, up to a maximum of 25 total minutes. This is generally necessary for files larger than 500 MB or longer than 30 minutes. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoConvertToMp4**
> string videoConvertToMp4($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality, $extend_processing_time)

Convert Video to MP4 format.

Automatically detect video file format and convert it to MP4 format. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Maximum output file size is 50GB.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\VideoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB.
$max_width = 56; // int | Optional; Maximum width of the output video, up to the original video width. Defaults to original video width.
$max_height = 56; // int | Optional; Maximum height of the output video, up to the original video width. Defaults to original video height.
$preserve_aspect_ratio = true; // bool | Optional; If false, the original video's aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true.
$frame_rate = 56; // int | Optional; Specify the frame rate of the output video. Defaults to original video frame rate.
$quality = 56; // int | Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50.
$extend_processing_time = true; // bool | Optional; If true, will allow additional processing time for the video file conversion, using one API call per additional minute over the 5 minute default processing time, up to a maximum of 25 total minutes. This is generally necessary for files larger than 500 MB or longer than 30 minutes.

try {
    $result = $apiInstance->videoConvertToMp4($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality, $extend_processing_time);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoConvertToMp4: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. |
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to original video width. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to original video height. | [optional]
 **preserve_aspect_ratio** | **bool**| Optional; If false, the original video&#39;s aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to original video frame rate. | [optional]
 **quality** | **int**| Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50. | [optional]
 **extend_processing_time** | **bool**| Optional; If true, will allow additional processing time for the video file conversion, using one API call per additional minute over the 5 minute default processing time, up to a maximum of 25 total minutes. This is generally necessary for files larger than 500 MB or longer than 30 minutes. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoConvertToWebm**
> string videoConvertToWebm($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality, $extend_processing_time)

Convert Video to WEBM format.

Automatically detect video file format and convert it to WEBM format. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Maximum output file size is 50GB.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\VideoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB.
$max_width = 56; // int | Optional; Maximum width of the output video, up to the original video width. Defaults to original video width.
$max_height = 56; // int | Optional; Maximum height of the output video, up to the original video width. Defaults to original video height.
$preserve_aspect_ratio = true; // bool | Optional; If false, the original video's aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true.
$frame_rate = 56; // int | Optional; Specify the frame rate of the output video. Defaults to original video frame rate.
$quality = 56; // int | Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50.
$extend_processing_time = true; // bool | Optional; If true, will allow additional processing time for the video file conversion, using one API call per additional minute over the 5 minute default processing time, up to a maximum of 25 total minutes. This is generally necessary for files larger than 500 MB or longer than 30 minutes.

try {
    $result = $apiInstance->videoConvertToWebm($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality, $extend_processing_time);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoConvertToWebm: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. |
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to original video width. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to original video height. | [optional]
 **preserve_aspect_ratio** | **bool**| Optional; If false, the original video&#39;s aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to original video frame rate. | [optional]
 **quality** | **int**| Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50. | [optional]
 **extend_processing_time** | **bool**| Optional; If true, will allow additional processing time for the video file conversion, using one API call per additional minute over the 5 minute default processing time, up to a maximum of 25 total minutes. This is generally necessary for files larger than 500 MB or longer than 30 minutes. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoGetInfo**
> string videoGetInfo($input_file, $file_url)

Get detailed information about a video or audio file

Retrieve detailed information about a video or audio file, including format, dimensions, file size, bit rate, duration and start time. Compatible with many formats, including: AVI, ASF, FLV, GIF, MP4, MPEG/MPG, Matroska/WEBM, MOV, AIFF, ASF, CAF, MP3, MP2, MP1, Ogg, OMG/OMA, and WAV. Uses 1 API call per 10 MB of file size.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\VideoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB.

try {
    $result = $apiInstance->videoGetInfo($input_file, $file_url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoGetInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. |
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

