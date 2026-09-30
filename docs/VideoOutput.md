# VideoOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cover_uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | [optional] 
**mime_type** | **str** |  | [optional] 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.video_output import VideoOutput

# TODO update the JSON string below
json = "{}"
# create an instance of VideoOutput from a JSON string
video_output_instance = VideoOutput.from_json(json)
# print the JSON string representation of the object
print(VideoOutput.to_json())

# convert the object into a dict
video_output_dict = video_output_instance.to_dict()
# create an instance of VideoOutput from a dict
video_output_from_dict = VideoOutput.from_dict(video_output_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


