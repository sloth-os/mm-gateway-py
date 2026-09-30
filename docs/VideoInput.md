# VideoInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] [default to 'reference_video']
**type** | **str** |  | 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.video_input import VideoInput

# TODO update the JSON string below
json = "{}"
# create an instance of VideoInput from a JSON string
video_input_instance = VideoInput.from_json(json)
# print the JSON string representation of the object
print(VideoInput.to_json())

# convert the object into a dict
video_input_dict = video_input_instance.to_dict()
# create an instance of VideoInput from a dict
video_input_from_dict = VideoInput.from_dict(video_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


