# VoiceParameters


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **str** |  | [optional] 
**name** | **str** |  | 
**remove_background_noise** | **bool** |  | [optional] 

## Example

```python
from mmgateway.models.voice_parameters import VoiceParameters

# TODO update the JSON string below
json = "{}"
# create an instance of VoiceParameters from a JSON string
voice_parameters_instance = VoiceParameters.from_json(json)
# print the JSON string representation of the object
print(VoiceParameters.to_json())

# convert the object into a dict
voice_parameters_dict = voice_parameters_instance.to_dict()
# create an instance of VoiceParameters from a dict
voice_parameters_from_dict = VoiceParameters.from_dict(voice_parameters_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


