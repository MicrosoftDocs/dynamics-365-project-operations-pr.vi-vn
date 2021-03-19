---
title: Hiệu suất lập kế hoạch nguồn lực dự án
description: Chủ đề này cung cấp thông tin về cách cải thiện hiệu suất lập kế hoạch nguồn lực cho một số lượng lớn các dự án.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289035"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="356d1-103">Hiệu suất lập kế hoạch nguồn lực dự án</span><span class="sxs-lookup"><span data-stu-id="356d1-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="356d1-104">Các vấn đề về hiệu suất liên quan đến lập kế hoạch nguồn lực có thể xảy ra khi số lượng dự án lên đến hàng nghìn.</span><span class="sxs-lookup"><span data-stu-id="356d1-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="356d1-105">Để cải thiện hiệu suất lập kế hoạch nguồn lực, một tính năng có sẵn cho phép người dùng giảm thời gian khởi chạy biểu mẫu về tính sẵn sàng của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="356d1-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="356d1-106">Cụ thể, điều này loại bỏ quá trình đồng bộ hóa tổng hợp năng lực của nguồn lực và sử dụng bảng **ResProjectResource** để tăng tốc độ tra cứu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="356d1-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="356d1-107">Lưu ý rằng bảng **ResRollup** sẽ không còn được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="356d1-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="356d1-108">Nếu có đối tượng phụ thuộc trong quá trình đồng bộ hóa tổng hợp năng lực của nguồn lực hoặc bảng **ResProjectResource**, không sử dụng tính năng này.</span><span class="sxs-lookup"><span data-stu-id="356d1-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="356d1-109">Bật nâng cao hiệu suất lập kế hoạch nguồn lực</span><span class="sxs-lookup"><span data-stu-id="356d1-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="356d1-110">Để bật tính năng nâng cao hiệu suất lập kế hoạch nguồn lực, hãy hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="356d1-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="356d1-111">Đi đến **Quản lý tính năng** > **Tất cả** và trong danh sách tính năng, hãy định vị **Bật tính năng nâng cao hiệu suất lập kế hoạch nguồn lực dự án**.</span><span class="sxs-lookup"><span data-stu-id="356d1-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="356d1-112">Chọn **Bật ngay**.</span><span class="sxs-lookup"><span data-stu-id="356d1-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="356d1-113">Nếu bạn không thể tìm thấy tính năng trong danh sách, hãy chọn **Kiểm tra cập nhật** để làm mới danh sách.</span><span class="sxs-lookup"><span data-stu-id="356d1-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="356d1-114">Làm mới trình duyệt của bạn, sau đó đi đến **Quản lý dự án và kế toán** > **Định kỳ** > **Nguồn lực dự án** > **Đồng bộ hóa năng lực theo lịch nguồn lực trên tất cả công ty**.</span><span class="sxs-lookup"><span data-stu-id="356d1-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="356d1-115">Đặt **Xóa hồ sơ năng lực hiện có** thành **Có** để xóa dữ liệu trước đó.</span><span class="sxs-lookup"><span data-stu-id="356d1-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="356d1-116">Nếu bạn muốn tạo dữ liệu gia tăng, hãy đặt thành **Không**.</span><span class="sxs-lookup"><span data-stu-id="356d1-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="356d1-117">Trong trường **Mã kỳ**, chọn khoảng thời gian mà dữ liệu sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="356d1-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="356d1-118">Nếu bạn chọn một mã kỳ, thì không cần xác định ngày bắt đầu và ngày kết thúc.</span><span class="sxs-lookup"><span data-stu-id="356d1-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="356d1-119">Nếu bạn để trống trường **Mã kỳ**, hãy chọn ngày bắt đầu và ngày kết thúc cụ thể để tạo dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="356d1-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="356d1-120">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="356d1-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="356d1-121">Điều này sẽ phân phối dữ liệu chung tới bảng **ResCalendarCapacity** trên tất cả các công ty trong môi trường của bạn, vì vậy, công việc hàng loạt chỉ cần được chạy trong một pháp nhân.</span><span class="sxs-lookup"><span data-stu-id="356d1-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="356d1-122">Cần có dữ liệu trong công việc hàng loạt này để tính toán năng lực của nguồn lực thông qua lịch liên quan.</span><span class="sxs-lookup"><span data-stu-id="356d1-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="356d1-123">Đi đến **Quản lý dự án và kế toán** > **Định kỳ** > **Nguồn lực dự án** > **Xác định nguồn lực dự án trên tất cả công ty**, sau đó chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="356d1-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="356d1-124">Đây là tập lệnh nâng cấp dữ liệu cho dữ liệu chung trong các bảng **ResProjectResource**, **ResCalendarDateTimeRange** và **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="356d1-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="356d1-125">Giá trị cho trường **PSAPRojSchedRole.RootActivity** cũng được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="356d1-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="356d1-126">Nếu điều này không được chạy, bạn sẽ nhận được cảnh báo khi cố gắng thực hiện các hoạt động lập kế hoạch nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="356d1-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="356d1-127">Tắt tính năng nâng cao hiệu suất lập kế hoạch nguồn lực</span><span class="sxs-lookup"><span data-stu-id="356d1-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="356d1-128">Đi đến **Quản lý tính năng** > **Tất cả** và tìm kiếm **Bật tính năng nâng cao hiệu suất lập kế hoạch nguồn lực dự án**.</span><span class="sxs-lookup"><span data-stu-id="356d1-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="356d1-129">Chọn tính năng, sau đó chọn nút **Tắt**.</span><span class="sxs-lookup"><span data-stu-id="356d1-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="356d1-130">Làm mới trình duyệt của bạn.</span><span class="sxs-lookup"><span data-stu-id="356d1-130">Refresh your browser.</span></span>
4. <span data-ttu-id="356d1-131">Đi đến **Quản lý dự án và kế toán** > **Định kỳ** > **Đồng bộ hóa năng lực** > **Đồng bộ hóa tổng hợp năng lực của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="356d1-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="356d1-132">Trên trang **Đồng bộ hóa tổng hợp năng lực**, hãy đặt **Xóa hồ sơ năng lực hiện có** thành **Có** để xóa dữ liệu trước đó.</span><span class="sxs-lookup"><span data-stu-id="356d1-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="356d1-133">Nếu bạn muốn tạo dữ liệu gia tăng, hãy đặt thành **Không**.</span><span class="sxs-lookup"><span data-stu-id="356d1-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="356d1-134">Trong trường **Mã kỳ**, chọn khoảng thời gian mà dữ liệu sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="356d1-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="356d1-135">Nếu bạn chọn một mã kỳ, thì không cần xác định ngày bắt đầu và ngày kết thúc.</span><span class="sxs-lookup"><span data-stu-id="356d1-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="356d1-136">Nếu bạn để trống trường **Mã kỳ**, hãy chọn ngày bắt đầu và ngày kết thúc cụ thể để tạo dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="356d1-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="356d1-137">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="356d1-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="356d1-138">Điều này sẽ phân phối dữ liệu chung tới bảng **ResRollup** trên tất cả các công ty trong môi trường của bạn, vì vậy, công việc hàng loạt chỉ cần được chạy trong một pháp nhân.</span><span class="sxs-lookup"><span data-stu-id="356d1-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="356d1-139">Công việc hàng loạt này là cần thiết cho tất cả dạng xem **Tính sẵn sàng của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="356d1-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="356d1-140">Nếu công việc hàng loạt này không được chạy, dữ liệu **ResRollup** sẽ được tạo nhanh chóng, có thể mất thời gian.</span><span class="sxs-lookup"><span data-stu-id="356d1-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]