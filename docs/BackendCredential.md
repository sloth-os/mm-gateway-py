# BackendCredential


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_key** | **str** |  | [optional] 
**base_url** | **str** |  | [optional] 
**extra** | **Dict[str, object]** |  | [optional] 
**id** | **str** |  | 

## Example

```python
from mmgateway.models.backend_credential import BackendCredential

# TODO update the JSON string below
json = "{}"
# create an instance of BackendCredential from a JSON string
backend_credential_instance = BackendCredential.from_json(json)
# print the JSON string representation of the object
print(BackendCredential.to_json())

# convert the object into a dict
backend_credential_dict = backend_credential_instance.to_dict()
# create an instance of BackendCredential from a dict
backend_credential_from_dict = BackendCredential.from_dict(backend_credential_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


