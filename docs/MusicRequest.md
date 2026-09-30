# MusicRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input** | [**List[InputInner1]**](InputInner1.md) | Non-empty ordered music-generation inputs. | 
**metadata** | **Dict[str, object]** | Client-owned metadata returned unchanged with the task. | [optional] 
**model** | **str** | Model id returned by GET /v1/models, or omit / set to &#x60;auto&#x60; to let the gateway auto-route to a backend whose limits fit the request&#39;s input (modalities, dimensions, duration, ...). | [optional] 
**parameters** | [**MusicParameters**](MusicParameters.md) |  | [optional] 
**routing** | [**RoutingDirective**](RoutingDirective.md) |  | [optional] 

## Example

```python
from mmgateway.models.music_request import MusicRequest

# TODO update the JSON string below
json = "{}"
# create an instance of MusicRequest from a JSON string
music_request_instance = MusicRequest.from_json(json)
# print the JSON string representation of the object
print(MusicRequest.to_json())

# convert the object into a dict
music_request_dict = music_request_instance.to_dict()
# create an instance of MusicRequest from a dict
music_request_from_dict = MusicRequest.from_dict(music_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


