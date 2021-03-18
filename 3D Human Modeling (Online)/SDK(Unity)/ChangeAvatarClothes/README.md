# Method - OnlineClient.ChangeAvatarClothes  

Create Avatar from specified clothes.

```cs
public static Response ChangeAvatarClothes(string vrcId, string relationIdOrg, string gender, string clothes, string body);
```

## Parameters
- vrcId `string`  
User's VrcId.(*Return by `CreateVrcId` method) 

- relationIdOrg `string`  
The orginal avatar's relationId

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
| RELATIONID_IS_NULL   | The RelationId is empty.  |
| GENDER_IS_NULL   | The gender does not exist.  |
| CLOTHES_IS_NULL   | Clothes code does not exist. |
| BODY_IS_NULL   | The Body size does not exist. |

