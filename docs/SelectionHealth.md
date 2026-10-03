# SelectionHealth


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account** | **str** |  | 
**attempts** | **int** |  | 
**backend** | **str** |  | 
**cooldown_remaining_s** | **float** |  | 
**latency_s** | **float** |  | 
**modality** | **str** |  | 
**model** | **str** |  | 
**rate_limited** | **bool** |  | 
**success_rate** | **float** |  | 

## Example

```python
from mmgateway.models.selection_health import SelectionHealth

# TODO update the JSON string below
json = "{}"
# create an instance of SelectionHealth from a JSON string
selection_health_instance = SelectionHealth.from_json(json)
# print the JSON string representation of the object
print(SelectionHealth.to_json())

# convert the object into a dict
selection_health_dict = selection_health_instance.to_dict()
# create an instance of SelectionHealth from a dict
selection_health_from_dict = SelectionHealth.from_dict(selection_health_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


