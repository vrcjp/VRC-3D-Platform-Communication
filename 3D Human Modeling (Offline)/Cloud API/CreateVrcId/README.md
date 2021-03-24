#  CreateVrcId

Create VrcId by UserId(Email).

## Request URL
```
/common/createvrcid
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
| Email      | string   |VRC user's email. |
| Password   | string   |VRC user's password. |


## Response
| Fields        |Description |
| ------        | -------    |
| Status        | Status Code.   |
| VrcId         | Vrc user's Id. |
| RelationId    | Relation Id.   |
| OfflineQrCode | Offline QrCode. |


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
 - Request:  
```
curl https://platform.vrcjp.com/common/createvrcid 
-d"{\"Email\":\"XXXXXXXX@XXXXX.com\", \"Password\":\"XXXXXX\"}"
-H"x-api-key: <ApiKey>"
-H"Content-Type: application/json"
```

 - Response:  
```
{"Status":"OK","VrcId":"XXXXXX","RelationId":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXX","OfflineQrCode":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXX"}
```


