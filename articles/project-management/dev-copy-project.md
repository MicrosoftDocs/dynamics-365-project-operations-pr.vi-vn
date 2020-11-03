---
title: Phát triển mẫu dự án với chức năng Sao chép dự án
description: Chủ đề này cung cấp thông tin về cách tạo mẫu dự án bằng hành động tùy chỉnh Sao chép dự án.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087048"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="41fa5-103">Phát triển mẫu dự án với chức năng Sao chép dự án</span><span class="sxs-lookup"><span data-stu-id="41fa5-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="41fa5-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="41fa5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="41fa5-105">Dynamics 365 Project Operations hỗ trợ khả năng sao chép dự án và hoàn nguyên mọi mục chỉ định thành các tài nguyên chung đại diện cho vai trò.</span><span class="sxs-lookup"><span data-stu-id="41fa5-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="41fa5-106">Khách hàng có thể sử dụng chức năng này để xây dựng các mẫu dự án cơ bản.</span><span class="sxs-lookup"><span data-stu-id="41fa5-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="41fa5-107">Khi bạn chọn **Sao chép dự án** , trạng thái của dự án mục tiêu sẽ được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="41fa5-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="41fa5-108">Hãy sử dụng **Lý do dẫn đến trạng thái** để xác định thời điểm hoàn tất hành động sao chép.</span><span class="sxs-lookup"><span data-stu-id="41fa5-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="41fa5-109">Thao tác chọn **Sao chép dự án** cũng cập nhật ngày bắt đầu của dự án thành ngày bắt đầu hiện tại nếu không có ngày mục tiêu nào được phát hiện trong thực thể dự án mục tiêu.</span><span class="sxs-lookup"><span data-stu-id="41fa5-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="41fa5-110">Hành động tùy chỉnh Sao chép dự án</span><span class="sxs-lookup"><span data-stu-id="41fa5-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="41fa5-111">Tên</span><span class="sxs-lookup"><span data-stu-id="41fa5-111">Name</span></span> 

<span data-ttu-id="41fa5-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="41fa5-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="41fa5-113">Tham số đầu vào</span><span class="sxs-lookup"><span data-stu-id="41fa5-113">Input parameters</span></span>
<span data-ttu-id="41fa5-114">Có ba tham số đầu vào:</span><span class="sxs-lookup"><span data-stu-id="41fa5-114">There are three input parameters:</span></span>

| <span data-ttu-id="41fa5-115">Tham số</span><span class="sxs-lookup"><span data-stu-id="41fa5-115">Parameter</span></span>          | <span data-ttu-id="41fa5-116">Loại</span><span class="sxs-lookup"><span data-stu-id="41fa5-116">Type</span></span>   | <span data-ttu-id="41fa5-117">Giá trị</span><span class="sxs-lookup"><span data-stu-id="41fa5-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="41fa5-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="41fa5-118">ProjectCopyOption</span></span>  | <span data-ttu-id="41fa5-119">String</span><span class="sxs-lookup"><span data-stu-id="41fa5-119">String</span></span> | <span data-ttu-id="41fa5-120">**{"removeNamedResources":true}** hoặc **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="41fa5-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="41fa5-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="41fa5-121">SourceProject</span></span>      | <span data-ttu-id="41fa5-122">Tham chiếu thực thể</span><span class="sxs-lookup"><span data-stu-id="41fa5-122">Entity Reference</span></span> | <span data-ttu-id="41fa5-123">Dự án nguồn</span><span class="sxs-lookup"><span data-stu-id="41fa5-123">Source Project</span></span> |
| <span data-ttu-id="41fa5-124">Đích</span><span class="sxs-lookup"><span data-stu-id="41fa5-124">Target</span></span>             | <span data-ttu-id="41fa5-125">Tham chiếu thực thể</span><span class="sxs-lookup"><span data-stu-id="41fa5-125">Entity Reference</span></span> | <span data-ttu-id="41fa5-126">Dự án mục tiêu</span><span class="sxs-lookup"><span data-stu-id="41fa5-126">Target Project</span></span> |


- <span data-ttu-id="41fa5-127">**{"clearTeamsAndAssignments":true}** : Hành vi mặc định cho Dự án dành cho web, sẽ loại bỏ tất cả các mục chỉ định và thành viên nhóm.</span><span class="sxs-lookup"><span data-stu-id="41fa5-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="41fa5-128">**{"removeNamedResources":true}** Hành vi mặc định cho Project Operations, sẽ hoàn nguyên các mục chỉ định thành tài nguyên chung.</span><span class="sxs-lookup"><span data-stu-id="41fa5-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="41fa5-129">Để biết thêm các giá trị mặc định trên hành động, hãy xem [Sử dụng hành động Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="41fa5-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="41fa5-130">Chỉ định các trường sẽ sao chép</span><span class="sxs-lookup"><span data-stu-id="41fa5-130">Specify fields to copy</span></span> 
<span data-ttu-id="41fa5-131">Khi **Sao chép dự án** được gọi, hành động này sẽ xem xét mục **Sao chép cột dự án** của dạng xem dự án để xác định những trường nào sẽ được sao chép trong quá trình sao chép dự án.</span><span class="sxs-lookup"><span data-stu-id="41fa5-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
