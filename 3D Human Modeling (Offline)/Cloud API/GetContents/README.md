# GetContents
Get avatar's 3D data stream url.  

## Request URL
```
/e/offline/v1/getcontents
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
| RelationId | string   | Unique identification of the 3d model.  |
| VrcId      | string   |VRC user's id. |
| Password   | string   |VRC user's password.|


## Response
| Fields      | Description    |
| -------     | -------        |
| fbxData.fbx | fbxData's url  |
| body.png    | body's url     |
| hair.png    | hair's url     |
| head.png    | head's url     |
| cloth.png   | cloth's url    |
| Status.png  | Status's url   |
| RelationId  | RelationId     |

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
curl https://platform.vrcjp.com/e/offline/v1/getcontents  
-d"{\"VrcId\":\"XXXXXX\", \"RelationId\":\"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX\", \"Password\":\"XXXXXX\" }" 
-H"x-api-key: <ApiKey>"
-H"Content-Type: application/json"
```

 - Response:
```
{"fbxData.fbx":"https://XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/XXXXXX.fbxData.fbx",
"body.png":"https://XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/XXXXXX.body.png",
"Status":"OK",
"RelationId":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"}
```
