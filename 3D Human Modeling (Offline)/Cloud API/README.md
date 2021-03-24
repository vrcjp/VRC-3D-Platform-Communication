# Cloud API for Communication
![](https://github.com/vrcjp/VRC-3D-Platform/blob/main/offline-api.png)

## Overview
You can use API to generate the QrCode for offline scanner.  
Then scan the whole body to generate the human avatar by offline scanner.  
Use API to get 3D data(fbx, texture) stream url from VRC Cloud.  
VrcFile is a high security protected file that only authorized users can access the 3D data.

### Prerequisites
 * Offline Scanner placed

### Follow the steps to quick start
 1. Download demo html
 2. Confirm the demo src and input your APIKEY.
 3. Open the demo on web brower
 
### Processing Detail
 1. Use [CreateVrcId](CreateVrcId/README.md) to create the VRCID by user email and get the QrCode to scan. 
 2. Scan the whole body by [Offline Scanner](https://www.youtube.com/watch?v=kCm7Gbe2Bp4&feature=emb_imp_woyt) with the QrCode.
 3. Use [GetVrcFileStatus](GetVrcFileStatus/README.md) to get the VrcFile Status.
 4. Use [GetContents](GetContents/README.md) to get the 3D data stream url from VRC Cloud.

## Version
1.0

## API
### List of API  
| Name             |Description |
| ------           | -------    |
| [CreateVrcId](CreateVrcId/README.md)    | 	Create user id through the user information.   |
| [GetVrcFileStatus](GetVrcFileStatus/README.md)  |Get the specified RelationId VrcFile status. |
| [GetContents](GetContents/README.md)    |  Get Fbx Contents 3D data stream url from VRC Cloud. |






