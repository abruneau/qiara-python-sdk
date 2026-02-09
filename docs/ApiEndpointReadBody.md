# ApiEndpointReadBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**list** | [**List[ApiEndpointReadBodyListInner]**](ApiEndpointReadBodyListInner.md) | List of nodes and endpoints to read | 

## Example

```python
from openapi_client.models.api_endpoint_read_body import ApiEndpointReadBody

# TODO update the JSON string below
json = "{}"
# create an instance of ApiEndpointReadBody from a JSON string
api_endpoint_read_body_instance = ApiEndpointReadBody.from_json(json)
# print the JSON string representation of the object
print(ApiEndpointReadBody.to_json())

# convert the object into a dict
api_endpoint_read_body_dict = api_endpoint_read_body_instance.to_dict()
# create an instance of ApiEndpointReadBody from a dict
api_endpoint_read_body_from_dict = ApiEndpointReadBody.from_dict(api_endpoint_read_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


