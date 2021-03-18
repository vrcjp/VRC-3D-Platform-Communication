# Method - OnlineClient.CreateVrcId  

Create user id through the user information.

```cs
public static Response CreateVrcId(string email, string password);
```
## Parameters
- email `string`  
VRC user's email.

- password `string`  
VRC user's password.

## Returns
 - `Response`  
 The response message.Gets the `VrcId` of a response message.
 
| Fields         |Type        | Description|
| ------         | -------    | -------    |
| Status         | StatusCode | Gets a value that indicates if the Process was successful. |
| StatusDetail   | string     |Processing status |
| Error          | string     |Error Information  |
| VrcId          | string     |User's Id |

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
| USERID_IS_NULL   | The user's email is empty. |
| PASSWORD_NOT_VALID   | The password id  does not exist.  |

