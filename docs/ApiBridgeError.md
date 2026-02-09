# ApiBridgeError

Error response from the API

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** | Error message | [optional] 
**code** | **int** | Error code | [optional] 

## Example

```python
from openapi_client.models.api_bridge_error import ApiBridgeError

# TODO update the JSON string below
json = "{}"
# create an instance of ApiBridgeError from a JSON string
api_bridge_error_instance = ApiBridgeError.from_json(json)
# print the JSON string representation of the object
print(ApiBridgeError.to_json())

# convert the object into a dict
api_bridge_error_dict = api_bridge_error_instance.to_dict()
# create an instance of ApiBridgeError from a dict
api_bridge_error_from_dict = ApiBridgeError.from_dict(api_bridge_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


