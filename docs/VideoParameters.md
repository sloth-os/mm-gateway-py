# VideoParameters


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**camera_motion** | **str** |  | [optional] 
**dimensions** | [**Dimensions**](Dimensions.md) |  | [optional] 
**duration_seconds** | **float** |  | [optional] 
**enhance_prompt** | **bool** |  | [optional] 
**file_format** | **str** |  | [optional] 
**fps** | **int** |  | [optional] 
**frame_count** | **int** |  | [optional] 
**guidance_scale** | **float** |  | [optional] 
**include_audio** | **bool** |  | [optional] 
**include_last_frame** | **bool** |  | [optional] 
**motion_intensity** | **int** |  | [optional] 
**negative_prompt** | **str** |  | [optional] 
**seed** | **int** |  | [optional] 
**watermark** | **bool** |  | [optional] 

## Example

```python
from mmgateway.models.video_parameters import VideoParameters

# TODO update the JSON string below
json = "{}"
# create an instance of VideoParameters from a JSON string
video_parameters_instance = VideoParameters.from_json(json)
# print the JSON string representation of the object
print(VideoParameters.to_json())

# convert the object into a dict
video_parameters_dict = video_parameters_instance.to_dict()
# create an instance of VideoParameters from a dict
video_parameters_from_dict = VideoParameters.from_dict(video_parameters_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


