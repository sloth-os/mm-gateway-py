# VideoImageInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] [default to 'first_frame']
**type** | **str** |  | 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.video_image_input import VideoImageInput

# TODO update the JSON string below
json = "{}"
# create an instance of VideoImageInput from a JSON string
video_image_input_instance = VideoImageInput.from_json(json)
# print the JSON string representation of the object
print(VideoImageInput.to_json())

# convert the object into a dict
video_image_input_dict = video_image_input_instance.to_dict()
# create an instance of VideoImageInput from a dict
video_image_input_from_dict = VideoImageInput.from_dict(video_image_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


