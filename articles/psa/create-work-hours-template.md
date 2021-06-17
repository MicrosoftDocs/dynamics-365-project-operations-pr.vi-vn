---
title: Tạo mẫu giờ làm việc
description: Chủ đề này mô tả cách tạo mẫu giờ làm việc trong Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997222"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="71567-103">Tạo mẫu giờ làm việc (Project Service)</span><span class="sxs-lookup"><span data-stu-id="71567-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="71567-104">Để tạo và quản lý dự án, bạn cần phải áp dụng mẫu lịch cho dự án.</span><span class="sxs-lookup"><span data-stu-id="71567-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="71567-105">Mẫu lịch xác định các thuộc tính sau của dự án:</span><span class="sxs-lookup"><span data-stu-id="71567-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="71567-106">Giờ làm việc, bao gồm thời gian bắt đầu và kết thúc</span><span class="sxs-lookup"><span data-stu-id="71567-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="71567-107">Ngày làm việc</span><span class="sxs-lookup"><span data-stu-id="71567-107">Working days</span></span>
- <span data-ttu-id="71567-108">Trường hợp ngoại lệ của lịch, chẳng hạn như những ngày không làm việc</span><span class="sxs-lookup"><span data-stu-id="71567-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="71567-109">Mẫu lịch được áp dụng cho dự án là bản sao của mẫu lịch được xác định trong cài đặt tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="71567-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="71567-110">Nếu bạn thay đổi mẫu lịch, những thay đổi đó sẽ không ảnh hưởng đến giờ làm việc của dự án.</span><span class="sxs-lookup"><span data-stu-id="71567-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="71567-111">Để thay đổi giờ làm việc của dự án, bạn cần áp dụng mẫu mới.</span><span class="sxs-lookup"><span data-stu-id="71567-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="71567-112">Để tạo mẫu lịch cho tổ chức của bạn, có hai yêu cầu chính:</span><span class="sxs-lookup"><span data-stu-id="71567-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="71567-113">Xác định giờ làm việc mong muốn của mẫu bằng cách sử dụng nguồn lực có thể đặt trước mới hoặc hiện có.</span><span class="sxs-lookup"><span data-stu-id="71567-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="71567-114">Tạo mẫu lịch mới và liên kết mẫu với nguồn lực có thể đặt trước.</span><span class="sxs-lookup"><span data-stu-id="71567-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="71567-115">**Xác định số giờ làm việc của mẫu**</span><span class="sxs-lookup"><span data-stu-id="71567-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="71567-116">Truy cập vào **Nguồn lực** \> **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="71567-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="71567-117">Tạo nguồn lực mới để tham chiếu trong mẫu lịch hoặc chọn một nguồn lực hiện có.</span><span class="sxs-lookup"><span data-stu-id="71567-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="71567-118">Chọn tab **Giờ làm việc** của nguồn lực và hoàn thành các hướng dẫn trong [Đặt giờ làm việc cho một nguồn lực](/dynamics365/field-service/set-work-hours-resource.md) để định cấu hình các quy tắc lịch.</span><span class="sxs-lookup"><span data-stu-id="71567-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="71567-119">**Tạo mẫu lịch mới**</span><span class="sxs-lookup"><span data-stu-id="71567-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="71567-120">Chuyển đến phần **Cài đặt** \> **Mẫu lịch**.</span><span class="sxs-lookup"><span data-stu-id="71567-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="71567-121">Chọn **Mới** rồi nhập tên, mô tả và nguồn lực mẫu.</span><span class="sxs-lookup"><span data-stu-id="71567-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="71567-122">Khi nguồn lực được tham chiếu trong mẫu lịch, bản sao lịch của nguồn lực được liên kết với mẫu lịch.</span><span class="sxs-lookup"><span data-stu-id="71567-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="71567-123">Nếu giờ làm việc của mẫu đã sao chép thay đổi, những thay đổi đó sẽ không ảnh hưởng đến mẫu lịch.</span><span class="sxs-lookup"><span data-stu-id="71567-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="71567-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="71567-124">See Also</span></span>  
 [<span data-ttu-id="71567-125">Thiết lập nguồn lực</span><span class="sxs-lookup"><span data-stu-id="71567-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
