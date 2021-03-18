# VRC-3D-Platform-Communication
VRC 3D Platform Communication SDK

## Unity SDK
  [3D Human Modeling (Offline)](3D%20Human%20Modeling%20(Offline)/SDK(Unity)/README.md)  
  [3D Human Modeling (Online)](3D%20Human%20Modeling%20(Online)/SDK(Unity)/README.md)

## VRCSDK.Platform.Management
 1. Enable or Disabled the local cache by Initializes VRCSDK.
 2. Make sure the avatar is generated at least once on client app.
 3. After avatar is generated, you can get avatar data without connecting to server.

### Methods
####  List of Method  
| Name         |Function | Description|
| ------       | -------    |-------    |
| Initialize       |public void Initialize(string localStorage)        | Initializes VRCSDK|
| GetAvatarUser    |public AvatarUser GetAvatarUser(string userId)     | Get avater user info by userId  |
| GetAvatarList    |public List<AvatarInfo> GetAvatarList(string vrcId)| Get avatar list by vrcId |
| GetLatestAvatar  |public AvatarInfo GetLatestAvatar(string vrcId, string serviceId)| Get latest avatar info by vrcId and serviceId|
| GetAvatarByCondition  | public AvatarInfo GetAvatarByCondition(string vrcId, string gender, string clothes, string body) | Get avatar info by condtions|
| GetAvatarByRelationId | public AvatarInfo GetAvatarByRelationId(string vrcId, string relationId) | Get avatar info by relationId|
