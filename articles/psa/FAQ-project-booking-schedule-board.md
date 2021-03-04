---
title: Tạo đăng ký dự án từ bảng Lịch trình
description: Chủ đề này cung cấp thông tin về cách tạo đặt chỗ dự án từ bảng lịch trình.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146554"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="e112c-103">Tạo đăng ký dự án từ bảng Lịch trình</span><span class="sxs-lookup"><span data-stu-id="e112c-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e112c-104">Bạn có thể đăng ký nguồn lực trên dự án bằng cả cách trực tiếp trên tab **Nhóm** của dự án hoặc bằng cách tạo yêu cầu nguồn lực từ phân công thành viên nhóm chung và sau đó thực hiện yêu cầu được tạo với thành viên nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="e112c-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="e112c-105">Bạn cũng có thể đăng ký nguồn lực trên dự án trực tiếp từ bảng Lịch trình.</span><span class="sxs-lookup"><span data-stu-id="e112c-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="e112c-106">Có ba cách để thực hiện việc này:</span><span class="sxs-lookup"><span data-stu-id="e112c-106">There are three ways to do this:</span></span>

- <span data-ttu-id="e112c-107">**Đăng ký từ một yêu cầu nguồn lực được tạo:** Bạn có thể tạo một yêu cầu nguồn lực sau khi tạo một tài nguyên chung và gán tác vụ trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="e112c-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="e112c-108">**Đặt lịch từ yêu cầu chính:** Các yêu cầu chính hiển thị trên bảng Lịch trình trên tab **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="e112c-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="e112c-109">**Đặt lịch từ một yêu cầu nguồn lực mới:** Bạn có thể tạo một yêu cầu nguồn lực từ đầu và liên kết với một dự án.</span><span class="sxs-lookup"><span data-stu-id="e112c-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="e112c-110">Trên bảng Lịch trình, yêu cầu nguồn lực hiển thị trên tab **Mở yêu cầu**.</span><span class="sxs-lookup"><span data-stu-id="e112c-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="e112c-111">Đăng ký từ một yêu cầu nguồn lực được tạo</span><span class="sxs-lookup"><span data-stu-id="e112c-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="e112c-112">Bạn có thể tạo nguồn lực chung và gán cho nguồn lực một hoặc nhiều nhiệm vụ ở trong dự án.</span><span class="sxs-lookup"><span data-stu-id="e112c-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="e112c-113">Sau đó, bạn có thể tạo yêu cầu nguồn lực từ thành viên nhóm chung.</span><span class="sxs-lookup"><span data-stu-id="e112c-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="e112c-114">Trên bảng Lịch trình, nguồn lực này sẽ hiển thị trên tab **Mở yêu cầu**. Bạn sẽ cần dùng các bộ lọc cột trên lưới nếu bạn có nhiều yêu cầu mở.</span><span class="sxs-lookup"><span data-stu-id="e112c-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="e112c-115">![Mở tab Yêu cầu trên bảng Lịch trình](media/FAQ-Project-Booking-Schedule-Board-1.png "Ảnh chụp màn hình khi đăng ký và bảng phân công")</span><span class="sxs-lookup"><span data-stu-id="e112c-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e112c-116">Chọn yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="e112c-116">Select the requirement.</span></span> <span data-ttu-id="e112c-117">Tab **Tìm khả năng đáp ứng** sẽ xuất hiện ở phía trên dòng được chọn.</span><span class="sxs-lookup"><span data-stu-id="e112c-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="e112c-118">Khi bạn chọn tab này, chế độ Trợ lý Lịch trình trên bảng Lịch trình sẽ mở ra và lọc các nguồn lực sẵn có đáp ứng được yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="e112c-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="e112c-119">Sau đó, bạn có thể đăng ký nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="e112c-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="e112c-120">Bạn cũng có thể kéo và thả dòng được chọn ở phía dưới bảng Lịch trình tới ô nguồn lực trong lưới ở trên.</span><span class="sxs-lookup"><span data-stu-id="e112c-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="e112c-121">Khi bạn thả ra, yêu cầu sẽ mở bảng điều khiển **Tạo đăng ký nguồn lực** ở bên phải.</span><span class="sxs-lookup"><span data-stu-id="e112c-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="e112c-122">Chọn **Đăng ký** để đăng ký nguồn lực trên nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="e112c-122">Selecting **Book** books the resource onto the project team.</span></span>

