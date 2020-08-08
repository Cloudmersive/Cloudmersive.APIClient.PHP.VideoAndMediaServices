# NsfwResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**successful** | **bool** | True if the operation was successful, false otherwise | [optional] 
**highest_classification_result** | **string** | The highest NSFW classification of the video | [optional] 
**highest_score** | **double** | The highest NSFW score out of all frames scanned | [optional] 
**total_racy_frames** | **int** | The total number of potentially \&quot;racy\&quot; frames. | [optional] 
**total_nsfw_frames** | **int** | The total number of frames with high probability of NSFW. | [optional] 
**total_frames** | **int** | The total number of frames scanned | [optional] 
**nsfw_scanned_frames** | [**\Swagger\Client\Model\NsfwScannedFrame[]**](NsfwScannedFrame.md) | The NSFW scanning results for each frame | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


