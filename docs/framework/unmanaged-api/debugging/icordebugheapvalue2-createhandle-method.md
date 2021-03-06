---
title: ICorDebugHeapValue2::CreateHandle 方法
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue2.CreateHandle
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue2::CreateHandle
helpviewer_keywords:
- CreateHandle method [.NET Framework debugging]
- ICorDebugHeapValue2::CreateHandle method [.NET Framework debugging]
ms.assetid: fbc418e8-fa22-420d-84ec-e0e1800db041
topic_type:
- apiref
ms.openlocfilehash: c7a1bf3cb10cbc8cdae2788b45e1badaf66a9dbd
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2020
ms.locfileid: "79178877"
---
# <a name="icordebugheapvalue2createhandle-method"></a>ICorDebugHeapValue2::CreateHandle 方法
为此 ICorDebugHeapValue2 对象表示的堆值创建指定类型的句柄。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateHandle (  
    [in] CorDebugHandleType      type,
    [out] ICorDebugHandleValue   **ppHandle  
);  
```  
  
## <a name="parameters"></a>parameters  
 `type`  
 [在]CorDebugHandleType 枚举的值，用于指定要创建的句柄的类型。  
  
 `ppHandle`  
 [出]指向 ICorDebugHandleValue 对象的地址的指针，该对象表示此堆值的新句柄。  
  
## <a name="remarks"></a>备注  
 该句柄将在与堆值关联的应用程序域中创建，如果卸载应用程序域，该句柄将变为无效。  
  
 对同一堆值的多次调用将创建多个句柄。 由于句柄会影响垃圾回收器的性能，调试器应将其限制为一次处于活动状态的相对较少的句柄（约 256）。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET 框架版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
