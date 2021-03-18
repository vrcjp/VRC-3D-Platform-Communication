# VRCSDK(Unity) for Entertainment
![](https://github.com/vrcjp/VRC-3D-Platform/blob/main/online.png)

## Overview
You can use Unity SDK to generate the avatar by face photo image.  
After download the VrcFile to local, then use SDK to get 3D data(fbx, texture) from VrcFile.  
VrcFile is a high security protected file that only authorized users can access the 3D data.

### Prerequisites
 * Common Client Initialize
```cs
public static void Initialize(string localStorage, bool useDataFactory = true)
```

### Follow the steps to quick start
 1. Download VRC-UnityPackage and import to Unity project.
 2. Confirm the demo src and input your APIKEY.
 3. Open the demo scene and run.
 
### Processing Detail
 1. Use [Initialize](Initialize/README.md) to initialize the VRCSDK by your APIKEY. 
 2. Use [CreateVrcId](CreateVrcId/README.md) to create the VRCID by user email.  
 3. Generate Avatar from these functions:
    * Use [CreateAvatarHead](CreateAvatarHead/README.md) to generate the Avatar from face image.
    * Use [ChangeAvatarClothes](ChangeAvatarClothes/README.md) to generate the Avatar from specified clothes.  
    * Use [CreateAvatarBody](CreateAvatarBody/README.md) to generate the real body Avatar from exsits avatar.  
    * Use [CreateAvatarFullBody](CreateAvatarFullBody/README.md) to generate the real body Avatar.  
 4. Use [GetVrcFileStatus](GetVrcFileStatus/README.md) to get the VrcFile Status.
 5. Use [GetVrcFile](GetVrcFile/README.md) to download the VrcFile to local storage when VrcFile status is OK(Completed).
 6. Use [GetContents](GetContents/README.md) to get the 3D data from VrcFile on local.
 
## Version
1.0

## Image requirements
* Image Format: JPG(JPEG)，PNG  
* Image pixel size: minimum 48*48 pixels, maximum 4096*4096 pixels  
* Image file size recommended: 2 MB - 8 MB  
* Minimum face pixel size: The face frame that the system can detect is a square. The minimum side length of the square is one-48th of the short side length of the image, and the minimum value is not less than 48 pixels. For example, if the picture is 4096*3200 pixels, the minimum face pixel size is 66*66 pixels.  

## Real Body Images requirements
 * 8 full body images from different angle
   - start from front image with 45 degrees counterclockwise

## SDK Info

### Assembly
`VRCSDK.Platform.Entertainment.dll`

### Namespace
`Vrc.Platform.Entertainment.Online`

### Class
`OnlineClient`

### Methods
####  List of Method  
| Name         | Description|
| ------       | -------    |
| [Initialize](Initialize/README.md)  | Initializes VRCSDK. |
| [CreateVrcId](CreateVrcId/README.md)  | Create vrc id through the user information.  |
| [CreateAvatarHead](CreateAvatarHead/README.md) | Create Human Avatar from Input Image.|
| [ChangeAvatarClothes](ChangeAvatarClothes/README.md) | Create Avatar from specified clothes.|
| [CreateAvatarBody](CreateAvatarBody/README.md) | Create real body Avatar from body images.|
| [CreateAvatarFullBody](CreateAvatarFullBody/README.md) | Create real body Avatar from face image and body images.|
| [GetVrcFileStatus](GetVrcFileStatus/README.md)  |Get the specified RelationId status. |
| [GetVrcFile](GetVrcFile/README.md)  |Get the specified RelationId VrcFile and return the file name. |
| [GetContents](GetContents/README.md) | Get Fbx Contents from local VrcFile. |

