#  GetVrcFileStatus

Get the specified RelationId's VrcFile status.  
If RelationId is empty then return the latest VrcFile Status. 

## Request URL
```
/e/online/v1/getvrcfilestatus
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
| VrcId      | string   |VRC user's id. |
| Password   | string   |VRC user's password. |
| RelationId | string   |The specified avatar's relationId.(set empty to get latest VrcFile's status)|

## Response

| Fields    | Description    |
| -------   | -------        |
| Status    | VrcFile Status Code.   |
| Detail    | VrcFile Status Detail info.   |
| RelationId | string   |The specified avatar's relationId. |

## VrcFile Status
| Status    | Description    |
| -------   | -------        |
| Completed | VrcFile has generated successfully. |
| Ready     | wating for input image or zip upload. |
| Pending   | VrcFile is generating. |
| Failed    | VrcFile is generated failed. |

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
```
curl https://platform.vrcjp.com/e/online/v1/getvrcfilestatus 
-d"{\"VrcId\":\"XXXXXX\", \"Password\":\"XXXXXXXXXXXX\", \"RelationId\":\"XXXXXXXXXXXX\"}"
-H"x-api-key: <ApiKey>" 
-H"Content-Type: application/json"
```
 - Response:  
```
{"Status":"Completed","RelationId":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"}

```

