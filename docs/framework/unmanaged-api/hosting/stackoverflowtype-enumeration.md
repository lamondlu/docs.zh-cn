---
title: "StackOverflowType 枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: StackOverflowType
api_location: mscoree.dll
api_type: COM
f1_keywords: StackOverflowType
helpviewer_keywords: StackOverflowType enumeration [.NET Framework hosting]
ms.assetid: dab648ad-972b-479c-b129-b4c1dcbd932e
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 64312398c95a33c2bbe136b1c4d03c06cb09aeef
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="stackoverflowtype-enumeration"></a><span data-ttu-id="6aadd-102">StackOverflowType 枚举</span><span class="sxs-lookup"><span data-stu-id="6aadd-102">StackOverflowType Enumeration</span></span>
<span data-ttu-id="6aadd-103">包含值，用于指示堆栈溢出事件的根本原因。</span><span class="sxs-lookup"><span data-stu-id="6aadd-103">Contains values that indicate the underlying cause of a stack overflow event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6aadd-104">语法</span><span class="sxs-lookup"><span data-stu-id="6aadd-104">Syntax</span></span>  
  
```  
typedef enum {  
    SO_Managed,  
    SO_ClrEngine,  
    SO_Other  
} StackOverflowType;  
```  
  
## <a name="members"></a><span data-ttu-id="6aadd-105">成员</span><span class="sxs-lookup"><span data-stu-id="6aadd-105">Members</span></span>  
  
|<span data-ttu-id="6aadd-106">成员</span><span class="sxs-lookup"><span data-stu-id="6aadd-106">Member</span></span>|<span data-ttu-id="6aadd-107">描述</span><span class="sxs-lookup"><span data-stu-id="6aadd-107">Description</span></span>|  
|------------|-----------------|  
|`SO_ClrEngine`|<span data-ttu-id="6aadd-108">堆栈溢出而引起的执行引擎。</span><span class="sxs-lookup"><span data-stu-id="6aadd-108">The stack overflow was caused by the execution engine.</span></span>|  
|`SO_Managed`|<span data-ttu-id="6aadd-109">由托管代码导致堆栈溢出。</span><span class="sxs-lookup"><span data-stu-id="6aadd-109">The stack overflow was caused by managed code.</span></span>|  
|`SO_Other`|<span data-ttu-id="6aadd-110">由非托管代码导致堆栈溢出。</span><span class="sxs-lookup"><span data-stu-id="6aadd-110">The stack overflow was caused by unmanaged code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6aadd-111">备注</span><span class="sxs-lookup"><span data-stu-id="6aadd-111">Remarks</span></span>  
 <span data-ttu-id="6aadd-112">此信息传递给该主机上，通过调用[iactiononclrevent:: Onevent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md)方法。</span><span class="sxs-lookup"><span data-stu-id="6aadd-112">This information is passed to the host through a call to the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6aadd-113">要求</span><span class="sxs-lookup"><span data-stu-id="6aadd-113">Requirements</span></span>  
 <span data-ttu-id="6aadd-114">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6aadd-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6aadd-115">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6aadd-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6aadd-116">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6aadd-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6aadd-117">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6aadd-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6aadd-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6aadd-118">See Also</span></span>  
 [<span data-ttu-id="6aadd-119">承载枚举</span><span class="sxs-lookup"><span data-stu-id="6aadd-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)