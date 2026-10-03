# VoiceCloneRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**consent** | [**VoiceConsent**](VoiceConsent.md) |  | 
**input** | [**List[VoiceSampleInput]**](VoiceSampleInput.md) |  | 
**metadata** | **Dict[str, object]** | Client-owned metadata returned unchanged with the task. | [optional] 
**model** | **str** | Model id returned by GET /v1/models, or omit / set to &#x60;auto&#x60; to let the gateway auto-route to a backend whose limits fit the request&#39;s input (modalities, dimensions, duration, ...). | [optional] 
**parameters** | [**VoiceParameters**](VoiceParameters.md) |  | 
**routing** | [**RoutingDirective**](RoutingDirective.md) |  | [optional] 

## Example

```python
from mmgateway.models.voice_clone_request import VoiceCloneRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VoiceCloneRequest from a JSON string
voice_clone_request_instance = VoiceCloneRequest.from_json(json)
# print the JSON string representation of the object
print(VoiceCloneRequest.to_json())

# convert the object into a dict
voice_clone_request_dict = voice_clone_request_instance.to_dict()
# create an instance of VoiceCloneRequest from a dict
voice_clone_request_from_dict = VoiceCloneRequest.from_dict(voice_clone_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


