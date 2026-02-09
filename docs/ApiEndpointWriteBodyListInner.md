# ApiEndpointWriteBodyListInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**node_id** | **int** | ID of the node to write to | 
**eps** | **List[object]** | List of endpoint values to write | 

## Example

```python
from openapi_client.models.api_endpoint_write_body_list_inner import ApiEndpointWriteBodyListInner

# TODO update the JSON string below
json = "{}"
# create an instance of ApiEndpointWriteBodyListInner from a JSON string
api_endpoint_write_body_list_inner_instance = ApiEndpointWriteBodyListInner.from_json(json)
# print the JSON string representation of the object
print(ApiEndpointWriteBodyListInner.to_json())

# convert the object into a dict
api_endpoint_write_body_list_inner_dict = api_endpoint_write_body_list_inner_instance.to_dict()
# create an instance of ApiEndpointWriteBodyListInner from a dict
api_endpoint_write_body_list_inner_from_dict = ApiEndpointWriteBodyListInner.from_dict(api_endpoint_write_body_list_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


