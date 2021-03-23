---
title: Các loại giai đoạn dự án
description: Chủ đề này cung cấp thông tin về các giai đoạn dự án.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283709"
---
# <a name="project-stage-types"></a><span data-ttu-id="f52ed-103">Các loại giai đoạn dự án</span><span class="sxs-lookup"><span data-stu-id="f52ed-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f52ed-104">Giai đoạn dự án được thiết kế để phản ánh trạng thái của dự án khi dự án tiến triển.</span><span class="sxs-lookup"><span data-stu-id="f52ed-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="f52ed-105">Hệ thống có thể sử dụng các tùy chỉnh để tự động cập nhật các dòng quy trình công việc, Power Automate hoặc tiện ích phần bổ trợ.</span><span class="sxs-lookup"><span data-stu-id="f52ed-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="f52ed-106">Các giai đoạn sau được xác định trong BPF mặc định:</span><span class="sxs-lookup"><span data-stu-id="f52ed-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="f52ed-107">Mới</span><span class="sxs-lookup"><span data-stu-id="f52ed-107">New</span></span>
- <span data-ttu-id="f52ed-108">Báo giá</span><span class="sxs-lookup"><span data-stu-id="f52ed-108">Quote</span></span>
- <span data-ttu-id="f52ed-109">Kế hoạch</span><span class="sxs-lookup"><span data-stu-id="f52ed-109">Plan</span></span>
- <span data-ttu-id="f52ed-110">Chuyển giao</span><span class="sxs-lookup"><span data-stu-id="f52ed-110">Deliver</span></span>
- <span data-ttu-id="f52ed-111">Hoàn thành</span><span class="sxs-lookup"><span data-stu-id="f52ed-111">Complete</span></span>
- <span data-ttu-id="f52ed-112">Đóng</span><span class="sxs-lookup"><span data-stu-id="f52ed-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="f52ed-113">Mới</span><span class="sxs-lookup"><span data-stu-id="f52ed-113">New</span></span>

<span data-ttu-id="f52ed-114">Khi bạn tạo một dự án, giai đoạn dự án sẽ được đặt thành **Mới**.</span><span class="sxs-lookup"><span data-stu-id="f52ed-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="f52ed-115">Nếu dự án được tạo ra từ một mẫu, dự án đó có thể có lịch trình, ước tính và nhóm dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="f52ed-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="f52ed-116">Nếu không, nó chỉ là một bản phác thảo của dự án và các thành phần còn lại phải được nhập vào.</span><span class="sxs-lookup"><span data-stu-id="f52ed-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="f52ed-117">Báo giá</span><span class="sxs-lookup"><span data-stu-id="f52ed-117">Quote</span></span>

<span data-ttu-id="f52ed-118">Khi bạn liên kết một dự án với một báo giá hoặc tạo một dự án từ báo giá, giai đoạn dự án được đặt thành **Báo giá** và ngày bắt đầu và ngày kết thúc ước tính được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="f52ed-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="f52ed-119">Khi dự án trong giai đoạn **Báo giá**, tab **Bán hàng** trên trang **Thực thể dự án** hiển thị thông tin chi tiết về báo giá.</span><span class="sxs-lookup"><span data-stu-id="f52ed-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="f52ed-120">Kế hoạch</span><span class="sxs-lookup"><span data-stu-id="f52ed-120">Plan</span></span>

<span data-ttu-id="f52ed-121">Khi bạn thắng báo giá liên kết với dự án, dự án được chuyển đến giai đoạn **Hợp đồng**, giai đoạn dự án được cập nhật thành **Kế hoạch**.</span><span class="sxs-lookup"><span data-stu-id="f52ed-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="f52ed-122">Khi dự án ở giai đoạn **Kế hoạch**, trang **Thực thể dự án** hiển thị thông tin chi tiết về hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="f52ed-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="f52ed-123">Chuyển giao</span><span class="sxs-lookup"><span data-stu-id="f52ed-123">Deliver</span></span>

<span data-ttu-id="f52ed-124">Khi kế hoạch dự án hoàn tất và bạn đã sẵn sàng để bắt đầu dự án, người quản lý dự án nên cập nhật giai đoạn dự án thành **Chuyển giao** để cho biết dự án đã bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="f52ed-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="f52ed-125">Hoàn thành</span><span class="sxs-lookup"><span data-stu-id="f52ed-125">Complete</span></span> 

<span data-ttu-id="f52ed-126">Khi công việc cho dự án được hoàn thành, người quản lý dự án có thể cập nhật giai đoạn thành **Hoàn thành**.</span><span class="sxs-lookup"><span data-stu-id="f52ed-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="f52ed-127">Bằng cách cập nhật giai đoạn dự án thành **Hoàn thành**, người quản lý dự án chỉ ra rằng công việc được hoàn thành 100% nhưng dự án được giữ ở trạng thái mở để mọi mục nhập thời gian hoặc chi phí đang chờ xử lý có thể được ghi lại.</span><span class="sxs-lookup"><span data-stu-id="f52ed-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="f52ed-128">Đóng</span><span class="sxs-lookup"><span data-stu-id="f52ed-128">Close</span></span>

<span data-ttu-id="f52ed-129">Khi tất cả giao dịch được ghi lại cho dự án, người quản lý dự án có thể cập nhật giai đoạn thành **Đóng**.</span><span class="sxs-lookup"><span data-stu-id="f52ed-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="f52ed-130">Tại thời điểm đó, không thể ghi lại giao dịch nào và dự án được đặt thành chế độ chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="f52ed-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]