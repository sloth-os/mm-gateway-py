# VoiceListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[VoiceResponse]**](VoiceResponse.md) |  | 
**object** | **str** |  | [optional] [default to 'list']

## Example

```python
from mmgateway.models.voice_list_response import VoiceListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of VoiceListResponse from a JSON string
voice_list_response_instance = VoiceListResponse.from_json(json)
# print the JSON string representation of the object
print(VoiceListResponse.to_json())

# convert the object into a dict
voice_list_response_dict = voice_list_response_instance.to_dict()
# create an instance of VoiceListResponse from a dict
voice_list_response_from_dict = VoiceListResponse.from_dict(voice_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


