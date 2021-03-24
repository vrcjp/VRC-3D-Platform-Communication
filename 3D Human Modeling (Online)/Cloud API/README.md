# Cloud API for Communication
![](https://github.com/vrcjp/VRC-3D-Platform/blob/main/online-api.png)

## Overview
You can use these APIs to generate the avatar by face photo image.  
And then get the 3D data (fbx) from VrcFile.  
VrcFile is a high security protected file that only authorized users can access the 3D data.

### Follow the steps to quick start
 1. Download demo html.
 2. Confirm the demo src and input your APIKEY.
 3. Open the demo html and run.

### Processing Detail
 1. Use [CreateVrcId](CreateVrcId/README.md) to create the VRCID by user email. 
 2. Use [CreateAvatarHead](CreateAvatarHead/README.md) to generate the Avatar from face image.
 3. Generate Avatar from these functions:
    * Use [CreateAvatarHead](CreateAvatarHead/README.md) to generate the Avatar from face image.
      - You will get upload url from the API response.
      - Upload face image from this url.
    * Use [ChangeAvatarClothes](ChangeAvatarClothes/README.md) to generate the Avatar from specified clothes.  
    * Use [CreateAvatarBody](CreateAvatarBody/README.md) to generate the real body Avatar.  
      - You will get upload url from the API response.
      - pack 8 body images to zip file (by VRC JS Utils)
      - Upload zip from this url.
 4. Use [GetContents](GetContents/README.md) to get the 3D data's stream url.

## Version
1.0

## Image requirements
* Image Format:JPG(JPEG)，PNG  
* Image pixel size: minimum 48*48 pixels, maximum 4096*4096 pixels  
* Image file size recommended: 2 MB - 8 MB  
* Minimum face pixel size: The face frame that the system can detect is a square. The minimum side length of the square is one-48th of the short side length of the image, and the minimum value is not less than 48 pixels. For example, if the picture is 4096*3200 pixels, the minimum face pixel size is 66*66 pixels.  

## Real Body Images requirements
 * 8 full body images from different angle
   - start from front image with 45 degrees counterclockwise
   
## API
### List of API  
| Name             |Description |
| ------           | -------    |
| [CreateVrcId](CreateVrcId/README.md)    | 	Create user id through the user information.   |
| [CreateAvatarHead](CreateAvatarHead/README.md) | Create Human Avatar from Input Image.|
| [ChangeAvatarClothes](ChangeAvatarClothes/README.md) | Create Avatar from specified clothes.|
| [CreateAvatarBody](CreateAvatarBody/README.md) | Create real body Avatar from body images.|
| [GetVrcFileStatus](GetVrcFileStatus/README.md)    |  Check VrcFile Status. |
| [GetContents](GetContents/README.md)    |  Get Fbx Contents Url from VRC Cloud. |



