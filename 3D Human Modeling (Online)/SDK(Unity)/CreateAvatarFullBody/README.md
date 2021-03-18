# Method - OnlineClient.CreateAvatarFullBody  

Create real body Avatar from face image and body images.

```cs
public static Response CreateAvatarFullBody(string faceImagePath, string bodyImageZipPath, string vrcId, 
                                        string gender, string clothes, int height);
```

```cs
public static Response CreateAvatarFullBody(string faceImagePath, string[] bodyImagePath, string vrcId,  
                                        string gender, string clothes, int height);
```

## Parameters
- faceImagePath `string`  
The face image path

- bodyImageZipPath `string`  
The 8 body images zip

- bodyImagePath `string[]`  
The 8 body images path array

- vrcId `string`  
User's VrcId.(*Return by `CreateVrcId` method) 

- gender `string`  
The gender of person in the image to be scanned(eg. M:male, F:female) 

- clothes `string`  
The clothes code  

- height `string`  
The real body's height (cm) (30 - 300)

## Support Image Extension
- jpg, jpeg, png

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
| CLOTHES_IS_NULL   | The clothes code does not exist. |
| HEIGHT_NOT_VALID   | The body height is not valid. |
| FACE_IMAGEPATH_NOT_EXISTS   | The face image does not exist. |
| BODY_IMAGEPATH_NOT_VALID   | The body image path is not valid. |
| BODY_IMAGE_NOT_EXISTS   | The body image does not exist.|
| BODY_IMAGE_NOT_SUPPORT   | The body image does not support.|
| BODY_IMAGE_TOO_LARGE   | The body image is too large (>10MB).|
| FACE_IMAGE_EXT_NOT_VALID   | The body image does not support.|

