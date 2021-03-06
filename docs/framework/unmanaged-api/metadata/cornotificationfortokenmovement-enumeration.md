---
title: CorNotificationForTokenMovement 枚举
ms.date: 03/30/2017
api_name:
- CorNotificationForTokenMovement
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNotificationForTokenMovement
helpviewer_keywords:
- CorNotificationForTokenMovement enumeration [.NET Framework metadata]
ms.assetid: 1edd1670-976a-4fc8-bef7-7c41e60ad989
topic_type:
- apiref
ms.openlocfilehash: 411fad0accb59431f776c5bd66e8bd3027ddd907
ms.sourcegitcommit: 9a39f2a06f110c9c7ca54ba216900d038aa14ef3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/23/2019
ms.locfileid: "74450157"
---
# <a name="cornotificationfortokenmovement-enumeration"></a>CorNotificationForTokenMovement 枚举
指定在进行标记重新映射时将发送到元数据 API 客户端的通知。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum CorNotificationForTokenMovement {  
  
    MDNotifyDefault             = 0x0000000f,  
    MDNotifyAll                 = 0xffffffff,  
    MDNotifyNone                = 0x00000000,  
    MDNotifyMethodDef           = 0x00000001,  
    MDNotifyMemberRef           = 0x00000002,  
    MDNotifyFieldDef            = 0x00000004,  
    MDNotifyTypeRef             = 0x00000008,  
  
    MDNotifyTypeDef             = 0x00000010,  
    MDNotifyParamDef            = 0x00000020,  
    MDNotifyInterfaceImpl       = 0x00000040,  
    MDNotifyProperty            = 0x00000080,  
    MDNotifyEvent               = 0x00000100,  
    MDNotifySignature           = 0x00000200,  
    MDNotifyTypeSpec            = 0x00000400,  
    MDNotifyCustomAttribute     = 0x00000800,  
    MDNotifySecurityValue       = 0x00001000,  
    MDNotifyPermission          = 0x00002000,  
    MDNotifyModuleRef           = 0x00004000,  
  
    MDNotifyNameSpace           = 0x00008000,  
  
    MDNotifyAssemblyRef         = 0x01000000,  
    MDNotifyFile                = 0x02000000,  
    MDNotifyExportedType        = 0x04000000,  
    MDNotifyResource            = 0x08000000  
  
} CorNotificationForTokenMovement;  
```  
  
## <a name="members"></a>Members  
  
|成员|说明|  
|------------|-----------------|  
|`MDNotifyDefault`|`mdTypeRef`、`mdMethodDef`、`mdMemberRef`或 `mdFieldDef` 标记移动时发出通知。|  
|`MDNotifyAll`|任何标记移动时发出通知。|  
|`MDNotifyNone`|标记移动时不发出通知。|  
|`MDNotifyMethodDef`|`mdMethodDef` 标记移动时发出通知。|  
|`MDNotifyMemberRef`|`mdMemberRef` 标记移动时发出通知。|  
|`MDNotifyFieldDef`|`mdFieldDef` 标记移动时发出通知。|  
|`MDNotifyTypeRef`|`mdTypeRef` 标记移动时发出通知。|  
|`MDNotifyTypeDef`|`mdTypeDef` 标记移动时发出通知。|  
|`MDNotifyParamDef`|`mdParamDef` 标记移动时发出通知。|  
|`MDNotifyInterfaceImpl`|`mdInterfaceImpl` 标记移动时发出通知。|  
|`MDNotifyProperty`|`mdProperty` 标记移动时发出通知。|  
|`MDNotifyEvent`|`mdEvent` 标记移动时发出通知。|  
|`MDNotifySignature`|`mdSignature` 标记移动时发出通知。|  
|`MDNotifyTypeSpec`|`mdTypeSpec` 标记移动时发出通知。|  
|`MDNotifyCustomAttribute`|`mdCustomAttribute` 标记移动时发出通知。|  
|`MDNotifySecurityValue`|`mdSecurityValue` 标记移动时发出通知。|  
|`MDNotifyPermission`|`mdPermission` 标记移动时发出通知。|  
|`MDNotifyModuleRef`|`mdModuleRef` 标记移动时发出通知。|  
|`MDNotifyNameSpace`|`mdNameSpace` 标记移动时发出通知。|  
|`MDNotifyAssemblyRef`|`mdAssemblyRef` 标记移动时发出通知。|  
|`MDNotifyFile`|`mdFile` 标记移动时发出通知。|  
|`MDNotifyExportedType`|`mdExportedType` 标记移动时发出通知。|  
|`MDNotifyResource`|`mdManifestResource` 标记移动时发出通知。|  
  
## <a name="remarks"></a>备注  
 可在元数据合并期间重新映射（即，移动）标记。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** Corhdr。h  
  
 **.NET Framework 版本：** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>另请参阅

- [Metadata 枚举](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
