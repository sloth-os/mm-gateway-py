# VideoAudioInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] [default to 'reference_audio']
**type** | **str** |  | 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.video_audio_input import VideoAudioInput

# TODO update the JSON string below
json = "{}"
# create an instance of VideoAudioInput from a JSON string
video_audio_input_instance = VideoAudioInput.from_json(json)
# print the JSON string representation of the object
print(VideoAudioInput.to_json())

# convert the object into a dict
video_audio_input_dict = video_audio_input_instance.to_dict()
# create an instance of VideoAudioInput from a dict
video_audio_input_from_dict = VideoAudioInput.from_dict(video_audio_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


