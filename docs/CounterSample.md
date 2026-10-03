# CounterSample


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**labels** | **Dict[str, str]** |  | 
**name** | **str** |  | 
**value** | **float** |  | 

## Example

```python
from mmgateway.models.counter_sample import CounterSample

# TODO update the JSON string below
json = "{}"
# create an instance of CounterSample from a JSON string
counter_sample_instance = CounterSample.from_json(json)
# print the JSON string representation of the object
print(CounterSample.to_json())

# convert the object into a dict
counter_sample_dict = counter_sample_instance.to_dict()
# create an instance of CounterSample from a dict
counter_sample_from_dict = CounterSample.from_dict(counter_sample_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


