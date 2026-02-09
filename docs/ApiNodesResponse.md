# ApiNodesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hash_i** | **int** | Hash value for the node list | 
**list** | [**List[Node]**](Node.md) | List of nodes (devices) in the system | 

## Example

```python
from openapi_client.models.api_nodes_response import ApiNodesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ApiNodesResponse from a JSON string
api_nodes_response_instance = ApiNodesResponse.from_json(json)
# print the JSON string representation of the object
print(ApiNodesResponse.to_json())

# convert the object into a dict
api_nodes_response_dict = api_nodes_response_instance.to_dict()
# create an instance of ApiNodesResponse from a dict
api_nodes_response_from_dict = ApiNodesResponse.from_dict(api_nodes_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


