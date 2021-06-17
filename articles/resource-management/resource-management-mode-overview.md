---
title: Tổng quan về chế độ quản lý nguồn lực
description: Chủ đề này cung cấp thông tin về chức năng Quản lý nguồn lực trong Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94db65a2ddbdc6a7226c70907bcce4c45b4a3923
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000912"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="da8b7-103">Tổng quan về chế độ quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="da8b7-103">Resource management modes overview</span></span>

<span data-ttu-id="da8b7-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="da8b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="da8b7-105">Dynamics 365 Project Operations hỗ trợ 2 chế độ để bạn thực hiện quy trình đăng ký tổng thể.</span><span class="sxs-lookup"><span data-stu-id="da8b7-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="da8b7-106">Chế độ quản lý được xác định như một tham số dự án và có thể được sửa đổi nếu nhu cầu kinh doanh của bạn thay đổi.</span><span class="sxs-lookup"><span data-stu-id="da8b7-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="da8b7-107">Chế độ trung tâm</span><span class="sxs-lookup"><span data-stu-id="da8b7-107">Central mode</span></span>
<span data-ttu-id="da8b7-108">Đối với các tổ chức tập trung phân bổ nguồn lực cho các dự án, Chế độ trung tâm cung cấp cách thức để đảm bảo Người quản lý dự án có thể xác định các yêu cầu về nguồn lực ở cấp độ dự án.</span><span class="sxs-lookup"><span data-stu-id="da8b7-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="da8b7-109">Việc thực hiện các yêu cầu về nguồn lực được giao cho Người quản lý nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="da8b7-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="da8b7-110">Người quản lý dự án có thể chấp nhận hoặc từ chối các nguồn lực do Người quản lý nguồn lực đề xuất.</span><span class="sxs-lookup"><span data-stu-id="da8b7-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Chế độ trung tâm](./media/resource-management-central.png)

<span data-ttu-id="da8b7-112">Để quản lý nguồn lực bằng Chế độ trung tâm, hãy xem:</span><span class="sxs-lookup"><span data-stu-id="da8b7-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="da8b7-113">Chỉ định nguồn lực chung có thể đặt trước cho nhiệm vụ và tạo yêu cầu về nguồn lực</span><span class="sxs-lookup"><span data-stu-id="da8b7-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="da8b7-114">Đặt trước nguồn lực được nêu tên từ yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="da8b7-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="da8b7-115">Gửi đề nghị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="da8b7-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="da8b7-116">Thực hiện yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="da8b7-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="da8b7-117">Chấp nhận hoặc từ chối nguồn lực được đề xuất từ yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="da8b7-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="da8b7-118">Chế độ kết hợp</span><span class="sxs-lookup"><span data-stu-id="da8b7-118">Hybrid mode</span></span>
<span data-ttu-id="da8b7-119">Đối với các tổ chức yêu cầu sự linh hoạt trong việc phân bổ nguồn lực, chế độ kết hợp cho phép cả Người quản lý dự án và Người quản lý nguồn lực có khả năng đặt trước nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="da8b7-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Chế độ kết hợp](./media/resource-management-hybrid.png)

<span data-ttu-id="da8b7-121">Ngoài quy trình ở Chế độ trung tâm được hỗ trợ, hãy xem các chủ đề sau để quản lý tất cả các quy trình đặt trước được hỗ trợ khác trong Chế độ kết hợp:</span><span class="sxs-lookup"><span data-stu-id="da8b7-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="da8b7-122">Đặt trước nguồn lực trực tiếp cho dự án:</span><span class="sxs-lookup"><span data-stu-id="da8b7-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="da8b7-123">Đặt trước nguồn lực có thể đặt lịch có tên cho nhóm dự án và chỉ định nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="da8b7-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="da8b7-124">Đặt trước nguồn lực từ yêu cầu nguồn lực:</span><span class="sxs-lookup"><span data-stu-id="da8b7-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="da8b7-125">Chỉ định nguồn lực chung có thể đặt trước cho nhiệm vụ và tạo yêu cầu về nguồn lực</span><span class="sxs-lookup"><span data-stu-id="da8b7-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="da8b7-126">Đặt trước nguồn lực được nêu tên từ yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="da8b7-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]