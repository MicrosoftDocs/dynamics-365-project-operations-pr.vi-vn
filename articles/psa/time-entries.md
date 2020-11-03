---
title: Tạo mục nhập thời gian
description: Chủ đề này cung cấp thông tin về cách tạo mục nhập thời gian.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087199"
---
# <a name="create-time-entries"></a><span data-ttu-id="11ef8-103">Tạo mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="11ef8-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="11ef8-104">Trong các phiên bản Dynamics 365 Project Service Automation trước, mục nhập thời gian đã được nhập trên cơ sở hàng tuần.</span><span class="sxs-lookup"><span data-stu-id="11ef8-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="11ef8-105">Trong phiên bản 3 của Project Service Automation, mục nhập thời gian được nhập trên cơ sở hàng ngày.</span><span class="sxs-lookup"><span data-stu-id="11ef8-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="11ef8-106">Tuy nhiên, sau khi một vài mục nhập thời gian đã được tạo, bạn có thể tạo hoặc sao chép hàng loạt các mục nhập đó.</span><span class="sxs-lookup"><span data-stu-id="11ef8-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="11ef8-107">Tạo mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="11ef8-107">Create a time entry</span></span>

<span data-ttu-id="11ef8-108">Làm theo các bước sau để tạo mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="11ef8-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="11ef8-109">Trên trang **Mục nhập thời gian** , hãy chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="11ef8-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="11ef8-110">Trong hộp thoại **Tạo nhanh: Mục thời gian** , hãy nhập khoảng thời gian của mục nhập thời gian theo phút, giờ hoặc ngày.</span><span class="sxs-lookup"><span data-stu-id="11ef8-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="11ef8-111">Phải nhập khoảng thời gian theo định dạng sau: *x* phút, *x* giờ hoặc *x* ngày.</span><span class="sxs-lookup"><span data-stu-id="11ef8-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="11ef8-112">Cũng có thể nhập giờ và ngày dưới dạng giá trị thập phân, chẳng hạn như *x.x* giờ hoặc *x.x* ngày.</span><span class="sxs-lookup"><span data-stu-id="11ef8-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="11ef8-113">Chọn loại mục nhập thời gian và dự án mà bạn đang nhập vào mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="11ef8-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="11ef8-114">Trong trường **Nhiệm vụ dự án** , hãy tìm nhiệm vụ cho mục nhập thời gian này.</span><span class="sxs-lookup"><span data-stu-id="11ef8-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="11ef8-115">Nếu bạn đang tạo mục nhập thời gian cho một nhiệm vụ không được gán cho người dùng, thì trong trường **nhiệm vụ dự án** , hãy chọn nút **Tìm kiếm** , chọn **Thay đổi dạng xem** rồi chọn **Tất cả nhiệm vụ dự án đang hoạt động** để liệt kê tất cả nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="11ef8-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View** , and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="11ef8-116">Nhập mô tả, nếu mô tả là bắt buộc, sau đó chọn **Lưu và Đóng**.</span><span class="sxs-lookup"><span data-stu-id="11ef8-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="11ef8-117">Sau khi mục nhập thời gian được tạo và lưu, bạn có thể chỉnh sửa trong lưới mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="11ef8-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="11ef8-118">Lưới mục nhập thời gian hỗ trợ 2 định dạng:</span><span class="sxs-lookup"><span data-stu-id="11ef8-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="11ef8-119">Bạn có thể nhập các mục nhập thời gian theo định dạng **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="11ef8-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="11ef8-120">Sau đó, định dạng này được chuyển đổi thành giờ và phân số.</span><span class="sxs-lookup"><span data-stu-id="11ef8-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="11ef8-121">Bạn có thể nhập trực tiếp số giờ và phân số.</span><span class="sxs-lookup"><span data-stu-id="11ef8-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="11ef8-122">Lưu ý rằng phân số của một giờ không phải là phút.</span><span class="sxs-lookup"><span data-stu-id="11ef8-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="11ef8-123">Do đó, 1,5 giờ đại diện cho 1 giờ và 30 phút.</span><span class="sxs-lookup"><span data-stu-id="11ef8-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="11ef8-124">Quy tắc này áp dụng cho cả phân số của một ngày.</span><span class="sxs-lookup"><span data-stu-id="11ef8-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="11ef8-125">Một ngày là 24 giờ và 0,5 ngày đại diện cho 12 giờ.</span><span class="sxs-lookup"><span data-stu-id="11ef8-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="11ef8-126">Tạo hàng loạt mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="11ef8-126">Bulk create time entries</span></span>