![Tạo bảng điều khiển Đăng ký Nguồn lực](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="e112c-124">Đăng ký từ Yêu cầu Chính</span><span class="sxs-lookup"><span data-stu-id="e112c-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="e112c-125">Tạo dự án tự động trong Project Service sẽ tự động tạo yêu cầu nguồn lực được gọi là Yêu cầu Chính.</span><span class="sxs-lookup"><span data-stu-id="e112c-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="e112c-126">Đây là một yêu cầu rỗng được dùng để đăng ký nhanh chóng nguồn lực bằng bảng Lịch trình mà không phải tạo yêu cầu hoặc tạo nguồn lực từ đầu.</span><span class="sxs-lookup"><span data-stu-id="e112c-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="e112c-127">Bởi vì yêu cầu này rỗng, bạn sẽ cần xác định ngày cũng như phương pháp phân bổ và số giờ nếu áp dụng.</span><span class="sxs-lookup"><span data-stu-id="e112c-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="e112c-128">Để đăng ký nguồn lực bằng Yêu cầu Chính, trên bảng Lịch trình, chọn tab **Dự án**. Bạn sẽ cần dùng bộ lọc cột trên cột **Dự án** nếu bạn có nhiều dự án.</span><span class="sxs-lookup"><span data-stu-id="e112c-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="e112c-129">![Bộ lọc cột trên bảng Lịch trình](media/FAQ-Project-Booking-Schedule-Board-2.png "Ảnh chụp màn hình khi đăng ký và bảng phân công")</span><span class="sxs-lookup"><span data-stu-id="e112c-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e112c-130">Chọn yêu cầu mà chỉ có tên dự án có cùng tên đó và có khoảng thời gian là không (0).</span><span class="sxs-lookup"><span data-stu-id="e112c-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="e112c-131">Chọn tab **Tìm sẵn có** hiện ở trên dòng.</span><span class="sxs-lookup"><span data-stu-id="e112c-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="e112c-132">Điều này khiến bảng Lịch trình trong chế độ Trợ lý Lịch trình và hiện các nguồn lực sẵn có mà có thể được đăng lý trên dự án.</span><span class="sxs-lookup"><span data-stu-id="e112c-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="e112c-133">Bởi vì **Yêu cầu Chính** là một yêu cầu rỗng có khoảng thời gian bằng không (0), bạn sẽ cần đặt khoảng thời gian trên bảng điều khiển **Tạo đăng ký nguồn lực** khi chọn và đăng ký nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="e112c-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="e112c-134">Bạn cũng có thể chọn **Yêu cầu Chính của Dự án** ở cuối bảng Lịch trình và kéo, thả yêu cầu vào nguồn lực để đăng ký.</span><span class="sxs-lookup"><span data-stu-id="e112c-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="e112c-135">Bởi vì **Yêu cầu Chính** là một yêu cầu rỗng có khoảng thời gian bằng không (0), bạn sẽ cần đặt khoảng thời gian trên bảng điều khiển **Tạo đăng ký nguồn lực** khi chọn và đăng ký nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="e112c-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="e112c-136">Khi bạn đăng ký nguồn lực qua **Yêu cầu Chính** trên bảng Lịch trình, bạn thêm nguồn lực vào nhóm dự án mà không cần phân công.</span><span class="sxs-lookup"><span data-stu-id="e112c-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="e112c-137">Đăng ký từ yêu cầu nguồn lực mới</span><span class="sxs-lookup"><span data-stu-id="e112c-137">Book from a new resource requirement</span></span>
<span data-ttu-id="e112c-138">Hoàn tất các bước sau để đặt lịch từ một yêu cầu nguồn lực mới.</span><span class="sxs-lookup"><span data-stu-id="e112c-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="e112c-139">Chuyển tới **Yêu cầu nguồn lực** và chọn **Mới** để tạo yêu cầu nguồn lực mới.</span><span class="sxs-lookup"><span data-stu-id="e112c-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="e112c-140">Trên tab **Dự án**, chọn một dự án liên kết yêu cầu dự án.</span><span class="sxs-lookup"><span data-stu-id="e112c-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="e112c-141">Trên bảng Lịch trình, yêu cầu mới này hiển thị là **Yêu cầu Mở** trên bảng lịch trình mà bạn có thể thực hiện.</span><span class="sxs-lookup"><span data-stu-id="e112c-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="e112c-142">Đăng ký nguồn lực để thêm nguồn lực vào nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="e112c-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="e112c-143">Bây giờ, nguồn lực đã được đăng ký, bạn phải gán nhiệm vụ theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="e112c-143">Now that the resource is booked, you must assign tasks manually.</span></span>

