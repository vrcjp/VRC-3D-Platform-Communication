#  ChangeAvatarClothes

Generate the Avatar from specified clothes.

## Request URL
```
/e/online/v1/changeavatarclothes
```

## Request Headers
| Name       |Value     | Description|
| ------     | -------  | -------    |
| x-api-key  | \<ApiKey\>|pass this key for call api request |

## Request Method
POST  

## Request ContentType
application/json   

## Request parameter
| Fields     |Type      | Description|
| ------     | -------  | -------    |
| VrcId      | string   |VRC user‘s id. |
| RelationIdOrg      | string   |The oringal avatar's relationId. |
| Gender     | string   |The gender of person in the image to be scanned. |
| Clothes    | string   |The clothes code. |
| Body       | string   |The body size (S/M/L). |

## Response

| Fields    | Description    |
| -------   | -------        |
| Status    | Status Code.   |
| RelationId | Unique identification of the 3d model.  |


## Response Codes
| HTTP Status Code  |Message Code  |
| ------            | -------      |
| 200(201)          | Success      |
| 400          | Bad Request       |
| 403          | Forbidden         |
| 404          | Not Found         |
| 408          | Request timeout   |
| 500          | Internal server error |
| 502          | Bad Gateway           |
| 503          | Service unavailable   |
| 504          | Gateway timeout    |


## Examples

### Step1:  
 - Request upload Url.  
```
curl https://platform.vrcjp.com/e/online/v1/createavatarhead 
-d"{\"VrcId\":\"XXXXXX\", \"RelationIdOrg\":\"XXXXXXXXXXXX\", \"Gender\":\"M\", \"Clothes\":\"M\", \"Body\":\"S\"}"
-H"x-api-key: <ApiKey>" 
-H"Content-Type: application/json"
```
 - Response:  
```
{"Status":"OK","RelationId":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"}

```

