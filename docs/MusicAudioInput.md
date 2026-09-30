# MusicAudioInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] [default to 'reference_audio']
**type** | **str** |  | 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.music_audio_input import MusicAudioInput

# TODO update the JSON string below
json = "{}"
# create an instance of MusicAudioInput from a JSON string
music_audio_input_instance = MusicAudioInput.from_json(json)
# print the JSON string representation of the object
print(MusicAudioInput.to_json())

# convert the object into a dict
music_audio_input_dict = music_audio_input_instance.to_dict()
# create an instance of MusicAudioInput from a dict
music_audio_input_from_dict = MusicAudioInput.from_dict(music_audio_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


