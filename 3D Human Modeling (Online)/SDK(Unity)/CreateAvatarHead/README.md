# Method - OnlineClient.CreateAvatarHead  

Create Human Avatar From Input Image.

```cs
public static Response CreateAvatarHead(string imagePath, string vrcId, string gender, string clothes, string body);
```

## Parameters
- imagePath `string`  
The full path of the image to be scanned  

- vrcId `string`  
User's VrcId.(*Return by `CreateVrcId` method) 

- gender `string`  
The gender of person in the image to be scanned(eg. M:male, F:female) 

- clothes `string`  
The clothes code  

- body `string`  
The default body size  

## Returns
`Response`  
The response message.Gets the `RelationId` of a response message.
| Fields         |Type        | Description|
| ------         | -------    | -------    |
| Status         | StatusCode | Gets a value that indicates if the Process was successful. |
| StatusDetail   | string     |Processing status |
| Error          | string     |Error Information  |
| RelationId     | string     |Unique identification of the 3d model |

## Remarks
 - `StatusDetail`  

| Status message | Description|
| ------         | -------    |
| Ready          | Processing preparation |
| Pending        | Processing   |
| Completed      | Processing Done    |
| Failed         | Processing failed    |
| NotFound       | File not exist    |
| WebException   | Web exception |
| BadRequest     | Bad Request |
| InternalServerError  | a generic error has occurred on the server|
| SystemException      | System exception |


 - `Error`  

| Error message   | Description|
| ------         | -------    |
| SDK_NOT_INITIALIZE  | The initialized API key does not exist. |
| VRCID_IS_NULL   | The VRC id  does not exist. |
| GENDER_IS_NULL   | The gender does not exist.  |
| CLOTHES_IS_NULL   | Clothes code does not exist. |
| BODY_IS_NULL   | The Body size does not exist. |

