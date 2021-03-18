# Method - OnlineClient.GetContents
Get Fbx Contents from local VrcFile

```cs
public static Response GetContents(string vrcId, string password, string relationId);
```

## Parameters
- vrcId `string`  
User's VrcId.(*Return by `CreateVrcId` method)  

- password `string`  
VRC user's password.  

- relationId `string`  
Unique identification of the 3d model(*Return by `CreateAvatarHead` method).  

## Returns
`Response`  
The response message.Gets the `DataInfo` of a response message.  
| Fields         |Type        | Description|
| ------         | -------    | -------    |
| Status         | StatusCode | Gets a value that indicates if the Process was successful. |
| StatusDetail   | string     |Processing status |
| Error          | string     |Error Information  |
| FileInfo       | FileInfo   |File Information |
| DataInfo       | DataInfo   |Data Information |

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

| Error message  | Description|
| ------         | -------    |
| SDK_NOT_INITIALIZE  | The initialized API key does not exist. |
| VRCID_IS_NULL       | The VRC id  does not exist. |
| PASSWORD_NOT_VALID  | The password is not valid.  |
