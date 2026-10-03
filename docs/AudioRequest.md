# AudioRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input** | [**List[TextInput]**](TextInput.md) |  | 
**metadata** | **Dict[str, object]** | Client-owned metadata returned unchanged with the task. | [optional] 
**model** | **str** | Model id returned by GET /v1/models, or omit / set to &#x60;auto&#x60; to let the gateway auto-route to a backend whose limits fit the request&#39;s input (modalities, dimensions, duration, ...). | [optional] 
**parameters** | [**AudioParameters**](AudioParameters.md) |  | [optional] 
**routing** | [**RoutingDirective**](RoutingDirective.md) |  | [optional] 

## Example

```python
from mmgateway.models.audio_request import AudioRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AudioRequest from a JSON string
audio_request_instance = AudioRequest.from_json(json)
# print the JSON string representation of the object
print(AudioRequest.to_json())

# convert the object into a dict
audio_request_dict = audio_request_instance.to_dict()
# create an instance of AudioRequest from a dict
audio_request_from_dict = AudioRequest.from_dict(audio_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