<span data-ttu-id="11ef8-127">Sau khi một vài mục nhập thời gian được tạo, bạn có thể sao chép chúng để tạo thêm hàng loạt các mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="11ef8-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="11ef8-128">Trên trang **Mục nhập thời gian** , hãy chọn **Sao chép tuần**.</span><span class="sxs-lookup"><span data-stu-id="11ef8-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="11ef8-129">Trong nhóm trường **Từ khoảng thời gian** , trong các trường **Ngày bắt đầu** và **Ngày kết thúc** , hãy xác định phạm vi ngày để sao chép mục nhập thời gian từ đó.</span><span class="sxs-lookup"><span data-stu-id="11ef8-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="11ef8-130">Trong trường nhóm **Tới khoảng thời gian** , trong trường **Ngày bắt đầu** , hãy chỉ định ngày để tạo mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="11ef8-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="11ef8-131">Chọn **Sao chép** để tạo bản sao của mục nhập thời gian tương ứng với ngày trong tuần được chỉ định trong nhóm trường **Tới khoảng thời gian**.</span><span class="sxs-lookup"><span data-stu-id="11ef8-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="11ef8-132">Ví dụ: mục nhập thời gian cho Thứ hai tuần cuối cùng được sao chép vào Thứ hai trong tuần được chỉ định trong nhóm trường  **Tới khoảng thời gian**.</span><span class="sxs-lookup"><span data-stu-id="11ef8-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="11ef8-133">Nhập dữ liệu cho các mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="11ef8-133">Import data for time entries</span></span>

<span data-ttu-id="11ef8-134">Bạn có thể nhập dữ liệu từ các mục đặt trước và chỉ định.</span><span class="sxs-lookup"><span data-stu-id="11ef8-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="11ef8-135">Khi bạn nhập dữ liệu, bạn có thể chỉ định phạm vi ngày của mục đặt trước sẽ nhập, sau đó chọn rõ ràng các mục đặt trước sẽ được tạo dưới dạng mục nhập thời gian **Nháp**.</span><span class="sxs-lookup"><span data-stu-id="11ef8-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="11ef8-136">Nhóm theo, sắp xếp, tìm kiếm và lọc khả năng</span><span class="sxs-lookup"><span data-stu-id="11ef8-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="11ef8-137">Bạn có thể nhóm và lọc các mục nhập thời gian theo các thứ nguyên được chỉ định trong các cột.</span><span class="sxs-lookup"><span data-stu-id="11ef8-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="11ef8-138">Trong trường **Nhóm theo** , hãy chọn thông số cần sử dụng để lọc các mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="11ef8-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="11ef8-139">Bạn cũng có thể sắp xếp các bản ghi mục nhập thời gian theo thứ tự tăng dần hoặc giảm dần bằng cách sử dụng mũi tên sắp xếp trên các tiêu đề cột.</span><span class="sxs-lookup"><span data-stu-id="11ef8-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="11ef8-140">Ngoài ra, bạn có thể hiển thị hoặc ẩn các mục nhập bằng cách chọn nút **Lọc** trên tiêu đề cột, rồi sau đó, trong hộp **Tìm kiếm** , nhập văn bản sẽ được sử dụng để tìm kiếm mục nhập thời gian theo tên dự án, nhiệm vụ dự án, mục nhập thời gian hoặc nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="11ef8-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
