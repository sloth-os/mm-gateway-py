# RoutingDirective

Steer auto mode: policy, ordering, cost ceiling, fallbacks and budget scope.  See docs/design/auto-mode.md. Every member is optional.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**budget** | [**BudgetDirective**](BudgetDirective.md) |  | [optional] 
**fallback** | **str** | Pinned models only: &#x60;none&#x60; (default) tries one backend, &#x60;same_model&#x60; every backend/account serving the model, &#x60;any&#x60; also the replacement and the auto candidates when the model is retired or unavailable. | [optional] 
**max_cost_usd** | **float** | Hard per-task ceiling on the estimated cost in USD; unpriced models are excluded. | [optional] 
**optimize** | **str** | How admissible candidates are ordered (default: the gateway&#39;s default, &#x60;balanced&#x60;). | [optional] 
**profile** | **str** | Gateway-defined routing profile, such as &#x60;quality&#x60;, &#x60;fast&#x60;, or &#x60;eu&#x60;. It never names a provider or backend. | [optional] 

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


