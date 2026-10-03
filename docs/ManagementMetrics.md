# ManagementMetrics


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collected_at** | **str** |  | 
**counters** | [**List[CounterSample]**](CounterSample.md) |  | 
**enabled** | **bool** |  | 
**histograms** | [**List[HistogramSample]**](HistogramSample.md) |  | 
**selection** | [**List[SelectionHealth]**](SelectionHealth.md) |  | 

## Example

```python
from mmgateway.models.management_metrics import ManagementMetrics

# TODO update the JSON string below
json = "{}"
# create an instance of ManagementMetrics from a JSON string
management_metrics_instance = ManagementMetrics.from_json(json)
# print the JSON string representation of the object
print(ManagementMetrics.to_json())

# convert the object into a dict
management_metrics_dict = management_metrics_instance.to_dict()
# create an instance of ManagementMetrics from a dict
management_metrics_from_dict = ManagementMetrics.from_dict(management_metrics_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


