# VoiceSampleInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | 

## Example

```python
from mmgateway.models.voice_sample_input import VoiceSampleInput

# TODO update the JSON string below
json = "{}"
# create an instance of VoiceSampleInput from a JSON string
voice_sample_input_instance = VoiceSampleInput.from_json(json)
# print the JSON string representation of the object
print(VoiceSampleInput.to_json())

# convert the object into a dict
voice_sample_input_dict = voice_sample_input_instance.to_dict()
# create an instance of VoiceSampleInput from a dict
voice_sample_input_from_dict = VoiceSampleInput.from_dict(voice_sample_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


