#  GetContents

Get the url to download 3d data.  

## Request URL
```
/e/online/v1/getcontents
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
| VrcId      | string   |VRC user‘s id. |
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
curl https://platform.vrcjp.com/e/online/v1/getcontents  
-d"{\"VrcId\":\"e09kg1dn\", \"RelationId\":\"user_id+xtabS44rC0DgYHGRXxsXuAcc+vrcapp\", \"Password\":\"Vrcjp2020\" }" 
-H"x-api-key:M9JKaF8sLenr4QsYfZRtvNBPZX8ZV8WF"
-H"Content-Type: application/json"
```

 - Response:
```
{"fbxData.fbx":"https://vrc-platform-avatar-temp.s3.ap-northeast-1.amazonaws.com/E/ONLINE/e4418fead63febfac35d986e5c690db3M.fbxData.fbx",
"body.png":"https://vrc-platform-avatar-temp.s3.ap-northeast-1.amazonaws.com/E/ONLINE/e4418fead63febfac35d986e5c690db3M.body.png",
"hair.png":"https://vrc-platform-avatar-temp.s3.ap-northeast-1.amazonaws.com/E/ONLINE/e4418fead63febfac35d986e5c690db3M.hair.png",
"head.png":"https://vrc-platform-avatar-temp.s3.ap-northeast-1.amazonaws.com/E/ONLINE/e4418fead63febfac35d986e5c690db3M.head.png",
"cloth.png":"https://vrc-platform-avatar-temp.s3.ap-northeast-1.amazonaws.com/E/ONLINE/e4418fead63febfac35d986e5c690db3M.cloth.png",
"Status":"OK","RelationId":"user_id+xtabS44rC0DgYHGRXxsXuAcc+vrcapp"}
```


