# CreateVrcId

Create VrcId by UserId(Email).

## Request URL
`/common/createvrcid`

## Request Headers
| Name       |Value     | Description|
| ------     | -------  | -------    |
| x-api-key  | \<ApiKey\>|pass this key for call api request |

## Request Method
`POST`

## Request ContentType
`application/json`

## Request Parameter
| Fields     |Type      | Description|
| ------     | -------  | -------    |
| Email      | string   |End User's email|
| Password   | string   |Password for Avatar Access |

## Response
| Fields           |Description |
| ------           | -------    |
| Status        | Status Code     |
| VrcId         | VrcId           |
| RelationId    | Avatar Identify |
| OfflineQrCode | Offline QrCode  |

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
 - Request
```
curl https://platform.vrcjp.com/common/createvrcid 
-d"{\"Email\":\"xxxxxx@example.com\", \"Password\":\"xxxxxx\"}"
-H"x-api-key:<ApiKey>"
-H"Content-Type: application/json"
```

 - Response
```
{"Status":"OK","VrcId":"xxxxxxxx","RelationId":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXX","OfflineQrCode":""}
```
