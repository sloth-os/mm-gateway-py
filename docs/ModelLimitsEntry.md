# ModelLimitsEntry

A model catalogue entry enriched with its documented input/output limits.  ``limits`` carries the neutral limits the auto-router uses and that a client can consult when crafting a prompt for a specific model. Unknown limits are omitted; clients ignore unknown response members.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**limits** | **Dict[str, object]** | Neutral input/output limits (modalities, max prompt, max output count, supported sizes/durations, role flags, ...). | [optional] 
**modality** | **str** |  | 
**object** | **str** |  | [optional] [default to 'model']

## Example

```python
from mmgateway.models.model_limits_entry import ModelLimitsEntry

# TODO update the JSON string below
json = "{}"
# create an instance of ModelLimitsEntry from a JSON string
model_limits_entry_instance = ModelLimitsEntry.from_json(json)
# print the JSON string representation of the object
print(ModelLimitsEntry.to_json())

# convert the object into a dict
model_limits_entry_dict = model_limits_entry_instance.to_dict()
# create an instance of ModelLimitsEntry from a dict
model_limits_entry_from_dict = ModelLimitsEntry.from_dict(model_limits_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


