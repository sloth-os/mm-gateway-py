# ModelSpend


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**modality** | **str** |  | 
**model** | **str** |  | 
**spent_usd** | **float** |  | [optional] [default to 0.0]
**tasks** | **int** |  | [optional] [default to 0]

## Example

```python
from mmgateway.models.model_spend import ModelSpend

# TODO update the JSON string below
json = "{}"
# create an instance of ModelSpend from a JSON string
model_spend_instance = ModelSpend.from_json(json)
# print the JSON string representation of the object
print(ModelSpend.to_json())

# convert the object into a dict
model_spend_dict = model_spend_instance.to_dict()
# create an instance of ModelSpend from a dict
model_spend_from_dict = ModelSpend.from_dict(model_spend_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


