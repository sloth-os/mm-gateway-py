# ImageRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input** | [**List[InputInner]**](InputInner.md) | Non-empty ordered image-generation inputs. | 
**metadata** | **Dict[str, object]** | Client-owned metadata returned unchanged with the task. | [optional] 
**model** | **str** | Model id returned by GET /v1/models, or omit / set to &#x60;auto&#x60; to let the gateway auto-route to a backend whose limits fit the request&#39;s input (modalities, dimensions, duration, ...). | [optional] 
**parameters** | [**ImageParameters**](ImageParameters.md) |  | [optional] 
**routing** | [**RoutingDirective**](RoutingDirective.md) |  | [optional] 

## Example

```python
from mmgateway.models.image_request import ImageRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ImageRequest from a JSON string
image_request_instance = ImageRequest.from_json(json)
# print the JSON string representation of the object
print(ImageRequest.to_json())

# convert the object into a dict
image_request_dict = image_request_instance.to_dict()
# create an instance of ImageRequest from a dict
image_request_from_dict = ImageRequest.from_dict(image_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


