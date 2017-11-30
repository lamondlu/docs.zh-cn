---
title: "ICorDebugManagedCallback2::CreateConnection 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback2.CreateConnection
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback2::CreateConnection
helpviewer_keywords:
- CreateConnection method [.NET Framework debugging]
- ICorDebugManagedCallback2::CreateConnection method [.NET Framework debugging]
ms.assetid: 49e647be-9d63-4250-9d11-704e2a400d1b
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 716321508c18a415dc8e5c1c3e7e350deaf00a4f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmanagedcallback2createconnection-method"></a><span data-ttu-id="1ecf9-102">ICorDebugManagedCallback2::CreateConnection 方法</span><span class="sxs-lookup"><span data-stu-id="1ecf9-102">ICorDebugManagedCallback2::CreateConnection Method</span></span>
<span data-ttu-id="1ecf9-103">通知调试器已创建新的连接。</span><span class="sxs-lookup"><span data-stu-id="1ecf9-103">Notifies the debugger that a new connection has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ecf9-104">语法</span><span class="sxs-lookup"><span data-stu-id="1ecf9-104">Syntax</span></span>  
  
```  
HRESULT CreateConnection (  
    [in] ICorDebugProcess     *pProcess,  
    [in] CONNID               dwConnectionId,  
    [in] WCHAR                *pConnName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1ecf9-105">参数</span><span class="sxs-lookup"><span data-stu-id="1ecf9-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="1ecf9-106">[in]指向一个表示在其中创建连接的过程的"ICorDebugProcess"对象的指针</span><span class="sxs-lookup"><span data-stu-id="1ecf9-106">[in] A pointer to an "ICorDebugProcess" object that represents the process in which the connection was created</span></span>  
  
 `dwConnectionId`  
 <span data-ttu-id="1ecf9-107">[in]新的连接的 ID。</span><span class="sxs-lookup"><span data-stu-id="1ecf9-107">[in] The ID of the new connection.</span></span>  
  
 `pConnName`  
 <span data-ttu-id="1ecf9-108">[in]指向新的连接的名称的指针。</span><span class="sxs-lookup"><span data-stu-id="1ecf9-108">[in] A pointer to the name of the new connection.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1ecf9-109">备注</span><span class="sxs-lookup"><span data-stu-id="1ecf9-109">Remarks</span></span>  
 <span data-ttu-id="1ecf9-110">A`CreateConnection`回调将触发在以下情况：</span><span class="sxs-lookup"><span data-stu-id="1ecf9-110">A `CreateConnection` callback will be fired in either of the following cases:</span></span>  
  
-   <span data-ttu-id="1ecf9-111">当调试器附加到进程，其中包含连接。</span><span class="sxs-lookup"><span data-stu-id="1ecf9-111">When a debugger attaches to a process that contains connections.</span></span> <span data-ttu-id="1ecf9-112">在这种情况下，运行时将生成并调度`CreateConnection`事件和一个[icordebugmanagedcallback2:: Changeconnection](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-changeconnection-method.md)事件过程中每个连接。</span><span class="sxs-lookup"><span data-stu-id="1ecf9-112">In this case, the runtime will generate and dispatch a `CreateConnection` event and a [ICorDebugManagedCallback2::ChangeConnection](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-changeconnection-method.md) event for each connection in the process.</span></span>  
  
-   <span data-ttu-id="1ecf9-113">当主机调用[iclrdebugmanager:: Beginconnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md)中[承载 API](../../../../docs/framework/unmanaged-api/hosting/index.md)。</span><span class="sxs-lookup"><span data-stu-id="1ecf9-113">When a host calls [ICLRDebugManager::BeginConnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md) in the [Hosting API](../../../../docs/framework/unmanaged-api/hosting/index.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ecf9-114">要求</span><span class="sxs-lookup"><span data-stu-id="1ecf9-114">Requirements</span></span>  
 <span data-ttu-id="1ecf9-115">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1ecf9-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ecf9-116">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1ecf9-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1ecf9-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1ecf9-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1ecf9-118">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1ecf9-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ecf9-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1ecf9-119">See Also</span></span>  
 [<span data-ttu-id="1ecf9-120">ICorDebugManagedCallback2 接口</span><span class="sxs-lookup"><span data-stu-id="1ecf9-120">ICorDebugManagedCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md)  
 [<span data-ttu-id="1ecf9-121">ICorDebugManagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="1ecf9-121">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)