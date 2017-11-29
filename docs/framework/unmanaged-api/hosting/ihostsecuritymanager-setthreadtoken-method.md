---
title: "IHostSecurityManager::SetThreadToken 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostSecurityManager.SetThreadToken
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostSecurityManager::SetThreadToken
helpviewer_keywords:
- SetThreadToken method [.NET Framework hosting]
- IHostSecurityManager::SetThreadToken method [.NET Framework hosting]
ms.assetid: e951c345-8a86-4587-911b-a1a57bc6428a
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 49a505af3ef7d0208af7c65713e615fd44253e93
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="ihostsecuritymanagersetthreadtoken-method"></a><span data-ttu-id="a5578-102">IHostSecurityManager::SetThreadToken 方法</span><span class="sxs-lookup"><span data-stu-id="a5578-102">IHostSecurityManager::SetThreadToken Method</span></span>
<span data-ttu-id="a5578-103">设置当前执行线程的句柄。</span><span class="sxs-lookup"><span data-stu-id="a5578-103">Sets a handle for the currently executing thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a5578-104">语法</span><span class="sxs-lookup"><span data-stu-id="a5578-104">Syntax</span></span>  
  
```  
HRESULT SetThreadToken (  
    [in] HANDLE hToken  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a5578-105">参数</span><span class="sxs-lookup"><span data-stu-id="a5578-105">Parameters</span></span>  
 `hToken`  
 <span data-ttu-id="a5578-106">[in]要设置与当前正在执行的线程的标记句柄。</span><span class="sxs-lookup"><span data-stu-id="a5578-106">[in] A handle to the token to set for the currently executing thread.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a5578-107">返回值</span><span class="sxs-lookup"><span data-stu-id="a5578-107">Return Value</span></span>  
  
|<span data-ttu-id="a5578-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a5578-108">HRESULT</span></span>|<span data-ttu-id="a5578-109">描述</span><span class="sxs-lookup"><span data-stu-id="a5578-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a5578-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5578-110">S_OK</span></span>|<span data-ttu-id="a5578-111">`SetThreadToken`已成功返回。</span><span class="sxs-lookup"><span data-stu-id="a5578-111">`SetThreadToken` returned successfully.</span></span>|  
|<span data-ttu-id="a5578-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a5578-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a5578-113">公共语言运行时 (CLR) 尚未加载到进程中，或 CLR 处于不能运行托管的代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="a5578-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a5578-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a5578-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a5578-115">调用操作已超时。</span><span class="sxs-lookup"><span data-stu-id="a5578-115">The call timed out.</span></span>|  
|<span data-ttu-id="a5578-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a5578-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a5578-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="a5578-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a5578-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a5578-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a5578-119">事件已被取消时被阻塞的线程，或者纤程正在等待它。</span><span class="sxs-lookup"><span data-stu-id="a5578-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a5578-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a5578-120">E_FAIL</span></span>|<span data-ttu-id="a5578-121">出现未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="a5578-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a5578-122">如果某方法返回 E_FAIL，CLR 不再可用进程内。</span><span class="sxs-lookup"><span data-stu-id="a5578-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a5578-123">到托管方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="a5578-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a5578-124">备注</span><span class="sxs-lookup"><span data-stu-id="a5578-124">Remarks</span></span>  
 <span data-ttu-id="a5578-125">`IHostSecurityManager::SetThreadToken`行为同样与对应的 Win32 函数的相同的名称，只不过 Win32 函数允许调用方传入到任意线程句柄，而`IHostSecurityManager::SetThreadToken`可以将令牌仅与当前正在执行的线程关联。</span><span class="sxs-lookup"><span data-stu-id="a5578-125">`IHostSecurityManager::SetThreadToken` behaves similarly to the corresponding Win32 function of the same name, except that the Win32 function allows the caller to pass in a handle to an arbitrary thread, while `IHostSecurityManager::SetThreadToken` can associate a token only with the currently executing thread.</span></span>  
  
 <span data-ttu-id="a5578-126">`HANDLE`类型不是 COM 兼容; 即，其大小是特定于操作系统，要求自定义封送处理。</span><span class="sxs-lookup"><span data-stu-id="a5578-126">The `HANDLE` type is not COM-compliant; that is, its size is specific to an operating system and it requires custom marshaling.</span></span> <span data-ttu-id="a5578-127">因此，此令牌是仅在 CLR 与主机之间的流程内使用。</span><span class="sxs-lookup"><span data-stu-id="a5578-127">Thus, this token is for use only within the process, between the CLR and the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a5578-128">要求</span><span class="sxs-lookup"><span data-stu-id="a5578-128">Requirements</span></span>  
 <span data-ttu-id="a5578-129">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a5578-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5578-130">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a5578-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a5578-131">**库：**作为 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="a5578-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a5578-132">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5578-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5578-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a5578-133">See Also</span></span>  
 [<span data-ttu-id="a5578-134">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="a5578-134">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)  
 [<span data-ttu-id="a5578-135">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="a5578-135">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)