# WriteEndpointsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**list** | [**List[ApiEndpointWriteBodyListInner]**](ApiEndpointWriteBodyListInner.md) | List of nodes and endpoints to write | 

## Example

```python
from openapi_client.models.write_endpoints_request import WriteEndpointsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of WriteEndpointsRequest from a JSON string
write_endpoints_request_instance = WriteEndpointsRequest.from_json(json)
# print the JSON string representation of the object
print(WriteEndpointsRequest.to_json())

# convert the object into a dict
write_endpoints_request_dict = write_endpoints_request_instance.to_dict()
# create an instance of WriteEndpointsRequest from a dict
write_endpoints_request_from_dict = WriteEndpointsRequest.from_dict(write_endpoints_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


