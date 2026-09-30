# VideoRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input** | [**List[InputInner2]**](InputInner2.md) | Non-empty ordered video-generation inputs. | 
**metadata** | **Dict[str, object]** | Client-owned metadata returned unchanged with the task. | [optional] 
**model** | **str** | Model id returned by GET /v1/models, or omit / set to &#x60;auto&#x60; to let the gateway auto-route to a backend whose limits fit the request&#39;s input (modalities, dimensions, duration, ...). | [optional] 
**parameters** | [**VideoParameters**](VideoParameters.md) |  | [optional] 
**routing** | [**RoutingDirective**](RoutingDirective.md) |  | [optional] 

## Example

```python
from mmgateway.models.video_request import VideoRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VideoRequest from a JSON string
video_request_instance = VideoRequest.from_json(json)
# print the JSON string representation of the object
print(VideoRequest.to_json())

# convert the object into a dict
video_request_dict = video_request_instance.to_dict()
# create an instance of VideoRequest from a dict
video_request_from_dict = VideoRequest.from_dict(video_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


