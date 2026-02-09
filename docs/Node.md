# Node


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**discarded** | **int** | Whether the node is discarded (0&#x3D;active, 1&#x3D;discarded) | 
**hash_t** | **int** | Node hash value | 
**id** | **int** | Unique node identifier | 
**type_name** | **str** | Type of the node/device (e.g., camera, sensor, keypad) | 

## Example

```python
from openapi_client.models.node import Node

# TODO update the JSON string below
json = "{}"
# create an instance of Node from a JSON string
node_instance = Node.from_json(json)
# print the JSON string representation of the object
print(Node.to_json())

# convert the object into a dict
node_dict = node_instance.to_dict()
# create an instance of Node from a dict
node_from_dict = Node.from_dict(node_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


