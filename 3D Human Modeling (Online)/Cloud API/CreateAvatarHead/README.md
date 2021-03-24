#  CreateAvatarHead

Generate the Avatar from face image.  

## Request URL
```
/e/online/v1/createavatarhead
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
| Gender     | string   |The gender of person in the image to be scanned. |
| ImgExt     | string   |The image's extension. |
| Clothes    | string   |The clothes code. |

## Response

| Fields    | Description    |
| -------   | -------        |
| Status    | Status Code.   |
| Url       | Upload Url.  |
| RelationId | Relation Id.  |


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
Step1:  
 - Request upload Url.  
```
curl https://platform.vrcjp.com/e/online/v1/createavatarhead 
-d"{\"VrcId\":\"e09kg1dn\", \"Gender\":\"M\", \"ImgExt\":\"jpg\", \"Clothes\":\"M\"}"
-H"x-api-key:M9JKaF8sLenr4QsYfZRtvNBPZX8ZV8WF" 
-H"Content-Type: application/json"
```
 - Response:  
```
{"Status":"OK","Url":"https://vrc-platform-avatar-input.s3.ap-northeast-1.amazonaws.com","RelationId":"user_id+tIw3GkAgL1apt5lfrVFSfwcc+vrcapp"}

```

Step2:  
 - Please upload the picture within 5 minutes after obtaining the response's url in step1.  otherwise,failed.
```
curl -X PUT "https://vrc-platform-avatar-input.s3.ap-northeast-1.amazonaws.com"
--upload-file "C:\Users\user\Desktop\tooo.test.jpg"
```

