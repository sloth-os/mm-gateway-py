# ModelEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**modality** | **str** |  | 
**object** | **str** |  | [optional] [default to 'model']

## Example

```python
from mmgateway.models.model_entry import ModelEntry

# TODO update the JSON string below
json = "{}"
# create an instance of ModelEntry from a JSON string
model_entry_instance = ModelEntry.from_json(json)
# print the JSON string representation of the object
print(ModelEntry.to_json())

# convert the object into a dict
model_entry_dict = model_entry_instance.to_dict()
# create an instance of ModelEntry from a dict
model_entry_from_dict = ModelEntry.from_dict(model_entry_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


