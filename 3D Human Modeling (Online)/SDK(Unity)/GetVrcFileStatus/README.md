# Method - OnlineClient.GetVrcFileStatus
Get the specified RelationId's VrcFile status.  
If RelationId is empty then return the latest VrcFile Status. 

```cs
public static Response GetVrcFileStatus(string vrcId, string password, string relationId = "");
```

## Parameters
- vrcId `string`  
User's VrcId.(*Return by `CreateVrcId` method).   

- password `string`  
VRC user's password for accessing avatar. 

- relationId `string`  
Unique identification of the 3d model(*Return by `CreateAvatarHead` method).  

## Returns
 - `Response`  

| Fields         |Type        | Description|
| ------         | -------    | -------    |
| Status         | StatusCode | Gets a value that indicates if the Process was successful. |
| StatusDetail   | string     |Processing status |
| Error          | string     |Error Information  |

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
| ------          | -------    |
| SDK_NOT_INITIALIZE  | The initialized API key does not exist. |
| VRCID_IS_NULL   | The VRC id  does not exist. |
| PASSWORD_NOT_VALID   | The password id  does not exist.  |
| APIKEY_NOT_VALID   | The APIKEY is not valid. |
