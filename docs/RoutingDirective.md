# RoutingDirective

Select a server-defined, provider-neutral routing policy.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile** | **str** | Gateway-defined routing profile, such as &#x60;quality&#x60;, &#x60;fast&#x60;, or &#x60;eu&#x60;. It never names a provider or backend. | 

## Example

```python
from mmgateway.models.routing_directive import RoutingDirective

# TODO update the JSON string below
json = "{}"
# create an instance of RoutingDirective from a JSON string
routing_directive_instance = RoutingDirective.from_json(json)
# print the JSON string representation of the object
print(RoutingDirective.to_json())

# convert the object into a dict
routing_directive_dict = routing_directive_instance.to_dict()
# create an instance of RoutingDirective from a dict
routing_directive_from_dict = RoutingDirective.from_dict(routing_directive_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


