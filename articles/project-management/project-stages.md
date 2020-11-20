---
title: Giai đoạn dự án
description: Chủ đề này cung cấp thông tin về các giai đoạn dự án được cung cấp trong Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127499"
---
# <a name="project-stages"></a><span data-ttu-id="07409-103">Giai đoạn dự án</span><span class="sxs-lookup"><span data-stu-id="07409-103">Project stages</span></span>

<span data-ttu-id="07409-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="07409-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="07409-105">Giai đoạn dự án được thiết kế để phản ánh trạng thái của dự án khi dự án tiến triển.</span><span class="sxs-lookup"><span data-stu-id="07409-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="07409-106">Hệ thống có thể sử dụng các tùy chỉnh để tự động cập nhật các dòng quy trình công việc, Power Automate hoặc tiện ích phần bổ trợ.</span><span class="sxs-lookup"><span data-stu-id="07409-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="07409-107">Các giai đoạn sau được xác định trong dòng quy trình công việc mặc định:</span><span class="sxs-lookup"><span data-stu-id="07409-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="07409-108">Mới</span><span class="sxs-lookup"><span data-stu-id="07409-108">New</span></span>
- <span data-ttu-id="07409-109">Báo giá</span><span class="sxs-lookup"><span data-stu-id="07409-109">Quote</span></span>
- <span data-ttu-id="07409-110">Gói</span><span class="sxs-lookup"><span data-stu-id="07409-110">Plan</span></span>
- <span data-ttu-id="07409-111">Chuyển giao</span><span class="sxs-lookup"><span data-stu-id="07409-111">Deliver</span></span>
- <span data-ttu-id="07409-112">Hoàn tất</span><span class="sxs-lookup"><span data-stu-id="07409-112">Complete</span></span>
- <span data-ttu-id="07409-113">Đóng</span><span class="sxs-lookup"><span data-stu-id="07409-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="07409-114">Mới</span><span class="sxs-lookup"><span data-stu-id="07409-114">New</span></span>

<span data-ttu-id="07409-115">Khi bạn tạo một dự án, giai đoạn dự án sẽ được đặt thành **Mới**.</span><span class="sxs-lookup"><span data-stu-id="07409-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="07409-116">Nếu dự án được tạo ra từ một mẫu, dự án đó có thể có lịch trình, ước tính và nhóm dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="07409-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="07409-117">Nếu không, đó sẽ là một bản phác thảo của dự án và các thành phần còn lại phải được nhập vào.</span><span class="sxs-lookup"><span data-stu-id="07409-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="07409-118">Báo giá</span><span class="sxs-lookup"><span data-stu-id="07409-118">Quote</span></span>

<span data-ttu-id="07409-119">Khi bạn liên kết một dự án với một báo giá hoặc tạo một dự án từ báo giá, giai đoạn dự án được đặt thành **Báo giá** và ngày bắt đầu và ngày kết thúc ước tính được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="07409-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="07409-120">Khi dự án trong giai đoạn **Báo giá**, tab **Bán hàng** trên trang **Thực thể dự án** hiển thị thông tin chi tiết về báo giá.</span><span class="sxs-lookup"><span data-stu-id="07409-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="07409-121">Kế hoạch</span><span class="sxs-lookup"><span data-stu-id="07409-121">Plan</span></span>

<span data-ttu-id="07409-122">Khi bạn thắng báo giá liên kết với dự án, dự án được chuyển đến giai đoạn **Hợp đồng**, giai đoạn dự án được cập nhật thành **Kế hoạch**.</span><span class="sxs-lookup"><span data-stu-id="07409-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="07409-123">Khi dự án ở giai đoạn **Kế hoạch**, trang **Thực thể dự án** hiển thị thông tin chi tiết về hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="07409-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="07409-124">Chuyển giao</span><span class="sxs-lookup"><span data-stu-id="07409-124">Deliver</span></span>

<span data-ttu-id="07409-125">Khi kế hoạch dự án hoàn tất và bạn đã sẵn sàng để bắt đầu dự án, người quản lý dự án nên cập nhật giai đoạn dự án thành **Chuyển giao** để cho biết dự án đã bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="07409-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="07409-126">Hoàn thành</span><span class="sxs-lookup"><span data-stu-id="07409-126">Complete</span></span> 

<span data-ttu-id="07409-127">Khi công việc cho dự án được hoàn thành, người quản lý dự án có thể cập nhật giai đoạn thành **Hoàn thành**.</span><span class="sxs-lookup"><span data-stu-id="07409-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="07409-128">Bằng cách cập nhật giai đoạn dự án thành **Hoàn thành**, người quản lý dự án chỉ ra rằng công việc được hoàn thành 100% nhưng dự án được giữ ở trạng thái mở để mọi mục nhập thời gian hoặc chi phí đang chờ xử lý có thể được ghi lại.</span><span class="sxs-lookup"><span data-stu-id="07409-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="07409-129">Đóng</span><span class="sxs-lookup"><span data-stu-id="07409-129">Close</span></span>

<span data-ttu-id="07409-130">Khi tất cả giao dịch được ghi lại cho dự án, người quản lý dự án có thể cập nhật giai đoạn thành **Đóng**.</span><span class="sxs-lookup"><span data-stu-id="07409-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="07409-131">Tại thời điểm đó, không thể ghi lại giao dịch nào và dự án được đặt thành chế độ chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="07409-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

