# VRCSDK(Unity) for Entertainment
![](https://github.com/vrcjp/VRC-3D-Platform/blob/main/offline.png)

## Overview
You can use Unity SDK to generate the QrCode for offline scanner.  
Then scan the whole body to generate the human avatar by offline scanner.  
With the VRCSDK download the VrcFile to local, then use SDK to get 3D data(fbx, texture) from VrcFile.  
VrcFile is a high security protected file that only authorized users can access the 3D data.

### Prerequisites
 * Common Client Initialize
```cs
public static void Initialize(string localStorage, bool useDataFactory = true)
```

 * Offline Scanner placed

### Follow the steps to quick start
 1. Download VRC-UnityPackage and import to Unity project.
 2. Confirm the demo src and input your APIKEY.
 3. Open the demo scene and run.
 
### Processing Detail
 1. Use [Initialize](Initialize/README.md) to initialize the VRCSDK by your APIKEY. 
 2. Use [CreateVrcId](CreateVrcId/README.md) to create the VRCID by user email and get the QrCode to scan. 
 3. Scan the whole body by [Offline Scanner](https://www.youtube.com/watch?v=kCm7Gbe2Bp4&feature=emb_imp_woyt) with the QrCode.
 4. Use [GetVrcFileStatus](GetVrcFileStatus/README.md) to get the VrcFile Status.
 5. Use [GetVrcFile](GetVrcFile/README.md) to download the VrcFile to local storage when VrcFile status is OK(Completed).
 6. Use [GetContents](GetContents/README.md) to get the 3D data from VrcFile on local.
 
## Version
1.0

## SDK Info

### Assembly
`VRCSDK.Platform.Entertainment.dll`

### Namespace
`Vrc.Platform.Entertainment.Offline`

### Class
`OfflineClient`

### Methods
####  List of Method  
| Name         | Description|
| ------       | -------    |
| [Initialize](Initialize/README.md)   | Initializes VRCSDK. |
| [CreateVrcId](CreateVrcId/README.md) | Create vrc id through the user information.  |
| [GetVrcFileStatus](GetVrcFileStatus/README.md)  |Get the specified RelationId VrcFile status. |
| [GetVrcFile](GetVrcFile/README.md)   |Get the specified RelationId file and return the file name. |
| [GetContents](GetContents/README.md)  | Get Fbx Contents from local VrcFile. |
