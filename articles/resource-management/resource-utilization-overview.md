---
title: Tổng quan về thời gian làm việc của nguồn lực
description: Chủ đề này cung cấp thông tin về cách sử dụng nguồn lực trong Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401402"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="9d29c-103">Tổng quan về thời gian làm việc của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="9d29c-103">Resource utilization overview</span></span>

<span data-ttu-id="9d29c-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="9d29c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9d29c-105">Nguồn lực có thể có thời gian làm việc tính phí mục tiêu.</span><span class="sxs-lookup"><span data-stu-id="9d29c-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="9d29c-106">Thời gian làm việc mục tiêu này được định nghĩa là thuộc tính trên vai trò mặc định của nguồn lực hoặc bộ trên bản ghi của nguồn lực riêng có thể đăng ký.</span><span class="sxs-lookup"><span data-stu-id="9d29c-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="9d29c-107">Phép tính thời gian làm việc dựa trên số giờ thực tế mà nguồn lực đã báo cáo bằng mục nhập thời gian được phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="9d29c-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="9d29c-108">Công thức sau dùng để tính toán thời gian làm việc:</span><span class="sxs-lookup"><span data-stu-id="9d29c-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="9d29c-109">Thời gian làm việc tính phí = Giờ thực tế tính phí ÷ Năng lực của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="9d29c-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="9d29c-110">Thời gian làm việc không tính phí = Thời gian thực tế có ID loại thanh toán = Không tính phí, Bổ sung hoặc Không có ÷ Năng lực của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="9d29c-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="9d29c-111">Nội bộ =Thời gian thực tế không có hợp đồng bán hàng ÷ Năng lực của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="9d29c-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="9d29c-112">Năng lực của nguồn lực = Giờ làm việc của nguồn lực – Thời gian ngoài văn phòng – Ngày không làm việc</span><span class="sxs-lookup"><span data-stu-id="9d29c-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="9d29c-113">Bạn có thể tìm thấy dạng xem **Thời gian làm việc của nguồn lực** trong ngăn **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="9d29c-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="9d29c-114">Mỗi ô trong lưới đại diện cho phần trăm thời gian làm việc tính phí của nguồn lực trong một khoảng thời gian, chẳng hạn như ngày, tuần hoặc tháng.</span><span class="sxs-lookup"><span data-stu-id="9d29c-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="9d29c-115">Công thức sau dùng để tô màu các ô:</span><span class="sxs-lookup"><span data-stu-id="9d29c-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="9d29c-116">**Màu lục**: Thời gian làm việc tính phí >= Thời gian làm việc mục tiêu của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="9d29c-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="9d29c-117">**Màu vàng**: Thời gian làm việc mục tiêu – 20 <= Thời gian làm việc tính phí < Thời gian làm việc mục tiêu</span><span class="sxs-lookup"><span data-stu-id="9d29c-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="9d29c-118">**Màu đỏ**: Thời gian làm việc tính phí < Thời gian làm việc mục tiêu – 20</span><span class="sxs-lookup"><span data-stu-id="9d29c-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="9d29c-119">Vì dạng xem **Thời gian làm việc của nguồn lực** dựa trên Bảng lịch trình, nên bạn có thể dùng các khả năng lọc của Bảng lịch trình để lọc các kết quả.</span><span class="sxs-lookup"><span data-stu-id="9d29c-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="9d29c-120">Lưới yêu cầu rằng bạn đặt thời gian làm việc mục tiêu trên vai trò hoặc nguồn lực riêng.</span><span class="sxs-lookup"><span data-stu-id="9d29c-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="9d29c-121">Để thực hiện bước thiết lập này, hãy chuyển đến **Nguồn lực** > **Vai trò nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="9d29c-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="9d29c-122">Ngoài ra, vai trò mặc định phải được gán cho từng nguồn lực có thể đăng ký.</span><span class="sxs-lookup"><span data-stu-id="9d29c-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="9d29c-123">Chuyển đến **Nguồn lực** > **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="9d29c-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="9d29c-124">Trên tab **Dịch vụ dự án**, hãy xác minh vai trò nguồn lực được xác định và trường **Là mặc định** được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="9d29c-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="9d29c-125">Bạn có thể thêm các vai trò bổ sung mà trường **Là mặc định** = **Không**.</span><span class="sxs-lookup"><span data-stu-id="9d29c-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="9d29c-126">Vai trò mà trường **Là mặc định** = **Có** dùng để đánh giá thời gian làm việc của nguồn lực so với mục tiêu cho vai trò đó.</span><span class="sxs-lookup"><span data-stu-id="9d29c-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="9d29c-127">Trên tab **Project Service**, bạn cũng có thể đặt thời gian làm việc mục tiêu riêng cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="9d29c-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="9d29c-128">Sau đó, phép tính thời gian làm việc dùng thời gian làm việc mục tiêu đó để đánh giá mục tiêu của nguồn lực thay vì mục tiêu của vai trò mặc định của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="9d29c-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="9d29c-129">Thời gian làm việc chỉ hiển thị cho nguồn lực chỉ khi nguồn lực đã phê duyệt, thời gian phải thanh toán trong khoảng thời gian hiển thị trong lưới.</span><span class="sxs-lookup"><span data-stu-id="9d29c-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>
