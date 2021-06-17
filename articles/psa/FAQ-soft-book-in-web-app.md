---
title: Làm thế nào để tôi "đăng ký dự kiến" các nguồn lực trong phiên bản ứng dụng 2.x?
description: Bài viết này mô tả cách "đăng ký dự kiến" các thành viên nhóm dự án bằng Project Service.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 413783d2386cccd98cfe216a7c7300a5b7f771ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992945"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="cbc62-103">Làm thế nào để tôi "đăng ký dự kiến" nguồn lực trong ứng dụng web (ứng dụng Project Service phiên bản 2.x)?</span><span class="sxs-lookup"><span data-stu-id="cbc62-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="cbc62-104">Bạn có thể lên lịch trình dự kiến hoặc "đăng ký dự kiến" nguồn lực trên nhóm dự án để hiện nguồn lực bạn lên kế hoạch gán cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="cbc62-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="cbc62-105">Đăng ký dự kiến không sử dụng năng lực sẵn có của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="cbc62-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="cbc62-106">Các thành viên nhóm được đăng ký dự kiến không thể được gán vào nhiệm vụ dự án.</span><span class="sxs-lookup"><span data-stu-id="cbc62-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="cbc62-107">Chỉ có nguồn lực với tình trạng Đăng ký Xác nhận và Loại Cam kết Đã cam kết mới có thể được gán cho nhiệm vụ (giả sử các nguồn lực có đủ số giờ đăng ký xác nhận để thực hiện mức nỗ lực thực hiện nhiệm vụ).</span><span class="sxs-lookup"><span data-stu-id="cbc62-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="cbc62-108">Thành viên nhóm dự án được đăng ký dự kiến hiển thị trong lưới Thành viên Nhóm số giờ đăng ký dự kiến hiển thị trong cột Đăng ký Dự kiến.</span><span class="sxs-lookup"><span data-stu-id="cbc62-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="cbc62-109">Các thành viên này cũng có mặt trên bảng lịch trình.</span><span class="sxs-lookup"><span data-stu-id="cbc62-109">They also show up on the schedule board.</span></span> <span data-ttu-id="cbc62-110">Một lần nữa, các thành viên nhóm không cho thấy bất kỳ mức sử dụng năng lực nào vì đăng ký dự kiến không sử dụng năng lực sẵn có của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="cbc62-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="cbc62-111">Có ba cách để đăng ký dự kiến một thành viên nhóm vào một dự án với Project Service phiên bản 2.x.</span><span class="sxs-lookup"><span data-stu-id="cbc62-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="cbc62-112">Bạn có thể đăng ký dự kiến với bảng lịch trình, sử dụng tính năng Duy trì Đăng ký hoặc bằng cách tạo ra một nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="cbc62-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="cbc62-113">Những phương pháp này được mô tả dưới đây.</span><span class="sxs-lookup"><span data-stu-id="cbc62-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="cbc62-114">Đăng ký dự kiến với bảng lịch trình</span><span class="sxs-lookup"><span data-stu-id="cbc62-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="cbc62-115">Để đăng ký dự kiến với bảng lịch trình, hãy làm theo thủ tục này:</span><span class="sxs-lookup"><span data-stu-id="cbc62-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="cbc62-116">Mở bảng lịch trình.</span><span class="sxs-lookup"><span data-stu-id="cbc62-116">Open the schedule board.</span></span>
2. <span data-ttu-id="cbc62-117">Chọn tab Dự án nằm ở cuối bảng điều khiển Yêu cầu Đăng ký của bảng lịch trình.</span><span class="sxs-lookup"><span data-stu-id="cbc62-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="cbc62-118">Tìm dự án bạn muốn đăng ký dự kiến nguồn lực vào.</span><span class="sxs-lookup"><span data-stu-id="cbc62-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="cbc62-119">Nếu bạn có nhiều dự án, hãy nhấp vào tiêu đề của cột Dự án và sau đó sử dụng các bộ lọc để tìm kiếm dự án của bạn.</span><span class="sxs-lookup"><span data-stu-id="cbc62-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="cbc62-120">Nhấp vào dự án, sau đó kéo và thả nó trên lưới thời gian của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="cbc62-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="cbc62-121">Thao tác này sẽ mở bảng điều khiển Tạo Đăng ký Nguồn lực ở bên phải.</span><span class="sxs-lookup"><span data-stu-id="cbc62-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="cbc62-122">Điều chỉnh ngày bắt đầu và kết thúc, chọn Trạng thái Đăng ký là Dự kiến và đặt giờ.</span><span class="sxs-lookup"><span data-stu-id="cbc62-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="cbc62-123">Bấm Đăng ký.</span><span class="sxs-lookup"><span data-stu-id="cbc62-123">Click Book.</span></span>
7. <span data-ttu-id="cbc62-124">Quay lại dự án, nguồn lực sẽ hiển thị như là một thành viên nhóm với số giờ đăng ký dự kiến trong cột Đăng ký Dự kiến.</span><span class="sxs-lookup"><span data-stu-id="cbc62-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="cbc62-125">Lưu ý rằng bạn không thể gán các nguồn lực vào các tác vụ trên cấu trúc phân tích công việc (WBS) vì nguồn lực phải được đăng ký xác nhận trong nhóm để được gán.</span><span class="sxs-lookup"><span data-stu-id="cbc62-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="cbc62-126">Đăng ký dự kiến bằng cách sử dụng tính năng Duy trì Đăng ký</span><span class="sxs-lookup"><span data-stu-id="cbc62-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="cbc62-127">Để đăng ký dự kiến với tính năng Duy trì Đăng ký, hãy làm theo thủ tục này:</span><span class="sxs-lookup"><span data-stu-id="cbc62-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="cbc62-128">Từ lưới thành viên nhóm, nhấp vào Mới.</span><span class="sxs-lookup"><span data-stu-id="cbc62-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="cbc62-129">Chọn ngày bắt đầu/kết thúc, vai trò, nguồn lực có thể đăng ký được.</span><span class="sxs-lookup"><span data-stu-id="cbc62-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="cbc62-130">Chọn một phương pháp phân bổ khác Không có:</span><span class="sxs-lookup"><span data-stu-id="cbc62-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="cbc62-131">Năng lực đầy đủ</span><span class="sxs-lookup"><span data-stu-id="cbc62-131">Full Capacity</span></span>
- <span data-ttu-id="cbc62-132">Năng lực tỉ lệ phần trăm</span><span class="sxs-lookup"><span data-stu-id="cbc62-132">Percentage Capacity</span></span>
- <span data-ttu-id="cbc62-133">Theo Giờ Phân phối Đồng đều</span><span class="sxs-lookup"><span data-stu-id="cbc62-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="cbc62-134">Theo Giờ Phân phối lượng công việc nặng lúc ban đầu</span><span class="sxs-lookup"><span data-stu-id="cbc62-134">By Hours Front Load</span></span>
4. <span data-ttu-id="cbc62-135">Bấm vào Lưu.</span><span class="sxs-lookup"><span data-stu-id="cbc62-135">Click Save.</span></span> <span data-ttu-id="cbc62-136">Bạn sẽ thấy nguồn lực trên lưới nhóm và số giờ của chúng cho thấy là Xác nhận.</span><span class="sxs-lookup"><span data-stu-id="cbc62-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="cbc62-137">Duy trì trạng thái đăng ký của nguồn lực bằng cách nhấp vào Duy trì Đăng ký.</span><span class="sxs-lookup"><span data-stu-id="cbc62-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="cbc62-138">Khi bảng lịch trình mở ra, hãy mở rộng nguồn lực để hiện các đăng ký.</span><span class="sxs-lookup"><span data-stu-id="cbc62-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="cbc62-139">Bạn sẽ thấy đăng ký cho thấy là Xác nhận.</span><span class="sxs-lookup"><span data-stu-id="cbc62-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="cbc62-140">Nhấp chuột phải đăng ký, dưới Thay đổi Trạng thái, chọn Đăng ký Dự kiến và sau đó là Dự kiến.</span><span class="sxs-lookup"><span data-stu-id="cbc62-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="cbc62-141">Trạng thái đăng ký bây giờ là Dự kiến.</span><span class="sxs-lookup"><span data-stu-id="cbc62-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="cbc62-142">Sau khi đóng bảng lịch trình, bạn sẽ thấy số giờ dành cho nguồn lực đã thay đổi từ Xác nhận thành Dự kiến trên lưới thành viên nhóm.</span><span class="sxs-lookup"><span data-stu-id="cbc62-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="cbc62-143">Lưu ý rằng nếu bạn đăng ký xác nhận nguồn lực trên nhóm và sau đó gán chúng nhiệm vụ trên cấu trúc phân tích công việc, khi bạn sử dụng duy trì đăng ký để đổi trạng thái từ Xác nhận sang Dự kiến, thao tác này sẽ loại bỏ nhiệm vụ cho nguồn lực vì chỉ có nguồn lực được đăng ký xác nhận mới có thể được gán cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="cbc62-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="cbc62-144">Đăng ký dự kiến bằng cách tạo ra một nguồn lực chung</span><span class="sxs-lookup"><span data-stu-id="cbc62-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="cbc62-145">Bạn có thể đăng ký dự kiến bằng cách tạo ra một thành viên nhóm nguồn lực chung, hoàn thành với bảng lịch trình hoặc Đề nghị Nguồn lực và thay đổi loại trong quá trình đăng ký.</span><span class="sxs-lookup"><span data-stu-id="cbc62-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="cbc62-146">Để thực hiện điều này, hãy làm theo thủ tục sau:</span><span class="sxs-lookup"><span data-stu-id="cbc62-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="cbc62-147">Trên WBS của dự án, hãy gán vai trò cho các nhiệm vụ bạn muốn tạo các thành viên nhóm chung cho.</span><span class="sxs-lookup"><span data-stu-id="cbc62-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="cbc62-148">Nhấp vào Tạo Thành viên Dự án/</span><span class="sxs-lookup"><span data-stu-id="cbc62-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="cbc62-149">Trên lưới thành viên nhóm của dự án. chọn nguồn lực chung và nhấp vào Đăng ký.</span><span class="sxs-lookup"><span data-stu-id="cbc62-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="cbc62-150">Trên bảng lịch trình, chọn nguồn lực bạn muốn đăng ký.</span><span class="sxs-lookup"><span data-stu-id="cbc62-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="cbc62-151">Trên bảng điều khiển Tạo Đăng ký Nguồn lực của bảng lịch trình, thay đổi Trạng thái Đăng ký từ Xác nhận sang Dự kiến.</span><span class="sxs-lookup"><span data-stu-id="cbc62-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="cbc62-152">Nhấp vào Đăng ký hay Đăng ký và Thoát.</span><span class="sxs-lookup"><span data-stu-id="cbc62-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="cbc62-153">Sau khi đóng bảng lịch trình, bạn sẽ thấy nguồn lực được chọn được thêm vào nhóm số giờ Đăng ký dự kiến cũng như số giờ được gán.</span><span class="sxs-lookup"><span data-stu-id="cbc62-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="cbc62-154">Bạn cũng sẽ thấy nguồn lực chung vẫn còn trong nhóm như là một chỉ báo cho thấy các nhiệm vụ được gán cho một thành viên nhóm được đăng ký dự kiến.</span><span class="sxs-lookup"><span data-stu-id="cbc62-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="cbc62-155">Khi bạn sẵn sàng đổi nguồn lực thành viên nhóm được đăng ký dự kiến sang thành viên nhóm được đăng ký xác nhận để gán vào nhiệm vụ, thực hiện như sau:</span><span class="sxs-lookup"><span data-stu-id="cbc62-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="cbc62-156">Chọn nguồn lực đó và nhấp vào Duy trì Đăng ký.</span><span class="sxs-lookup"><span data-stu-id="cbc62-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="cbc62-157">Khi bảng lịch trình mở ra, hãy mở rộng nguồn lực để hiện các đăng ký.</span><span class="sxs-lookup"><span data-stu-id="cbc62-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="cbc62-158">Bạn sẽ thấy đăng ký được đánh dấu là Dự kiến.</span><span class="sxs-lookup"><span data-stu-id="cbc62-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="cbc62-159">Nhấp chuột phải vào đăng ký, dưới Thay đổi Trạng thái, chọn Đăng ký Xác nhận và sau đó là Xác nhận.</span><span class="sxs-lookup"><span data-stu-id="cbc62-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="cbc62-160">Trạng thái đăng ký bây giờ là Xác nhận.</span><span class="sxs-lookup"><span data-stu-id="cbc62-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="cbc62-161">Sau khi đóng bảng lịch trình, bạn sẽ thấy số giờ dành cho nguồn lực đã thay đổi từ Dự kiến thành Xác nhận trên lưới thành viên nhóm.</span><span class="sxs-lookup"><span data-stu-id="cbc62-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="cbc62-162">Bây giờ bạn có thể gán tài nguyên cho nhiệm vụ (miễn là có sự liên kết giữa số giờ đăng ký xác nhận và số giờ nỗ lực của nhiệm vụ).</span><span class="sxs-lookup"><span data-stu-id="cbc62-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="cbc62-163">Lưu ý rằng nếu bạn làm theo các bước hoàn thành nguồn lực chung trong mục #3 ở trên, khi bạn thay đổi trạng thái của nguồn lực được đăng ký dự kiến sang xác nhận, thành viên nhóm chung sẽ bị loại khỏi nhóm.</span><span class="sxs-lookup"><span data-stu-id="cbc62-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]