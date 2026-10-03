# ManagementConfigResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**config** | [**ManagementConfigOutput**](ManagementConfigOutput.md) |  | 
**persistent** | **bool** |  | 
**revision** | **str** |  | 

## Example

```python
from mmgateway.models.management_config_response import ManagementConfigResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ManagementConfigResponse from a JSON string
management_config_response_instance = ManagementConfigResponse.from_json(json)
# print the JSON string representation of the object
print(ManagementConfigResponse.to_json())

# convert the object into a dict
management_config_response_dict = management_config_response_instance.to_dict()
# create an instance of ManagementConfigResponse from a dict
management_config_response_from_dict = ManagementConfigResponse.from_dict(management_config_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


