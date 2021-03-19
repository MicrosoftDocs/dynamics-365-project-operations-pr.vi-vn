---
title: Xác định lịch nguồn lực
description: Chủ đề này cung cấp thông tin về cách xác định lịch giờ làm việc cho các nguồn lực trong Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a7b7c45ad2116519b0369bfd3d7cf6743704f4e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279839"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="6eaca-103">Xác định lịch nguồn lực</span><span class="sxs-lookup"><span data-stu-id="6eaca-103">Define resource calendars</span></span>

<span data-ttu-id="6eaca-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="6eaca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6eaca-105">Mỗi nguồn lực có thể đặt trước làm việc trong một dự án phải có lịch giờ làm việc để xác định tính sẵn sàng.</span><span class="sxs-lookup"><span data-stu-id="6eaca-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="6eaca-106">Giờ làm việc cho một nguồn lực có thể được xác định theo hai cách:</span><span class="sxs-lookup"><span data-stu-id="6eaca-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="6eaca-107">Xác định các quy tắc lịch riêng lẻ cho một nguồn lực</span><span class="sxs-lookup"><span data-stu-id="6eaca-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="6eaca-108">Áp dụng mẫu lịch hiện có cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="6eaca-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="6eaca-109">Xác định giờ làm việc của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="6eaca-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="6eaca-110">Trên menu **Nguồn lực**, hãy chọn **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="6eaca-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="6eaca-111">Từ dạng xem lưới, hãy chọn **Nguồn lực có thể đặt trước**.</span><span class="sxs-lookup"><span data-stu-id="6eaca-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="6eaca-112">Trê trang **Chi tiết nguồn lực**, chọn tab **Giờ làm việc**. Theo mặc định, lịch của nguồn lực có thể đặt chỗ mặc định theo giờ làm việc của mẫu giờ làm việc mặc định được xác định cho tổ chức.</span><span class="sxs-lookup"><span data-stu-id="6eaca-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="6eaca-113">Để cập nhật giờ làm việc, hãy nhấp chuột phải vào ngày bắt đầu của quy tắc lịch được đề xuất sẽ được xác định.</span><span class="sxs-lookup"><span data-stu-id="6eaca-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="6eaca-114">Sử dụng menu quy tắc lịch để xác định quy tắc lịch cho một ngày cụ thể, phần còn lại của chuỗi hoặc toàn bộ lịch.</span><span class="sxs-lookup"><span data-stu-id="6eaca-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="6eaca-115">Sau khi chọn tùy chọn này, bạn có thể xác định:</span><span class="sxs-lookup"><span data-stu-id="6eaca-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="6eaca-116">Ngày trong tuần áp dụng giờ làm việc.</span><span class="sxs-lookup"><span data-stu-id="6eaca-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="6eaca-117">Thời gian làm việc trong mỗi ngày.</span><span class="sxs-lookup"><span data-stu-id="6eaca-117">The working times within each day.</span></span>
    - <span data-ttu-id="6eaca-118">Múi giờ cho quy tắc lịch.</span><span class="sxs-lookup"><span data-stu-id="6eaca-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="6eaca-119">Nếu có thể, thời gian không làm việc cũng có thể được chỉ định cho quy tắc.</span><span class="sxs-lookup"><span data-stu-id="6eaca-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="6eaca-120">Áp dụng mẫu lịch cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="6eaca-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="6eaca-121">Trên menu **Nguồn lực**, hãy chọn **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="6eaca-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="6eaca-122">Từ dạng xem lưới, hãy chọn tối đa 25 **Nguồn lực có thể đặt trước** để cập nhật.</span><span class="sxs-lookup"><span data-stu-id="6eaca-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="6eaca-123">Chọn **Đặt lịch** và một hộp thoại sẽ nhắc bạn với danh sách các mẫu giờ làm việc có sẵn.</span><span class="sxs-lookup"><span data-stu-id="6eaca-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="6eaca-124">Chọn mẫu mà bạn muốn dùng, sau đó chọn **Áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="6eaca-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]