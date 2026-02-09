# ReadEndpointsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**list** | [**List[ApiEndpointReadBodyListInner]**](ApiEndpointReadBodyListInner.md) | List of nodes and endpoints to read | 

## Example

```python
from openapi_client.models.read_endpoints_request import ReadEndpointsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ReadEndpointsRequest from a JSON string
read_endpoints_request_instance = ReadEndpointsRequest.from_json(json)
# print the JSON string representation of the object
print(ReadEndpointsRequest.to_json())

# convert the object into a dict
read_endpoints_request_dict = read_endpoints_request_instance.to_dict()
# create an instance of ReadEndpointsRequest from a dict
read_endpoints_request_from_dict = ReadEndpointsRequest.from_dict(read_endpoints_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


