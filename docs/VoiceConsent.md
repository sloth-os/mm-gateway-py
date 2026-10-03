# VoiceConsent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**granted** | **bool** | The speaker authorized creation and use of this voice. | 
**language** | **str** |  | [optional] 
**recording_uri** | **str** | Absolute media URI. Inline media uses a base64 data URI. | [optional] 

## Example

```python
from mmgateway.models.voice_consent import VoiceConsent

# TODO update the JSON string below
json = "{}"
# create an instance of VoiceConsent from a JSON string
voice_consent_instance = VoiceConsent.from_json(json)
# print the JSON string representation of the object
print(VoiceConsent.to_json())

# convert the object into a dict
voice_consent_dict = voice_consent_instance.to_dict()
# create an instance of VoiceConsent from a dict
voice_consent_from_dict = VoiceConsent.from_dict(voice_consent_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


