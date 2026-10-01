# UsagePeriod


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**end** | **datetime** |  | [optional] 
**kind** | **str** |  | 
**start** | **datetime** |  | [optional] 

## Example

```python
from mmgateway.models.usage_period import UsagePeriod

# TODO update the JSON string below
json = "{}"
# create an instance of UsagePeriod from a JSON string
usage_period_instance = UsagePeriod.from_json(json)
# print the JSON string representation of the object
print(UsagePeriod.to_json())

# convert the object into a dict
usage_period_dict = usage_period_instance.to_dict()
# create an instance of UsagePeriod from a dict
usage_period_from_dict = UsagePeriod.from_dict(usage_period_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


