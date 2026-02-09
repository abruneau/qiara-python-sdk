# ApiEndpointWriteBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**list** | [**List[ApiEndpointWriteBodyListInner]**](ApiEndpointWriteBodyListInner.md) | List of nodes and endpoints to write | 

## Example

```python
from openapi_client.models.api_endpoint_write_body import ApiEndpointWriteBody

# TODO update the JSON string below
json = "{}"
# create an instance of ApiEndpointWriteBody from a JSON string
api_endpoint_write_body_instance = ApiEndpointWriteBody.from_json(json)
# print the JSON string representation of the object
print(ApiEndpointWriteBody.to_json())

# convert the object into a dict
api_endpoint_write_body_dict = api_endpoint_write_body_instance.to_dict()
# create an instance of ApiEndpointWriteBody from a dict
api_endpoint_write_body_from_dict = ApiEndpointWriteBody.from_dict(api_endpoint_write_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


