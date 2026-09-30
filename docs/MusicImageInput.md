# MusicImageInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] [default to 'reference_image']
**type** | **str** |  | 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.music_image_input import MusicImageInput

# TODO update the JSON string below
json = "{}"
# create an instance of MusicImageInput from a JSON string
music_image_input_instance = MusicImageInput.from_json(json)
# print the JSON string representation of the object
print(MusicImageInput.to_json())

# convert the object into a dict
music_image_input_dict = music_image_input_instance.to_dict()
# create an instance of MusicImageInput from a dict
music_image_input_from_dict = MusicImageInput.from_dict(music_image_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


