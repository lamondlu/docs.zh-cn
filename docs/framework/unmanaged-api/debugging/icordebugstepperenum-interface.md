---
title: "ICorDebugStepperEnum 接口 1"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugStepperEnum
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugStepperEnum
helpviewer_keywords: ICorDebugStepperEnum interface [.NET Framework debugging]
ms.assetid: 988718c1-1a4a-40f2-a04c-7d67e5cfe1e2
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c0ef1888026a5df59916fe7decc2955760c934d8
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugstepperenum-interface1"></a><span data-ttu-id="f0791-102">ICorDebugStepperEnum 接口 1</span><span class="sxs-lookup"><span data-stu-id="f0791-102">ICorDebugStepperEnum Interface1</span></span>
<span data-ttu-id="f0791-103">实现 ICorDebugEnum 方法，并枚举 ICorDebugStepper 数组。</span><span class="sxs-lookup"><span data-stu-id="f0791-103">Implements ICorDebugEnum methods, and enumerates ICorDebugStepper arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f0791-104">方法</span><span class="sxs-lookup"><span data-stu-id="f0791-104">Methods</span></span>  
  
|<span data-ttu-id="f0791-105">方法</span><span class="sxs-lookup"><span data-stu-id="f0791-105">Method</span></span>|<span data-ttu-id="f0791-106">描述</span><span class="sxs-lookup"><span data-stu-id="f0791-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f0791-107">Next 方法</span><span class="sxs-lookup"><span data-stu-id="f0791-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstepperenum-next-method.md)|<span data-ttu-id="f0791-108">获取指定的数目的`ICorDebugStepper`枚举，从当前位置开始中的实例。</span><span class="sxs-lookup"><span data-stu-id="f0791-108">Gets the specified number of `ICorDebugStepper` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f0791-109">备注</span><span class="sxs-lookup"><span data-stu-id="f0791-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f0791-110">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="f0791-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0791-111">要求</span><span class="sxs-lookup"><span data-stu-id="f0791-111">Requirements</span></span>  
 <span data-ttu-id="f0791-112">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0791-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0791-113">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f0791-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f0791-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f0791-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f0791-115">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0791-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0791-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f0791-116">See Also</span></span>  
 [<span data-ttu-id="f0791-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="f0791-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)