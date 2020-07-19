# cloudmersive_video_api_client
The video APIs help you convert, encode, and transcode videos.

[Cloudmersive Video and Media Services API](https://cloudmersive.com/video-and-media-services-api) - Convert and encode video and media files and content between file formats. On-demand.

- API version: v1
- Package version: 1.0.1


## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/cloudmersive/cloudmersive_video_api_client.git"
    }
  ],
  "require": {
    "cloudmersive/cloudmersive_video_api_client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/cloudmersive_video_api_client/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://api.cloudmersive.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*VideoApi* | [**videoConvertToGif**](docs/Api/VideoApi.md#videoconverttogif) | **POST** /video/convert/to/gif | Convert Video to Animated GIF format.
*VideoApi* | [**videoConvertToMov**](docs/Api/VideoApi.md#videoconverttomov) | **POST** /video/convert/to/mov | Convert Video to MOV format.
*VideoApi* | [**videoConvertToMp4**](docs/Api/VideoApi.md#videoconverttomp4) | **POST** /video/convert/to/mp4 | Convert Video to MP4 format.
*VideoApi* | [**videoConvertToWebm**](docs/Api/VideoApi.md#videoconverttowebm) | **POST** /video/convert/to/webm | Convert Video to WEBM format.
*VideoApi* | [**videoGetInfo**](docs/Api/VideoApi.md#videogetinfo) | **POST** /video/convert/get-info | Get detailed information about a video or audio file


## Documentation For Models

 - [MediaInformation](docs/Model/MediaInformation.md)


## Documentation For Authorization


## Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header


## Author




