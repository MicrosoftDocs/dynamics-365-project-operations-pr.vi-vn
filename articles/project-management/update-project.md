---
title: Cập nhật dự án
description: Chủ đề này cung cấp thông tin về cách cập nhật dự án trong Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c07542444b970430d8143a60aad6970305769b22
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993397"
---
# <a name="update-a-project"></a><span data-ttu-id="56c60-103">Cập nhật dự án</span><span class="sxs-lookup"><span data-stu-id="56c60-103">Update a project</span></span>

<span data-ttu-id="56c60-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="56c60-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="56c60-105">Dưới đây là thông tin tóm tắt về các trường có thể được cập nhật trên một dự án sau khi được tạo và mọi chỉ báo có thể áp dụng được của các bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="56c60-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="56c60-106">Các trường chi tiết dự án</span><span class="sxs-lookup"><span data-stu-id="56c60-106">Project detail fields</span></span>

- <span data-ttu-id="56c60-107">**Tên**: Tiêu đề của dự án.</span><span class="sxs-lookup"><span data-stu-id="56c60-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="56c60-108">**Mô tả**: Thông tin tổng quan về dự án.</span><span class="sxs-lookup"><span data-stu-id="56c60-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="56c60-109">**Khách hàng**: Công ty mà dự án sẽ được chuyển giao.</span><span class="sxs-lookup"><span data-stu-id="56c60-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="56c60-110">**Mẫu lịch**: Giờ làm việc của dự án.</span><span class="sxs-lookup"><span data-stu-id="56c60-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="56c60-111">Khi trường được thay đổi, toàn bộ lịch trình sẽ được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="56c60-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="56c60-112">**Tiền tệ**: Đơn vị tiền tệ cho dự án.</span><span class="sxs-lookup"><span data-stu-id="56c60-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="56c60-113">Trường này mặc định dựa trên đơn vị tiền tệ được xác định trong đơn vị ký hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="56c60-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="56c60-114">Khi đơn vị hợp đồng được cập nhật, trường cũng được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="56c60-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="56c60-115">**Đơn vị ký hợp đồng**: Đơn vị tổ chức đại diện cho nhóm hoặc bộ phận của công ty có trách nhiệm chính là giành được hợp đồng bán hàng và quản lý việc cung cấp công việc cũng như dịch vụ cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="56c60-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="56c60-116">**Quản lý dự án** : Thành viên nhóm dự án, người có thẩm quyền xem xét và phê duyệt các mục nhập thời gian và chi phí.</span><span class="sxs-lookup"><span data-stu-id="56c60-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="56c60-117">Trường ước tính</span><span class="sxs-lookup"><span data-stu-id="56c60-117">Estimate fields</span></span>

- <span data-ttu-id="56c60-118">**Ngày bắt đầu dự tính** : Ngày mà dự án sẽ bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="56c60-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="56c60-119">Khi trường này được cập nhật, mọi nhiệm vụ trên dự án sẽ di chuyển tương ứng với ngày bắt đầu mới.</span><span class="sxs-lookup"><span data-stu-id="56c60-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="56c60-120">**Ngày kết thúc**: Ngày dự án kết thúc.</span><span class="sxs-lookup"><span data-stu-id="56c60-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="56c60-121">**Nhân công**: Nhân công ước tính của dự án.</span><span class="sxs-lookup"><span data-stu-id="56c60-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="56c60-122">Khi các nhiệm vụ được thêm vào dự án, trường này không thể chỉnh sửa được nữa.</span><span class="sxs-lookup"><span data-stu-id="56c60-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="56c60-123">**Chi phí lao động ước tính**: Giá nhân công ước tính của dự án.</span><span class="sxs-lookup"><span data-stu-id="56c60-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="56c60-124">Khi chi phí lao động được thêm vào dự án, trường này không thể chỉnh sửa được nữa.</span><span class="sxs-lookup"><span data-stu-id="56c60-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="56c60-125">**Chi phí ước tính**: Các chi phí ước tính của dự án.</span><span class="sxs-lookup"><span data-stu-id="56c60-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="56c60-126">Khi các chi phí được thêm vào dự án, trường này không thể chỉnh sửa được nữa.</span><span class="sxs-lookup"><span data-stu-id="56c60-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="56c60-127">Trường giá trị thực tế của dự án</span><span class="sxs-lookup"><span data-stu-id="56c60-127">Project actual fields</span></span>
- <span data-ttu-id="56c60-128">**Ngày bắt đầu thực tế** : Ngày mà dự án đã bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="56c60-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="56c60-129">**Ngày kết thúc thực tế** : Được cập nhật sau khi dự án đã hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="56c60-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="56c60-130">Trường trạng thái dự án</span><span class="sxs-lookup"><span data-stu-id="56c60-130">Project status fields</span></span>

- <span data-ttu-id="56c60-131">**Trạng thái tổng thể của dự án**: Tình trạng tổng thể của dự án do người quản lý Dự án cung cấp.</span><span class="sxs-lookup"><span data-stu-id="56c60-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="56c60-132">**Nhận xét**: Bản tường thuật về tình trạng hiện tại của dự án do người quản lý Dự án cung cấp.</span><span class="sxs-lookup"><span data-stu-id="56c60-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]