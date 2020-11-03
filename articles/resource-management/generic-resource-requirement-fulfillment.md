---
title: Đáp ứng các yêu về nguồn lực chung
description: Chủ đề này cung cấp thông tin về cách đặt trước nguồn lực được nêu tên cho một yêu cầu nguồn lực chung.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6bb7c185656ff87bb3ca24209594c07d25862d70
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087053"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="333b1-103">Đáp ứng các yêu về nguồn lực chung</span><span class="sxs-lookup"><span data-stu-id="333b1-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="333b1-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="333b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="333b1-105">Bạn có thể đặt một nguồn lực được đặt tên để thay thế nguồn lực chung có yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="333b1-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="333b1-106">Trên trang **Dự án** , chọn tab **Nhóm**.</span><span class="sxs-lookup"><span data-stu-id="333b1-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="333b1-107">Chọn nguồn lực chung có yêu cầu nguồn lực từ danh sách, sau đó chọn **Đặt lịch**.</span><span class="sxs-lookup"><span data-stu-id="333b1-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="333b1-108">Hoặc mở yêu cầu nguồn lực rồi nhấp chọn **Đặt lịch**.</span><span class="sxs-lookup"><span data-stu-id="333b1-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="333b1-109">Trên trang **Trợ lý lịch trình** , chọn nguồn lực có tên để đặt trước vào nhóm dự án của bạn rồi chọn **Đặt lịch**.</span><span class="sxs-lookup"><span data-stu-id="333b1-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="333b1-110">Khi đặt lịch xong và được thực hiện bởi một nguồn lực có tên, thì nguồn lực chung được thay thế bằng nguồn lực có tên đó.</span><span class="sxs-lookup"><span data-stu-id="333b1-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="333b1-111">Các phân công trên lịch trình cũng được cập nhật bằng nguồn lực có tên.</span><span class="sxs-lookup"><span data-stu-id="333b1-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="333b1-112">Hoàn thành một nguồn lực chung với nhiều nguồn lực được đặt tên</span><span class="sxs-lookup"><span data-stu-id="333b1-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="333b1-113">Thực hiện một yêu cầu cho một nguồn lực chung với nhiều nguồn lực có tên sẽ tương tự như việc gán một nguồn lực có tên.</span><span class="sxs-lookup"><span data-stu-id="333b1-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="333b1-114">Ví dụ: có một nhiệm vụ với thời gian năm ngày và 120 giờ làm việc.</span><span class="sxs-lookup"><span data-stu-id="333b1-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="333b1-115">Một nguồn lực không thể hoàn thành nhiệm vụ này trong tám giờ trong năm ngày trong tuần.</span><span class="sxs-lookup"><span data-stu-id="333b1-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="333b1-116">Yêu cầu này là cho 120 giờ kỹ thuật robot trong năm ngày, trong đó mỗi ngày 24 giờ.</span><span class="sxs-lookup"><span data-stu-id="333b1-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="333b1-117">Đây là một ví dụ khi nhiều nguồn lực được đặt tên là cần thiết để hoàn thành một yêu cầu nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="333b1-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="333b1-118">Bạn sẽ cần phải đặt nhiều nguồn lực để hoàn thành yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="333b1-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="333b1-119">Sự khác biệt chính trong trường hợp này là nguồn lực chung vẫn còn trên nhóm được chỉ định nhiệm vụ và các thành viên nhóm nguồn lực được đặt tên không được chỉ định là một phần của vị trí.</span><span class="sxs-lookup"><span data-stu-id="333b1-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="333b1-120">Người quản lý dự án có thể gán công việc phù hợp với các nguồn lực được đặt tên.</span><span class="sxs-lookup"><span data-stu-id="333b1-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="333b1-121">Dạng xem **Hợp nhất** có thể hỗ trợ người quản lý dự án trong việc chia các đặt lịch cho nhiều nguồn lực cho phân công nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="333b1-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="333b1-122">Điều này không được thực hiện tự động bởi vì trong bất kỳ trường hợp nào phức tạp hơn ví dụ đơn giản ở trên, chẳng hạn như nơi bạn có một yêu cầu gồm nhiều nhiệm vụ hoặc ý định về cách thức người quản lý dự án muốn chỉ định, mà hệ thống cần tính đến.</span><span class="sxs-lookup"><span data-stu-id="333b1-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="333b1-123">Vì hệ thống không thể hiểu được ý định, nên các giả định có thể sẽ khác ý định và có thể xảy ra kết quả không chính xác hoặc không dự đoán được.</span><span class="sxs-lookup"><span data-stu-id="333b1-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="333b1-124">Kết quả dự đoán được đó là nguồn lực chung vẫn được gán cho đến khi ngời quản lý dự án cố ý tạo phân công với sự trợ giúp của dạng xem **Hợp nhất**.</span><span class="sxs-lookup"><span data-stu-id="333b1-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


