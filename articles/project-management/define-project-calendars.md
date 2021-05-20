---
title: Xác định lịch dự án
description: Chủ đề này cung cấp thông tin về cách áp dụng mẫu lịch cho dự án để theo dõi tiến độ dự án.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981326"
---
# <a name="define-project-calendars"></a><span data-ttu-id="b5505-103">Xác định lịch dự án</span><span class="sxs-lookup"><span data-stu-id="b5505-103">Define project calendars</span></span>

<span data-ttu-id="b5505-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="b5505-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b5505-105">Để tạo và quản lý dự án, bạn cần phải áp dụng mẫu lịch cho dự án.</span><span class="sxs-lookup"><span data-stu-id="b5505-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="b5505-106">Mẫu lịch xác định các thuộc tính sau của dự án:</span><span class="sxs-lookup"><span data-stu-id="b5505-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="b5505-107">Giờ làm việc, bao gồm thời gian bắt đầu và kết thúc</span><span class="sxs-lookup"><span data-stu-id="b5505-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="b5505-108">Ngày làm việc</span><span class="sxs-lookup"><span data-stu-id="b5505-108">Working days</span></span>
- <span data-ttu-id="b5505-109">Trường hợp ngoại lệ của lịch, chẳng hạn như những ngày không làm việc</span><span class="sxs-lookup"><span data-stu-id="b5505-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="b5505-110">Mẫu lịch được áp dụng cho dự án là bản sao của mẫu lịch được xác định trong cài đặt tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="b5505-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="b5505-111">Nếu bạn thay đổi mẫu lịch, những thay đổi đó sẽ không ảnh hưởng đến giờ làm việc của dự án.</span><span class="sxs-lookup"><span data-stu-id="b5505-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="b5505-112">Để thay đổi giờ làm việc của dự án, bạn cần áp dụng mẫu mới.</span><span class="sxs-lookup"><span data-stu-id="b5505-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="b5505-113">Để tạo mẫu lịch cho tổ chức của bạn, có hai yêu cầu chính:</span><span class="sxs-lookup"><span data-stu-id="b5505-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="b5505-114">Xác định giờ làm việc mong muốn của mẫu bằng cách sử dụng nguồn lực có thể đặt trước mới hoặc hiện có.</span><span class="sxs-lookup"><span data-stu-id="b5505-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="b5505-115">Tạo mẫu lịch mới và liên kết mẫu với nguồn lực có thể đặt trước.</span><span class="sxs-lookup"><span data-stu-id="b5505-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="b5505-116">**Xác định số giờ làm việc của mẫu**</span><span class="sxs-lookup"><span data-stu-id="b5505-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="b5505-117">Truy cập vào **Nguồn lực** \> **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="b5505-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="b5505-118">Tạo nguồn lực mới để tham chiếu trong mẫu lịch hoặc chọn một nguồn lực hiện có.</span><span class="sxs-lookup"><span data-stu-id="b5505-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="b5505-119">Chọn tab **Giờ làm việc** của nguồn lực và hoàn thành các hướng dẫn trong [Đặt giờ làm việc cho một nguồn lực](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) để định cấu hình các quy tắc lịch.</span><span class="sxs-lookup"><span data-stu-id="b5505-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="b5505-120">**Tạo mẫu lịch mới**</span><span class="sxs-lookup"><span data-stu-id="b5505-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="b5505-121">Chuyển đến phần **Cài đặt** \> **Mẫu lịch**.</span><span class="sxs-lookup"><span data-stu-id="b5505-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="b5505-122">Chọn **Mới** rồi nhập tên, mô tả và nguồn lực mẫu.</span><span class="sxs-lookup"><span data-stu-id="b5505-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="b5505-123">Khi nguồn lực được tham chiếu trong mẫu lịch, bản sao lịch của nguồn lực được liên kết với mẫu lịch.</span><span class="sxs-lookup"><span data-stu-id="b5505-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="b5505-124">Nếu giờ làm việc của mẫu đã sao chép thay đổi, những thay đổi đó sẽ không ảnh hưởng đến mẫu lịch.</span><span class="sxs-lookup"><span data-stu-id="b5505-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="b5505-125">Bạn hiện có thể liên kết mẫu công việc với mẫu lịch dự án.</span><span class="sxs-lookup"><span data-stu-id="b5505-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

