# Swagger\Client\VideoApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**videoConvertToGif**](VideoApi.md#videoConvertToGif) | **POST** /video/convert/to/gif | Convert Video to Animated GIF format.
[**videoConvertToMov**](VideoApi.md#videoConvertToMov) | **POST** /video/convert/to/mov | Convert Video to MOV format.
[**videoConvertToMp4**](VideoApi.md#videoConvertToMp4) | **POST** /video/convert/to/mp4 | Convert Video to MP4 format.
[**videoConvertToStillFrames**](VideoApi.md#videoConvertToStillFrames) | **POST** /video/convert/to/still-frames | Convert Video to PNG Still Frames.
[**videoConvertToWebm**](VideoApi.md#videoConvertToWebm) | **POST** /video/convert/to/webm | Convert Video to WEBM format.
[**videoCutVideo**](VideoApi.md#videoCutVideo) | **POST** /video/cut | Cut a Video to a Shorter Length
[**videoGetInfo**](VideoApi.md#videoGetInfo) | **POST** /video/convert/get-info | Get detailed information about a video or audio file
[**videoResizeVideo**](VideoApi.md#videoResizeVideo) | **POST** /video/resize/preserveAspectRatio | Resizes a Video Preserving the Original Aspect Ratio.
[**videoResizeVideoSimple**](VideoApi.md#videoResizeVideoSimple) | **POST** /video/resize/target | Resizes a Video without Preserving Aspect Ratio.
[**videoScanForNsfw**](VideoApi.md#videoScanForNsfw) | **POST** /video/scan/nsfw | Scan a Video for NSFW content.
[**videoSplitVideo**](VideoApi.md#videoSplitVideo) | **POST** /video/split | Split a Video into Two Shorter Videos


# **videoConvertToGif**
> string videoConvertToGif($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $start_time, $time_span)

Convert Video to Animated GIF format.

Automatically detect video file format and convert it to animated GIF format. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB. Default height is 250 pixels, while preserving the video's aspect ratio.

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
$max_width = 56; // int | Optional; Maximum width of the output video, up to the original video width. Defaults to 250 pixels, maximum is 500 pixels.
$max_height = 56; // int | Optional; Maximum height of the output video, up to the original video width. Defaults to 250 pixels, maximum is 500 pixels.
$preserve_aspect_ratio = true; // bool | Optional; If false, the original video's aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true.
$frame_rate = 56; // int | Optional; Specify the frame rate of the output video. Defaults to 24 frames per second.
$start_time = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional; Specify the desired starting time of the GIF video in TimeSpan format.
$time_span = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional; Specify the desired length of the GIF video in TimeSpan format. Limit is 30 seconds. Default is 10 seconds.

try {
    $result = $apiInstance->videoConvertToGif($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $start_time, $time_span);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoConvertToGif: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to 250 pixels, maximum is 500 pixels. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to 250 pixels, maximum is 500 pixels. | [optional]
 **preserve_aspect_ratio** | **bool**| Optional; If false, the original video&#39;s aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to 24 frames per second. | [optional]
 **start_time** | **\DateTime**| Optional; Specify the desired starting time of the GIF video in TimeSpan format. | [optional]
 **time_span** | **\DateTime**| Optional; Specify the desired length of the GIF video in TimeSpan format. Limit is 30 seconds. Default is 10 seconds. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoConvertToMov**
> string videoConvertToMov($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality)

Convert Video to MOV format.

Automatically detect video file format and convert it to MOV format. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

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

try {
    $result = $apiInstance->videoConvertToMov($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoConvertToMov: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to original video width. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to original video height. | [optional]
 **preserve_aspect_ratio** | **bool**| Optional; If false, the original video&#39;s aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to original video frame rate. | [optional]
 **quality** | **int**| Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoConvertToMp4**
> string videoConvertToMp4($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality)

Convert Video to MP4 format.

Automatically detect video file format and convert it to MP4 format. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

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

try {
    $result = $apiInstance->videoConvertToMp4($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoConvertToMp4: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to original video width. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to original video height. | [optional]
 **preserve_aspect_ratio** | **bool**| Optional; If false, the original video&#39;s aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to original video frame rate. | [optional]
 **quality** | **int**| Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoConvertToStillFrames**
> \Swagger\Client\Model\StillFramesResult videoConvertToStillFrames($input_file, $file_url, $max_width, $max_height, $frames_per_second)

Convert Video to PNG Still Frames.

Automatically detect video file format and convert it to an array of still frame PNG images. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time.

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
$frames_per_second = 8.14; // float | Optional; How many video frames per second to be returned as PNG images. Minimum value is 0.1, maximum is 60. Default is 1 frame per second. Maximum of 2000 total frames.

try {
    $result = $apiInstance->videoConvertToStillFrames($input_file, $file_url, $max_width, $max_height, $frames_per_second);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoConvertToStillFrames: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to original video width. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to original video height. | [optional]
 **frames_per_second** | **float**| Optional; How many video frames per second to be returned as PNG images. Minimum value is 0.1, maximum is 60. Default is 1 frame per second. Maximum of 2000 total frames. | [optional]

### Return type

[**\Swagger\Client\Model\StillFramesResult**](../Model/StillFramesResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoConvertToWebm**
> string videoConvertToWebm($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality)

Convert Video to WEBM format.

Automatically detect video file format and convert it to WEBM format. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

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

try {
    $result = $apiInstance->videoConvertToWebm($input_file, $file_url, $max_width, $max_height, $preserve_aspect_ratio, $frame_rate, $quality);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoConvertToWebm: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to original video width. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to original video height. | [optional]
 **preserve_aspect_ratio** | **bool**| Optional; If false, the original video&#39;s aspect ratio will not be preserved, allowing customization of the aspect ratio using maxWidth and maxHeight, potentially skewing the video. Default is true. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to original video frame rate. | [optional]
 **quality** | **int**| Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoCutVideo**
> string videoCutVideo($input_file, $file_url, $start_time, $time_span)

Cut a Video to a Shorter Length

Cuts a video to the specified start and end times. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

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
$start_time = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional; Specify the desired starting time of the cut video in TimeSpan format.
$time_span = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional; Specify the desired length of the cut video in TimeSpan format. Leave blank to include the rest of the video. Maximum time is 4 hours.

try {
    $result = $apiInstance->videoCutVideo($input_file, $file_url, $start_time, $time_span);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoCutVideo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **start_time** | **\DateTime**| Optional; Specify the desired starting time of the cut video in TimeSpan format. | [optional]
 **time_span** | **\DateTime**| Optional; Specify the desired length of the cut video in TimeSpan format. Leave blank to include the rest of the video. Maximum time is 4 hours. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoGetInfo**
> \Swagger\Client\Model\MediaInformation videoGetInfo($input_file, $file_url)

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
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]

### Return type

[**\Swagger\Client\Model\MediaInformation**](../Model/MediaInformation.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoResizeVideo**
> string videoResizeVideo($input_file, $file_url, $max_width, $max_height, $frame_rate, $quality, $extension)

Resizes a Video Preserving the Original Aspect Ratio.

Resizes a video, while maintaining the original aspect ratio and encoding. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

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
$frame_rate = 56; // int | Optional; Specify the frame rate of the output video. Defaults to original video frame rate.
$quality = 56; // int | Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50.
$extension = "extension_example"; // string | Optional; Specify the file extension of the input video. This is recommended when inputting a file directly, without a file name. If no file name is available and no extension is provided, the extension will be inferred from the file data, which may cause a different extension to be used in the output.

try {
    $result = $apiInstance->videoResizeVideo($input_file, $file_url, $max_width, $max_height, $frame_rate, $quality, $extension);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoResizeVideo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to original video width. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to original video height. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to original video frame rate. | [optional]
 **quality** | **int**| Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50. | [optional]
 **extension** | **string**| Optional; Specify the file extension of the input video. This is recommended when inputting a file directly, without a file name. If no file name is available and no extension is provided, the extension will be inferred from the file data, which may cause a different extension to be used in the output. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoResizeVideoSimple**
> string videoResizeVideoSimple($input_file, $file_url, $max_width, $max_height, $frame_rate, $quality, $extension)

Resizes a Video without Preserving Aspect Ratio.

Resizes a video without maintaining original aspect ratio, allowing fully customizable dimensions. May cause image skewing. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

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
$frame_rate = 56; // int | Optional; Specify the frame rate of the output video. Defaults to original video frame rate.
$quality = 56; // int | Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50.
$extension = "extension_example"; // string | Optional; Specify the file extension of the input video. This is recommended when inputting a file directly, without a file name. If no file name is available and no extension is provided, the extension will be inferred from the file data, which may cause a different extension to be used in the output.

try {
    $result = $apiInstance->videoResizeVideoSimple($input_file, $file_url, $max_width, $max_height, $frame_rate, $quality, $extension);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoResizeVideoSimple: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **max_width** | **int**| Optional; Maximum width of the output video, up to the original video width. Defaults to original video width. | [optional]
 **max_height** | **int**| Optional; Maximum height of the output video, up to the original video width. Defaults to original video height. | [optional]
 **frame_rate** | **int**| Optional; Specify the frame rate of the output video. Defaults to original video frame rate. | [optional]
 **quality** | **int**| Optional; Specify the quality of the output video, where 100 is lossless and 1 is the lowest possible quality with highest compression. Default is 50. | [optional]
 **extension** | **string**| Optional; Specify the file extension of the input video. This is recommended when inputting a file directly, without a file name. If no file name is available and no extension is provided, the extension will be inferred from the file data, which may cause a different extension to be used in the output. | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoScanForNsfw**
> \Swagger\Client\Model\NsfwResult videoScanForNsfw($input_file, $file_url, $frames_per_second)

Scan a Video for NSFW content.

Automatically detect video file format and scan it for Not Safe For Work (NSFW)/Porn/Racy content. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, OGV, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per frame scanned.

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
$file_url = "file_url_example"; // string | Optional; URL of a video file being scanned. Use this option for files larger than 2GB.
$frames_per_second = 8.14; // float | Optional; How many video frames per second to be scanned. Minimum value is 0.05 (1 frame per 20 seconds), maximum is 1. Default is 0.33 frame per second (1 frame scanned every 3 seconds). Maximum of 1000 total frames can be scanned, potentially adjusting the framerate for longer videos.

try {
    $result = $apiInstance->videoScanForNsfw($input_file, $file_url, $frames_per_second);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoScanForNsfw: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being scanned. Use this option for files larger than 2GB. | [optional]
 **frames_per_second** | **float**| Optional; How many video frames per second to be scanned. Minimum value is 0.05 (1 frame per 20 seconds), maximum is 1. Default is 0.33 frame per second (1 frame scanned every 3 seconds). Maximum of 1000 total frames can be scanned, potentially adjusting the framerate for longer videos. | [optional]

### Return type

[**\Swagger\Client\Model\NsfwResult**](../Model/NsfwResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **videoSplitVideo**
> \Swagger\Client\Model\SplitVideoResult videoSplitVideo($split_time, $input_file, $file_url, $time_span)

Split a Video into Two Shorter Videos

Cuts a video into two videos based on the specified start time. Supports many input video formats, including AVI, ASF, FLV, MP4, MPEG/MPG, Matroska/WEBM, 3G2, MKV, M4V and MOV. Uses 1 API call per 10 MB of file size. Also uses 1 API call per additional minute of processing time over 5 minutes, up to a maximum of 25 minutes total processing time. Maximum output file size is 50GB.

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
$split_time = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Specify the desired time at which to split the video in TimeSpan format.
$input_file = "/path/to/file.txt"; // \SplFileObject | Input file to perform the operation on.
$file_url = "file_url_example"; // string | Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB.
$time_span = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | Optional; Specify the desired length of the second video in TimeSpan format. Leave blank to include the rest of the video. Maximum time is 4 hours.

try {
    $result = $apiInstance->videoSplitVideo($split_time, $input_file, $file_url, $time_span);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VideoApi->videoSplitVideo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **split_time** | **\DateTime**| Specify the desired time at which to split the video in TimeSpan format. |
 **input_file** | **\SplFileObject**| Input file to perform the operation on. | [optional]
 **file_url** | **string**| Optional; URL of a video file being used for conversion. Use this option for files larger than 2GB. | [optional]
 **time_span** | **\DateTime**| Optional; Specify the desired length of the second video in TimeSpan format. Leave blank to include the rest of the video. Maximum time is 4 hours. | [optional]

### Return type

[**\Swagger\Client\Model\SplitVideoResult**](../Model/SplitVideoResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

