---
title: "IMetaDataImport::EnumPermissionSets 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.EnumPermissionSets
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::EnumPermissionSets
helpviewer_keywords:
- EnumPermissionSets method [.NET Framework metadata]
- IMetaDataImport::EnumPermissionSets method [.NET Framework metadata]
ms.assetid: 347d7e5c-c90f-45ad-bd1e-2c7912b0b19c
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 031e97ad1b8180a64bc789ae52e141932d600782
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportenumpermissionsets-method"></a><span data-ttu-id="5f55f-102">IMetaDataImport::EnumPermissionSets 方法</span><span class="sxs-lookup"><span data-stu-id="5f55f-102">IMetaDataImport::EnumPermissionSets Method</span></span>
<span data-ttu-id="5f55f-103">枚举指定的元数据范围内的对象的权限。</span><span class="sxs-lookup"><span data-stu-id="5f55f-103">Enumerates permissions for the objects in a specified metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f55f-104">语法</span><span class="sxs-lookup"><span data-stu-id="5f55f-104">Syntax</span></span>  
  
```  
HRESULT EnumPermissionSets  
   [in, out] HCORENUM      *phEnum,   
   [in]      mdToken       tk,   
   [in]      DWORD         dwActions,  
   [out]     mdPermission  rPermission[],  
   [in]      ULONG         cMax,  
   [out]     ULONG         *pcTokens  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5f55f-105">参数</span><span class="sxs-lookup"><span data-stu-id="5f55f-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="5f55f-106">[在中，out]枚举数指向的指针。</span><span class="sxs-lookup"><span data-stu-id="5f55f-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="5f55f-107">这必须在首次调用此方法为 NULL。</span><span class="sxs-lookup"><span data-stu-id="5f55f-107">This must be NULL for the first call of this method.</span></span>  
  
 `tk`  
 <span data-ttu-id="5f55f-108">[in]元数据标记，用于限制搜索，或者为 NULL 以搜索可能提供给最大的作用域的作用域。</span><span class="sxs-lookup"><span data-stu-id="5f55f-108">[in] A metadata token that limits the scope of the search, or NULL to search the widest scope possible.</span></span>  
  
 `dwActions`  
 <span data-ttu-id="5f55f-109">[in]标志表示<xref:System.Security.Permissions.SecurityAction>值时要包含在`rPermission`，或为零，则返回所有操作。</span><span class="sxs-lookup"><span data-stu-id="5f55f-109">[in] Flags representing the <xref:System.Security.Permissions.SecurityAction> values to include in `rPermission`, or zero to return all actions.</span></span>  
  
 `rPermission`  
 <span data-ttu-id="5f55f-110">[out]用于存储权限标记数组。</span><span class="sxs-lookup"><span data-stu-id="5f55f-110">[out] The array used to store the Permission tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="5f55f-111">[in] `rPermission` 数组的最大大小。</span><span class="sxs-lookup"><span data-stu-id="5f55f-111">[in] The maximum size of the `rPermission` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="5f55f-112">[out]权限标记中返回的数目`rPermission`。</span><span class="sxs-lookup"><span data-stu-id="5f55f-112">[out] The number of Permission tokens returned in `rPermission`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5f55f-113">返回值</span><span class="sxs-lookup"><span data-stu-id="5f55f-113">Return Value</span></span>  
  
|<span data-ttu-id="5f55f-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="5f55f-114">HRESULT</span></span>|<span data-ttu-id="5f55f-115">描述</span><span class="sxs-lookup"><span data-stu-id="5f55f-115">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="5f55f-116">`EnumPermissionSets`已成功返回。</span><span class="sxs-lookup"><span data-stu-id="5f55f-116">`EnumPermissionSets` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="5f55f-117">没有要枚举的标记。</span><span class="sxs-lookup"><span data-stu-id="5f55f-117">There are no tokens to enumerate.</span></span> <span data-ttu-id="5f55f-118">在这种情况下，`pcTokens`为零。</span><span class="sxs-lookup"><span data-stu-id="5f55f-118">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5f55f-119">要求</span><span class="sxs-lookup"><span data-stu-id="5f55f-119">Requirements</span></span>  
 <span data-ttu-id="5f55f-120">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5f55f-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f55f-121">**标头：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="5f55f-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5f55f-122">**库：**作为 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="5f55f-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5f55f-123">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f55f-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f55f-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f55f-124">See Also</span></span>  
 [<span data-ttu-id="5f55f-125">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="5f55f-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="5f55f-126">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="5f55f-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)