# ApiEndpointReadBodyListInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node_id** | **int** | ID of the node to read from | 
**eps** | **List[str]** | List of endpoint names to read | 

## Example

```python
from openapi_client.models.api_endpoint_read_body_list_inner import ApiEndpointReadBodyListInner

# TODO update the JSON string below
json = "{}"
# create an instance of ApiEndpointReadBodyListInner from a JSON string
api_endpoint_read_body_list_inner_instance = ApiEndpointReadBodyListInner.from_json(json)
# print the JSON string representation of the object
print(ApiEndpointReadBodyListInner.to_json())

# convert the object into a dict
api_endpoint_read_body_list_inner_dict = api_endpoint_read_body_list_inner_instance.to_dict()
# create an instance of ApiEndpointReadBodyListInner from a dict
api_endpoint_read_body_list_inner_from_dict = ApiEndpointReadBodyListInner.from_dict(api_endpoint_read_body_list_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


