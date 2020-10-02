---
title: Định cấu hình hoạt động tạo hóa đơn tự động
description: Chủ đề này cung cấp thông tin về cách thức định cấu hình hệ thống để tạo hóa đơn tự động.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898152"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="dce9f-103">Định cấu hình hoạt động tạo hóa đơn tự động</span><span class="sxs-lookup"><span data-stu-id="dce9f-103">Configure automated invoice creation</span></span>

<span data-ttu-id="dce9f-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="dce9f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dce9f-105">Hoàn thành các bước sau để định cấu hình chạy hóa đơn tự động trong Hoạt động dự án.</span><span class="sxs-lookup"><span data-stu-id="dce9f-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="dce9f-106">Chuyển đến **Chế độ cài đặt** \> **Công việc theo lô**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="dce9f-107">Tạo một công việc theo lô rồi đặt tên là **Tạo hóa đơn trong hoạt động dự án**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="dce9f-108">Tên của công việc theo lô phải gồm cụm từ "tạo hóa đơn".</span><span class="sxs-lookup"><span data-stu-id="dce9f-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="dce9f-109">Trong trường **Loại công việc**, hãy chọn **Không**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="dce9f-110">Theo mặc định, các tùy chọn **Tần suất hàng ngày** và **Hiện hoạt** được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="dce9f-111">Chọn **Chạy quy trình làm việc**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-111">Select **Run Workflow**.</span></span> <span data-ttu-id="dce9f-112">Trong hộp thoại **Tra cứu bản ghi**, bạn sẽ thấy 3 quy trình làm việc:</span><span class="sxs-lookup"><span data-stu-id="dce9f-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="dce9f-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="dce9f-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="dce9f-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="dce9f-114">ProcessRunner</span></span>
    - <span data-ttu-id="dce9f-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="dce9f-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="dce9f-116">Chọn **ProcessRunCaller** rồi chọn **Thêm**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="dce9f-117">Trong hộp thoại tiếp theo, hãy chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="dce9f-118">Quy trình làm việc **Ngủ** nằm trước quy trình công việc **Xử lý**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="dce9f-119">Bạn cũng có thể chọn **ProcessRunner** trong bước 5.</span><span class="sxs-lookup"><span data-stu-id="dce9f-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="dce9f-120">Sau đó, khi bạn chọn **OK**, quy trình làm việc **Xử lý** nằm trước quy trình làm việc **Ngủ**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="dce9f-121">Các quy trình làm việc **ProcessRunCaller** và **ProcessRunner** tạo các hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="dce9f-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="dce9f-122">**ProcessRunCaller** gọi **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="dce9f-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="dce9f-123">**ProcessRunner** là quy trình làm việc thực sự tạo ra hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="dce9f-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="dce9f-124">Quy trình này thông qua tất cả mô tả hợp đồng mà các hóa đơn phải được tạo cho và tạo hóa đơn cho các mô tả đó.</span><span class="sxs-lookup"><span data-stu-id="dce9f-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="dce9f-125">Để xác định mô tả hợp đồng mà hóa đơn phải được tạo cho, công việc xem xét ngày chạy hóa đơn cho mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="dce9f-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="dce9f-126">Nếu mô tả hợp đồng thuộc một hợp đồng có cùng ngày chạy hóa đơn, thì các giao dịch được kết hợp thành một hóa đơn và có 2 mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="dce9f-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="dce9f-127">Nếu không có giao dịch để tạo hóa đơn cho, công việc này sẽ bỏ qua bước tạo hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="dce9f-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="dce9f-128">Sau khi **ProcessRunner** chạy xong, quy trình này gọi **ProcessRunCaller**, cung cấp thời gian kết thúc và đóng lại.</span><span class="sxs-lookup"><span data-stu-id="dce9f-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="dce9f-129">Sau đó, **ProcessRunCaller** khởi động bộ hẹn giờ trong 24 giờ từ thời gian kết thúc đã chỉ định.</span><span class="sxs-lookup"><span data-stu-id="dce9f-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="dce9f-130">Khi hết bộ hẹn giờ, **ProcessRunCaller** sẽ đóng lại.</span><span class="sxs-lookup"><span data-stu-id="dce9f-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="dce9f-131">Công việc xử lý lô cho việc tạo hóa đơn là công việc lặp lại.</span><span class="sxs-lookup"><span data-stu-id="dce9f-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="dce9f-132">Nếu quy trình lô này chạy nhiều lần, thì nhiều trường hợp công việc được tạo và gây ra lỗi.</span><span class="sxs-lookup"><span data-stu-id="dce9f-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="dce9f-133">Do đó, bạn chỉ nên bắt đầu quy trình lô một lần và bắt đầu lại chỉ khi quy trình này dừng chạy.</span><span class="sxs-lookup"><span data-stu-id="dce9f-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="dce9f-134">Việc lập hóa đơn theo lô chỉ chạy cho các dòng hợp đồng dự án được định cấu hình theo lịch trình hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="dce9f-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="dce9f-135">Mô tả hợp đồng với phương thức thanh toán giá cố định phải được định cấu hình các mốc.</span><span class="sxs-lookup"><span data-stu-id="dce9f-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="dce9f-136">Mô tả hợp đồng dự án với phương thức thanh toán theo thời gian và vật tư cần thiết lập lịch trình lập hóa đơn theo ngày.</span><span class="sxs-lookup"><span data-stu-id="dce9f-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="dce9f-137">Điều này cũng áp dụng cho mô tả hợp đồng dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="dce9f-137">The same applies to a project-based contract line.</span></span>     
