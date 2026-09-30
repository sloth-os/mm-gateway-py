# MusicOutput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mime_type** | **str** |  | [optional] 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.music_output import MusicOutput

# TODO update the JSON string below
json = "{}"
# create an instance of MusicOutput from a JSON string
music_output_instance = MusicOutput.from_json(json)
# print the JSON string representation of the object
print(MusicOutput.to_json())

# convert the object into a dict
music_output_dict = music_output_instance.to_dict()
# create an instance of MusicOutput from a dict
music_output_from_dict = MusicOutput.from_dict(music_output_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


