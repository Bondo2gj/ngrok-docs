import TCPEdgeIPRestrictionModuleReplaceRequest from './examples/_tcp_edge_ip_restriction_module_replace_request.md';
import TCPEdgeIPRestrictionModuleReplaceResponse from './examples/_tcp_edge_ip_restriction_module_replace_response.md';
import TCPEdgeIPRestrictionModuleGetRequest from './examples/_tcp_edge_ip_restriction_module_get_request.md';
import TCPEdgeIPRestrictionModuleGetResponse from './examples/_tcp_edge_ip_restriction_module_get_response.md';
import TCPEdgeIPRestrictionModuleDeleteRequest from './examples/_tcp_edge_ip_restriction_module_delete_request.md';

# TCP Edge IP Restriction
------------



## Replace TCP Edge IP Restriction Module


### Request

PUT /edges/tcp/{id}/ip_restriction

<TCPEdgeIPRestrictionModuleReplaceRequest />


#### Parameters

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `enabled` | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| `ip_policy_ids` | List&lt;string&gt; | list of all IP policies that will be used to check if a source IP is allowed access to the endpoint |


### Response

Returns a 200 response  on success

<TCPEdgeIPRestrictionModuleReplaceResponse />


#### Fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `enabled` | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| `ip_policies` | [Ref](#api-tcp-edge-ip-restriction-module-replace-fields-ref) |  |

#### Ref fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `id` | string | a resource identifier |
| `uri` | string | a uri for locating a resource |


## Get TCP Edge IP Restriction Module


### Request

GET /edges/tcp/{id}/ip_restriction

<TCPEdgeIPRestrictionModuleGetRequest />


### Response

Returns a 200 response  on success

<TCPEdgeIPRestrictionModuleGetResponse />


#### Fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `enabled` | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| `ip_policies` | [Ref](#api-tcp-edge-ip-restriction-module-get-fields-ref) |  |

#### Ref fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `id` | string | a resource identifier |
| `uri` | string | a uri for locating a resource |


## Delete TCP Edge IP Restriction Module


### Request

DELETE /edges/tcp/{id}/ip_restriction

<TCPEdgeIPRestrictionModuleDeleteRequest />


### Response

Returns a 204 response with no body on success