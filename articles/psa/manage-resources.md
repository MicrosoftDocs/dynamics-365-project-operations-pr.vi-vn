---
title: Quản lý nguồn lực
description: Chủ đề này cung cấp thông tin về cách bạn có thể quản lý nguồn lực.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132359"
---
# <a name="manage-resources"></a><span data-ttu-id="b1666-103">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b1666-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b1666-104">Dynamics 365 Project Service Automation bao gồm một bảng thông tin cho người quản lý nguồn lực cung cấp tổng quan trực quan về nhu cầu nguồn lực và thời gian làm việc trong toàn tổ chức.</span><span class="sxs-lookup"><span data-stu-id="b1666-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="b1666-105">Bạn có thể dùng biểu đồ trên bảng thông tin này để hình dung thông tin sau:</span><span class="sxs-lookup"><span data-stu-id="b1666-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="b1666-106">**Nhu cầu nguồn lực** – Biểu đồ **Yêu cầu nguồn lực hiện hoạt** cho biết các nguồn lực đã được gửi.</span><span class="sxs-lookup"><span data-stu-id="b1666-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="b1666-107">Các nguồn lực được tổng hợp theo vai trò hoặc dự án.</span><span class="sxs-lookup"><span data-stu-id="b1666-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="b1666-108">**Nhu cầu nguồn lực chưa được gửi** – Biểu đồ **Nhu cầu nguồn lực chưa được gán** cho biết tất cả yêu cầu nguồn lực chưa được gửi.</span><span class="sxs-lookup"><span data-stu-id="b1666-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="b1666-109">Biểu đồ này giúp người quản lý nguồn lực xem nhu cầu chưa chắc chắn và có thể được gửi thông qua yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="b1666-110">**Thời gian làm việc tính phí cho tuần qua** – Biểu đồ **Thời gian làm việc theo vai trò** hiển thị tỷ lệ thời gian làm việc tính phí thực tế của tổ chức theo vai trò so với thời gian làm việc tính phí mục tiêu của tổ chức theo vai trò.</span><span class="sxs-lookup"><span data-stu-id="b1666-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1666-111">Để chia sẻ biểu đồ **Thời gian làm việc theo vai trò**, hãy tạo một công việc chạy quy trình làm việc UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="b1666-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="b1666-112">Công việc định kỳ này chạy 7 ngày 1 lần để tính thời gian làm việc tính phí cho 7 ngày trước đó.</span><span class="sxs-lookup"><span data-stu-id="b1666-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="b1666-113">Kết quả được tổng hợp theo vai trò.</span><span class="sxs-lookup"><span data-stu-id="b1666-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="b1666-114">Quản lý thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="b1666-114">Manage project team members</span></span>

<span data-ttu-id="b1666-115">Người quản lý dự án có thể dùng bảng thông tin cho người quản lý dự án để quản lý nguồn lực trên dự án.</span><span class="sxs-lookup"><span data-stu-id="b1666-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="b1666-116">Ví dụ: họ có thể thêm trực tiếp thành viên nhóm vào một dự án và đặt thành viên nhóm hoàn thành các yêu cầu nguồn lực được nguồn lực chung ghi lại.</span><span class="sxs-lookup"><span data-stu-id="b1666-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="b1666-117">Thêm trực tiếp thành viên nhóm vào một dự án</span><span class="sxs-lookup"><span data-stu-id="b1666-117">Add a team member directly to a project</span></span>

<span data-ttu-id="b1666-118">Để thêm trực tiếp một thành viên nhóm vào dự án, trên trang **Dự án**, trên tab **Nhóm**, hãy chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="b1666-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="b1666-119">Hộp thoại **Tạo nhanh: Thành viên nhóm dự án** xuất hiện.</span><span class="sxs-lookup"><span data-stu-id="b1666-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="b1666-120">Trong hộp thoại này, bạn có thể thực hiện các tác vụ sau:</span><span class="sxs-lookup"><span data-stu-id="b1666-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="b1666-121">**Đặt một nguồn lực có tên** – Trong trường **Nguồn lực có thể đăng ký**, hãy chọn tên nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="b1666-122">Sau đó, chọn vai trò, thiết lập khoảng thời gian rồi chọn một phương pháp phân bổ.</span><span class="sxs-lookup"><span data-stu-id="b1666-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="b1666-123">Nguồn lực có tên mà bạn đã chọn được thêm vào dự án bằng phương pháp phân bổ đã chọn và lịch nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="b1666-124">**Thêm nguồn lực chung** – Để trống trường **Tài nguyên có thể đăng ký**, sau đó chọn vai trò, chọn khoảng thời gian rồi chọn phương pháp phân bổ ưa thích.</span><span class="sxs-lookup"><span data-stu-id="b1666-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="b1666-125">Nguồn lực chung được thêm vào nhóm ở dạng chỗ dành sẵn để giữ mẫu nhu cầu dùng để đặt nguồn lực có tên trong nhóm.</span><span class="sxs-lookup"><span data-stu-id="b1666-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="b1666-126">Yêu cầu được thực hiện theo lịch dự án.</span><span class="sxs-lookup"><span data-stu-id="b1666-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="b1666-127">**Thêm nguồn lực có tên vào nhóm mà không dùng năng lực của nguồn lực** – Trong trường **Nguồn lực có thể đăng ký**, hãy chọn một nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="b1666-128">Sau đó, chọn khoảng thời gian rồi chọn **Không** làm phương pháp phân bổ.</span><span class="sxs-lookup"><span data-stu-id="b1666-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="b1666-129">Nguồn lực được thêm vào nhóm nhưng năng lực của nguồn lực không bị hao tốn khi đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="b1666-130">Đăng ký một thành viên nhóm để thực hiện các yêu cầu nguồn lực cho nguồn lực chung</span><span class="sxs-lookup"><span data-stu-id="b1666-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="b1666-131">Trong PSA, bạn có thể đăng ký một nguồn lực chung trên nhóm dự án và có thể chỉ rõ vai trò, năng lực cần thiết và cách năng lực được phân bổ.</span><span class="sxs-lookup"><span data-stu-id="b1666-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="b1666-132">Trên yêu cầu nguồn lực, bạn có thể chỉ định các thuộc tính liên kết với nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="b1666-133">Các thuộc tính này bao gồm các kỹ năng cần thiết, đơn vị tổ chức ưa thích và nguồn lực ưa thích.</span><span class="sxs-lookup"><span data-stu-id="b1666-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="b1666-134">Hãy làm theo các bước sau để chỉ định kỹ năng cần thiết trên nguồn lực chung cho nhà phát triển.</span><span class="sxs-lookup"><span data-stu-id="b1666-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="b1666-135">Trên trang **Dự án**, trên tab **Nhóm**, hãy chọn **Mới** để đăng ký nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Nguồn lực chung đã đăng ký trong nhóm](media/Resource-Management-image9.png)

2. <span data-ttu-id="b1666-137">Trong dạng xem **Tất cả thành viên nhóm**, trong cột **Yêu cầu nguồn lực**, hãy chọn liên kết để thêm kỹ năng cần thiết cho nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Liên kết yêu cầu](media/Resource-Management-image10.png)

3. <span data-ttu-id="b1666-139">Trên trang **Yêu cầu nguồn lực** xuất hiện, trong lưới **Kỹ năng**, hãy chọn dấu chấm lửng (**...**), sau đó chọn **Thêm đặc điểm yêu cầu mới** để thêm các kỹ năng cần thiết cho nhà phát triển của bạn.</span><span class="sxs-lookup"><span data-stu-id="b1666-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Lệnh Thêm đặc điểm yêu cầu mới](media/Resource-Management-image11.png)

4. <span data-ttu-id="b1666-141">Trong hộp thoại **Tạo nhanh: Đặc điểm yêu cầu** xuất hiện, trong trường **Đặc điểm**, chọn kỹ năng cần thiết.</span><span class="sxs-lookup"><span data-stu-id="b1666-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="b1666-142">Sau đó, trong trường **Giá trị xếp hạng**, hãy chọn mức độ thành thạo cho kỹ năng đó.</span><span class="sxs-lookup"><span data-stu-id="b1666-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="b1666-143">Cuối cùng, trong trường **Yêu cầu nguồn lực**, hãy đặt yêu cầu thành nguồn lực nguồn từ đơn vị tổ chức hoặc thậm chí là nguồn lực có tên.</span><span class="sxs-lookup"><span data-stu-id="b1666-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="b1666-144">Sau khi hoàn tất, hãy chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b1666-144">When you've finished, select **Save**.</span></span>

    ![Hộp thoại Tạo nhanh: Đặc điểm yêu cầu](media/Resource-Management-image12.png)

5. <span data-ttu-id="b1666-146">Trên trang **Yêu cầu nguồn lực**, hãy chọn **Đăng ký** để thực hiện yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Nút Đăng ký trên trang Yêu cầu nguồn lực](media/Resource-Management-image13.png)

    <span data-ttu-id="b1666-148">Bạn cũng có thể chọn nguồn lực chung trong lưới **Tất cả thành viên nhóm** rồi chọn **Đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="b1666-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Nút Đăng ký dưới lưới Tất cả thành viên nhóm](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="b1666-150">Trong ví dụ này, có 40 giờ yêu cầu nhưng không có giờ đã đăng ký thực tế vì nguồn lực chung không có đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="b1666-151">Ngoài ra, không có giờ được gán, vì nguồn lực chung được thêm trực tiếp vào nhóm.</span><span class="sxs-lookup"><span data-stu-id="b1666-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="b1666-152">Nguồn lực không được thêm bằng cách phân công nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="b1666-153">Trên trang **Trợ lý lập lịch biểu**, bạn có thể lọc các nguồn lực có sẵn theo yêu cầu được chỉ định trên yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="b1666-154">Nguồn lực được sắp xếp theo các tham số sắp xếp đã chỉ định trên Bảng lịch trình.</span><span class="sxs-lookup"><span data-stu-id="b1666-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Trang Trợ lý lập lịch biểu](media/Resource-Management-image15.png)

    <span data-ttu-id="b1666-156">Dưới đây là một số bộ lọc thường dùng:</span><span class="sxs-lookup"><span data-stu-id="b1666-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="b1666-157">**Đặc điểm cùng với xếp hạng** – Lọc theo kỹ năng, chứng nhận và các năng lực khác của nguồn lực, ngoài xếp hạng mức độ thành thạo.</span><span class="sxs-lookup"><span data-stu-id="b1666-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="b1666-158">**Vai trò** – Lọc theo các vai trò mặc định được gán cho các nguồn lực có thể đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="b1666-159">**Đơn vị tổ chức** – Lọc nguồn lực có thể đăng ký theo đơn vị tổ chức mà các nguồn lực này được phân công đến.</span><span class="sxs-lookup"><span data-stu-id="b1666-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="b1666-160">Nếu không hài lòng với kết quả tìm kiếm yêu cầu ban đầu, bạn có thể thay đổi tiêu chí lọc.</span><span class="sxs-lookup"><span data-stu-id="b1666-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="b1666-161">Mở rộng ngăn **Dạng xem lọc** ở bên trái, sau đó chọn **Tìm kiếm** để tìm các nguồn lực bổ sung.</span><span class="sxs-lookup"><span data-stu-id="b1666-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Ngăn Dạng xem lọc](media/Resource-Management-image16.png)

7. <span data-ttu-id="b1666-163">Để thay đổi cách kết quả được sắp xếp, hãy chọn **Sắp xếp**.</span><span class="sxs-lookup"><span data-stu-id="b1666-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Lệnh sắp xếp](media/Resource-Management-image17.png)

8. <span data-ttu-id="b1666-165">Chọn nguồn lực theo nhu cầu được chỉ rõ trên yêu cầu, như đã nêu ở phần đầu lưới.</span><span class="sxs-lookup"><span data-stu-id="b1666-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="b1666-166">Bạn có thể xóa lựa chọn các ô trong lưới và để năng lực của nguồn lực đó ở trạng thái mở.</span><span class="sxs-lookup"><span data-stu-id="b1666-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="b1666-167">Chỉ có thể chọn từng nguồn lực một khi đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="b1666-168">Chọn **Đăng ký** để đăng ký nguồn lực đã chọn và để Bảng lịch trình ở trạng thái mở để bạn có thể chọn thêm nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="b1666-169">Ngoài ra, hãy chọn **Đăng ký và thoát** để đăng ký nguồn lực đã chọn và đóng Bảng lịch trình.</span><span class="sxs-lookup"><span data-stu-id="b1666-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Nguồn lực cần đăng ký](media/Resource-Management-image19.png)

    <span data-ttu-id="b1666-171">Bạn nhận được thông báo về giờ đã đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="b1666-172">Các chỉ số nhu cầu cho thấy lượng yêu cầu đăng ký được thỏa mãn và lượng còn lại.</span><span class="sxs-lookup"><span data-stu-id="b1666-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="b1666-173">Bạn cũng có thể xem lượng tiêu thụ của năng lực của nguồn lực đã chọn.</span><span class="sxs-lookup"><span data-stu-id="b1666-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="b1666-174">Chọn **Bung rộng** để xem thêm thông tin chi tiết về đăng ký nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="b1666-175">Quay lại dạng xem **Tất cả thành viên**.</span><span class="sxs-lookup"><span data-stu-id="b1666-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="b1666-176">Trong lưới, thông báo rằng nguồn lực chung đã được thay thế bằng nguồn lực có tên và 40 giờ được liệt kê là đã đăng ký cho nguồn lực đó.</span><span class="sxs-lookup"><span data-stu-id="b1666-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Lưới Tất cả thành viên nhóm đã cập nhật](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="b1666-178">Không có giờ đã phân công nào hiển thị vì nguồn lực được đăng ký trực tiếp trên nhóm.</span><span class="sxs-lookup"><span data-stu-id="b1666-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="b1666-179">Các nguồn lực không được đăng ký bằng phân công nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="b1666-180">Phân công nhiệm vụ cho nguồn lực chung và tạo yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b1666-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="b1666-181">Trong PSA, bạn có thể tạo các nhiệm vụ, sau đó phân công nguồn lực chung cho các nhiệm vụ đó.</span><span class="sxs-lookup"><span data-stu-id="b1666-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="b1666-182">Bằng cách này, nhu cầu nguồn lực có thể được chỗ dành sẵn đại diện khi bạn ước tính số tài chính và lịch trình của mình.</span><span class="sxs-lookup"><span data-stu-id="b1666-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="b1666-183">Sau đó, bạn có thể tạo yêu cầu nguồn lực cho nguồn lực chung và thực hiện các yêu cầu đó.</span><span class="sxs-lookup"><span data-stu-id="b1666-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="b1666-184">Trên trang **Dự án**, trên tab **Lịch trình**, hãy chọn **Thêm** để tạo nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Nhiệm vụ mới được tạo](media/Resource-Management-image21.png)

2. <span data-ttu-id="b1666-186">Trong trường **Nguồn lực**, hãy chọn biểu tượng **Bộ chọn nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="b1666-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="b1666-187">Bộ chọn nguồn lực xuất hiện và hiển thị thành viên nhóm hiện tại cho dự án.</span><span class="sxs-lookup"><span data-stu-id="b1666-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Bộ chọn nguồn lực](media/Resource-Management-image22.png)

3. <span data-ttu-id="b1666-189">Nhập tên của nguồn lực chung mới rồi chọn **Tạo**.</span><span class="sxs-lookup"><span data-stu-id="b1666-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Tên của nguồn lực chung mới đã tạo](media/Resource-Management-image23.png)

4. <span data-ttu-id="b1666-191">Trong hộp thoại **Tạo nhanh: Thành viên nhóm dự án** xuất hiện, trong trường **Vai trò**, hãy chọn vai trò cho nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="b1666-192">Trong trường **Đơn vị nguồn lực**, hãy chọn đơn vị tổ chức cho nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="b1666-193">Tiếp đó, chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b1666-193">Then select **Save**.</span></span>

    ![Hộp thoại Tạo nhanh: Thành viên nhóm dự án](media/Resource-Management-image24.png)

    <span data-ttu-id="b1666-195">Thành viên nhóm chung hiện được phân công cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-195">The generic team member is now assigned to the task.</span></span>

    ![Thành viên nhóm chung được phân công cho nhiệm vụ](media/Resource-Management-image25.png)

    <span data-ttu-id="b1666-197">Trên tab **Nhóm**, bạn sẽ thấy thành viên nhóm chung mới.</span><span class="sxs-lookup"><span data-stu-id="b1666-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="b1666-198">Lưu ý rằng nó chỉ có giờ được phân công.</span><span class="sxs-lookup"><span data-stu-id="b1666-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="b1666-199">Các giờ này là tổng tất cả nhiệm vụ được phân công cho thành viên nhóm chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="b1666-200">Thành viên nhóm chung chưa có giờ yêu cầu hoặc yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Thành viên nhóm chung trên tab Nhóm](media/Resource-Management-image26.png)

5. <span data-ttu-id="b1666-202">Bạn hiện có thể phân công thành viên nhóm chung cho các nhiệm vụ khác bằng Bộ chọn nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Thành viên nhóm chung trong Bộ chọn nguồn lực](media/Resource-Management-image27.png)

    <span data-ttu-id="b1666-204">Khi đã hoàn tất việc phân công nguồn lực chung cho các nhiệm vụ, bạn có thể tạo yêu cầu nguồn lực cho nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="b1666-205">Trên tab **Nhóm**, hãy chọn nguồn lực chung rồi chọn **Tạo yêu cầu**.</span><span class="sxs-lookup"><span data-stu-id="b1666-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Lệnh Tạo yêu cầu](media/Resource-Management-image28.png)

    <span data-ttu-id="b1666-207">Khi yêu cầu được tạo, thành viên nhóm chung sẽ có giờ yêu cầu và liên kết cho yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Liên kết yêu cầu nguồn lực](media/Resource-Management-image29.png)

    <span data-ttu-id="b1666-209">Sau khi bạn đăng ký nguồn lực có tên, nguồn lực chung bị xóa khỏi nhóm và được thay thế bằng nguồn lực có tên.</span><span class="sxs-lookup"><span data-stu-id="b1666-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Nguồn lực chung được thay thế bằng nguồn lực có tên](media/Resource-Management-image30.png)

    <span data-ttu-id="b1666-211">Trên tab **Lịch trình**, phân công nguồn lực chung bị xóa và thay thế bằng nguồn lực có tên.</span><span class="sxs-lookup"><span data-stu-id="b1666-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Phân công nguồn lực chung được thay thế bằng nguồn lực có tên trên tab Lịch trình](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="b1666-213">Hành vi này chỉ xảy ra khi nguồn lực có tên được đăng ký đầy đủ cho yêu cầu nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="b1666-214">Chọn nguồn lực có tên thay thế một phần cho yêu cầu nguồn lực chung hoặc nhiều nguồn lực có tên thay thế cho yêu cầu nguồn lực chung, nguồn lực chung vẫn được phân công cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="b1666-215">Trong hình minh họa sau, một nhiệm vụ 80 giờ được lên kế hoạch trong thời gian 5 ngày (16 giờ/ngày trong 5 ngày) và được phân công cho nguồn lực chung có tên **Chức năng**.</span><span class="sxs-lookup"><span data-stu-id="b1666-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Nhiệm vụ 80 giờ, 5 ngày được phân công cho nguồn lực chung Chức năng](media/Resource-Management-image32.png)

    <span data-ttu-id="b1666-217">Khi bạn tạo yêu cầu, đó sẽ là yêu cầu 80 giờ trong 5 ngày.</span><span class="sxs-lookup"><span data-stu-id="b1666-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Yêu cầu được tạo ra cho 80 giờ trong 5 ngày](media/Resource-Management-image33.png)

    <span data-ttu-id="b1666-219">Vì các nguồn lực có sẵn chỉ làm việc 8 giờ/ngày nên sẽ cần 2 nguồn lực để đáp ứng yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="b1666-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Nguồn lực thứ hai](media/Resource-Management-image35.png)

    <span data-ttu-id="b1666-221">Trên tab **Nhóm**, bạn hiện có thể thấy nguồn lực chung không có giờ yêu cầu, nhưng giờ được phân công vẫn xuất hiện cùng với 2 nguồn lực có tên thực hiện.</span><span class="sxs-lookup"><span data-stu-id="b1666-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![2 nguồn lực có tên trên tab Nhóm](media/Resource-Management-image36.png)

    <span data-ttu-id="b1666-223">Trên tab **Lịch trình**, nguồn lực chung vẫn được phân công cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Nguồn lực chung trên tab Lịch trình](media/Resource-Management-image37.png)

<span data-ttu-id="b1666-225">PSA không phân công cả hai nguồn lực cho nhiệm vụ, vì hành vi đó sẽ tạo ra lịch trình khó dự đoán.</span><span class="sxs-lookup"><span data-stu-id="b1666-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="b1666-226">Trong ví dụ đơn giản này, thật dễ dàng để chia các giờ bằng nhau giữa hai nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="b1666-227">Tuy nhiên, trong trường hợp phức tạp hơn liên quan đến nhiều nhiệm vụ và nhiều nguồn lực, PSA sẽ phải đưa ra giả định về cách nó sẽ phân bổ các đăng ký nhận được cho nhiều nguồn lực trên nhiều nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="b1666-228">Do đó, trong các trường hợp này, người quản lý dự án phụ trách việc phân tích nhiều đăng ký và phân công các đăng ký đó nếu cần.</span><span class="sxs-lookup"><span data-stu-id="b1666-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="b1666-229">Để phân bổ các đăng ký, người quản lý dự án phân công các nhiệm vụ từ nguồn lực chung đến nguồn lực có tên, sau đó sử dụng dạng xem **Điều hòa** để đảm bảo phân bổ hoạt động với đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="b1666-230">Chỉnh sửa yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b1666-230">Edit a resource requirement</span></span>

<span data-ttu-id="b1666-231">Sau khi yêu cầu nguồn lực được tạo, người quản lý dự án hoặc người quản lý nguồn lực có thể muốn chỉnh sửa thông tin chi tiết để tinh chỉnh tiêu chí tìm kiếm khi Bảng lịch trình được dùng.</span><span class="sxs-lookup"><span data-stu-id="b1666-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="b1666-232">Để chỉnh sửa yêu cầu nguồn lực, hãy làm theo các bước sau.</span><span class="sxs-lookup"><span data-stu-id="b1666-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="b1666-233">Trên trang **Dự án**, trên tab **Nhóm**, hãy chọn liên kết đến bất kỳ yêu cầu nào trên nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="b1666-234">Trên trang **Yêu cầu nguồn lực** xuất hiện, bạn có thể cập nhật một số thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="b1666-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="b1666-235">Dưới đây là một số ví dụ:</span><span class="sxs-lookup"><span data-stu-id="b1666-235">Here are some examples:</span></span>

    - <span data-ttu-id="b1666-236">Tên</span><span class="sxs-lookup"><span data-stu-id="b1666-236">Name</span></span>
    - <span data-ttu-id="b1666-237">Từ Ngày</span><span class="sxs-lookup"><span data-stu-id="b1666-237">From Date</span></span>
    - <span data-ttu-id="b1666-238">Đến Ngày</span><span class="sxs-lookup"><span data-stu-id="b1666-238">To Date</span></span>
    - <span data-ttu-id="b1666-239">Khoảng thời gian</span><span class="sxs-lookup"><span data-stu-id="b1666-239">Duration</span></span>
    - <span data-ttu-id="b1666-240">Loại Nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b1666-240">Resource Type</span></span>

<span data-ttu-id="b1666-241">Trên trang **Yêu cầu nguồn lực**, người quản lý dự án hoặc người quản lý nguồn lực cũng có thể xác định thông tin sau:</span><span class="sxs-lookup"><span data-stu-id="b1666-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="b1666-242">Kỹ năng</span><span class="sxs-lookup"><span data-stu-id="b1666-242">Skills</span></span>
- <span data-ttu-id="b1666-243">Vai trò</span><span class="sxs-lookup"><span data-stu-id="b1666-243">Roles</span></span>
- <span data-ttu-id="b1666-244">Các tùy chọn nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b1666-244">Resource preferences</span></span>
- <span data-ttu-id="b1666-245">Đơn vị tổ chức ưu tiên</span><span class="sxs-lookup"><span data-stu-id="b1666-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="b1666-246">Cập nhật đăng ký nguồn lực sau khi chúng được đăng ký trên dự án</span><span class="sxs-lookup"><span data-stu-id="b1666-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="b1666-247">Sau khi thêm nguồn lực chung hoặc có tên vào nhóm dự án, bạn có thể thay đổi đăng ký của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="b1666-248">Trên trang **Dự án**, trên tab **Nhóm**, hãy chọn thành viên nhóm rồi chọn **Duy trì đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="b1666-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Bảng lịch trình mở cho thành viên nhóm đã chọn](media/Resource-Management-image40.png)

    <span data-ttu-id="b1666-250">Bảng lịch trình xuất hiện và hiển thị các đăng ký của thành viên nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="b1666-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="b1666-251">Mở rộng hồ sơ của thành viên nhóm để xem những giờ đã được đặt với dự án này và các dự án khác đang sử dụng năng lực của thành viên nhóm.</span><span class="sxs-lookup"><span data-stu-id="b1666-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="b1666-252">Chọn và kéo đăng ký để mở rộng hoặc thu gọn.</span><span class="sxs-lookup"><span data-stu-id="b1666-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="b1666-253">Hộp thoại **Tạo đăng ký nguồn lực** xuất hiện cho phép bạn điều chỉnh đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Hộp thoại Tạo đăng ký nguồn lực](media/Resource-Management-image41.png)

3. <span data-ttu-id="b1666-255">Bấm chuột phải vào đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-255">Right-click the booking.</span></span> <span data-ttu-id="b1666-256">Sau đó, bạn có thể dùng menu phím tắt để hoàn thành các hành động sau:</span><span class="sxs-lookup"><span data-stu-id="b1666-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="b1666-257">Thay đổi trạng thái đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-257">Change the booking status.</span></span>
    - <span data-ttu-id="b1666-258">Chỉnh sửa đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-258">Edit the booking.</span></span>
    - <span data-ttu-id="b1666-259">Thay thế nguồn lực trên nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="b1666-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="b1666-260">Thay đổi trạng thái đăng ký</span><span class="sxs-lookup"><span data-stu-id="b1666-260">Change the booking status</span></span>

<span data-ttu-id="b1666-261">Bạn có thể thay đổi bất kỳ trạng thái đăng ký mặc định hoặc tùy chỉnh nào.</span><span class="sxs-lookup"><span data-stu-id="b1666-261">You can change any default or custom booking status.</span></span>

![Lệnh Thay đổi trạng thái](media/Resource-Management-image42.png)

<span data-ttu-id="b1666-263">Các trạng thái sau có trong PSA:</span><span class="sxs-lookup"><span data-stu-id="b1666-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="b1666-264">**Đã hủy** – Trạng thái này hủy đăng ký của nguồn lực và giải phóng năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="b1666-265">**Đăng ký chắc chắn** – Trạng thái này chiếm năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="b1666-266">Đăng ký thường có trạng thái này khi bạn mở **Duy trì đăng ký** từ lưới **Tất cả thành viên nhóm** trên trang **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="b1666-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="b1666-267">**Đăng ký không chắc chắn** – Trạng thái này thêm nguồn lực vào nhóm nhưng không chiếm năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="b1666-268">Trạng thái này cho biết nguồn lực đã được dự trữ cho công việc tiềm năng nhưng vẫn có năng lực nếu công việc khác cần.</span><span class="sxs-lookup"><span data-stu-id="b1666-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="b1666-269">Trong dạng xem tổng quan về trạng thái rảnh/bận của nguồn lực, đăng ký không chắc chắn có trạng thái khác với đăng ký chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="b1666-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="b1666-270">**Đã đề xuất** – Trạng thái này thể hiện nguồn lực được người quản lý nguồn lực hoặc người quản lý dự án đề xuất.</span><span class="sxs-lookup"><span data-stu-id="b1666-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="b1666-271">Đề xuất không chiếm năng lực của nguồn lực và nguồn lực không được thêm vào nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="b1666-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="b1666-272">Để đăng ký nguồn lực đó trên nhóm một cách chắc chắn, người quản lý dự án phải chấp nhận đề xuất.</span><span class="sxs-lookup"><span data-stu-id="b1666-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="b1666-273">Gửi yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b1666-273">Submit resource requests</span></span>

<span data-ttu-id="b1666-274">Yêu cầu nguồn lực dùng để thực hiện nhu cầu (yêu cầu nguồn lực) phải được người quản lý nguồn lực thực hiện.</span><span class="sxs-lookup"><span data-stu-id="b1666-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="b1666-275">Đối với nguồn lực chung đã có trong nhóm, bạn có thể gửi trực tiếp yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="b1666-276">Yêu cầu nguồn lực có thể được thực hiện theo hai cách:</span><span class="sxs-lookup"><span data-stu-id="b1666-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="b1666-277">Người quản lý nguồn lực trực tiếp đáp ứng yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="b1666-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="b1666-278">Trong trường hợp này, nguồn lực chung được thay thế bằng đăng ký chắc chắn có nguồn lực có tên.</span><span class="sxs-lookup"><span data-stu-id="b1666-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="b1666-279">Người quản lý nguồn lực đề xuất nguồn lực cho người quản lý dự án và người quản lý dự án phê duyệt hoặc từ chối nguồn lực được đề xuất.</span><span class="sxs-lookup"><span data-stu-id="b1666-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="b1666-280">Thực hiện trực tiếp yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b1666-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="b1666-281">Khi yêu cầu nguồn lực được tạo, người quản lý dự án có thể gửi yêu cầu nguồn lực cho nguồn lực chung bằng cách chọn nguồn lực, sau đó chọn **Gửi yêu cầu**.</span><span class="sxs-lookup"><span data-stu-id="b1666-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Nút Gửi yêu cầu](media/Resource-Management-image45.png)

<span data-ttu-id="b1666-283">Nhận xét về nguồn lực có thể được cung cấp cho người quản lý nguồn lực đang thực hiện yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="b1666-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="b1666-284">Sau khi yêu cầu được gửi, trường **Trạng thái** cho thành viên nhóm được thay đổi thành **Đã gửi**.</span><span class="sxs-lookup"><span data-stu-id="b1666-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Nhập nhận xét tùy chọn](media/Resource-Management-image46.png)

<span data-ttu-id="b1666-286">Khi người quản lý nguồn lực đáp ứng yêu cầu, thành viên nhóm chung được thay thế bằng nguồn lực có tên trong lưới **Tất cả thành viên nhóm**.</span><span class="sxs-lookup"><span data-stu-id="b1666-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Thành viên nhóm chung được thay thế bằng nguồn lực có tên trong lưới Tất cả thành viên nhóm](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="b1666-288">Sử dụng đề xuất nguồn lực cho yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b1666-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="b1666-289">Người quản lý nguồn lực có thể đề xuất nguồn lực cho người quản lý dự án thay vì trực tiếp đăng ký nguồn lực trên yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="b1666-290">Người quản lý nguồn lực có thể dùng tùy chọn này khi không có kết hợp chính xác cho yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="b1666-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="b1666-291">Khi người quản lý nguồn lực đề xuất nguồn lực, người quản lý dự án sẽ thấy trường **Trạng thái** cho thành viên nhóm chung được thay đổi thành **Cần đánh giá**.</span><span class="sxs-lookup"><span data-stu-id="b1666-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Trạng thái của thành viên nhóm chung thay đổi thành Cần đánh giá](media/Resource-Management-image48.png)

<span data-ttu-id="b1666-293">Để xem nguồn lực được đề xuất cùng với trực quan hóa hiệu ứng đăng ký của đề xuất, hãy bấm đúp vào thành viên nhóm có trạng thái **Cần đánh giá**.</span><span class="sxs-lookup"><span data-stu-id="b1666-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="b1666-294">Sau đó, chọn tab **Nguồn lực được đề xuất**.</span><span class="sxs-lookup"><span data-stu-id="b1666-294">Then select the **Proposed Resources** tab.</span></span>

![Tab Nguồn lực được đề xuất](media/Resource-Management-image49.png)

<span data-ttu-id="b1666-296">Chọn **Chấp nhận tất cả đề xuất** để chấp nhận tất cả nguồn lực được đề xuất hoặc **Từ chối tất cả đề xuất** để từ chối các nguồn lực đó.</span><span class="sxs-lookup"><span data-stu-id="b1666-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="b1666-297">Nếu bạn chấp nhận các nguồn lực được đề xuất, thì các nguồn lực này được đăng ký chắc chắn trên dự án ở dạng thành viên nhóm và thay thế nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="b1666-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="b1666-298">Bạn phải chấp nhận hoặc từ chối tất cả nguồn lực được đề xuất.</span><span class="sxs-lookup"><span data-stu-id="b1666-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="b1666-299">Bạn không thể chấp nhận một phần hoặc từ chối các nguồn lực này.</span><span class="sxs-lookup"><span data-stu-id="b1666-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="b1666-300">Thay thế nguồn lực trên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="b1666-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="b1666-301">Đôi khi, người quản lý dự án phải thay thế một thành viên nhóm đã đăng ký trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="b1666-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="b1666-302">Trong trang **Dự án**, trên tab **Nhóm**, hãy chọn nguồn lực cần thay thế rồi chọn **Duy trì đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="b1666-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="b1666-303">Bung rộng nguồn lực để xem các dự án mà nguồn lực này được phân công.</span><span class="sxs-lookup"><span data-stu-id="b1666-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Nguồn lực được bung rộng để hiển thị các dự án được phân công](media/Resource-Management-image50.png)

3. <span data-ttu-id="b1666-305">Bấm chuột phải vào dự án rồi chọn **Thay thế nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="b1666-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="b1666-306">Nếu bạn biết nguồn lực mà bạn muốn thay thế cho nguồn lực hiện tại, hãy chọn hoặc nhập tên rồi chọn **Phân công lại**.</span><span class="sxs-lookup"><span data-stu-id="b1666-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Chỉ định nguồn lực thay thế](media/Resource-Management-image51.png)

    <span data-ttu-id="b1666-308">Ngoài ra, hãy làm theo các bước sau để tìm kiếm nguồn lực:</span><span class="sxs-lookup"><span data-stu-id="b1666-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="b1666-309">Chọn **Tìm mục thay thế**.</span><span class="sxs-lookup"><span data-stu-id="b1666-309">Select **Find Substitution**.</span></span>

        ![Tìm kiếm nguồn lực thay thế](media/Resource-Management-image52.png)

        <span data-ttu-id="b1666-311">Trợ lý lập lịch biểu trả về danh sách các thay thế có sẵn.</span><span class="sxs-lookup"><span data-stu-id="b1666-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="b1666-312">Trong Trợ lý lập lịch biểu, bạn có thể lọc thêm các nguồn lực có sẵn để tìm mục thay thế thích hợp.</span><span class="sxs-lookup"><span data-stu-id="b1666-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Danh sách mục thay thế có sẵn](media/Resource-Management-image53.png)

    2. <span data-ttu-id="b1666-314">Để thay thế nguồn lực, hãy chọn nguồn lực mà bạn muốn rồi chọn **Thay thế**.</span><span class="sxs-lookup"><span data-stu-id="b1666-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Nguồn lực thay thế đã chọn](media/Resource-Management-image54.png)

    <span data-ttu-id="b1666-316">Đăng ký và phân công được thay thế bằng nguồn lực mới.</span><span class="sxs-lookup"><span data-stu-id="b1666-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Đăng ký và phân công được thay thế bằng nguồn lực mới](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="b1666-318">Điều hòa phân công và đăng ký thành viên nhóm</span><span class="sxs-lookup"><span data-stu-id="b1666-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="b1666-319">Đối với các thành viên nhóm, đăng ký và phân công được kết hợp lỏng lẻo.</span><span class="sxs-lookup"><span data-stu-id="b1666-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="b1666-320">Nói cách khác, nguồn lực có thể có phân công nhưng không có đăng ký hoặc ngược lại.</span><span class="sxs-lookup"><span data-stu-id="b1666-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="b1666-321">Tốt hơn hết, đăng ký nên phù hợp với phân công để các nguồn lực có năng lực được cam kết có thể thực hiện các phân công nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="b1666-322">Tuy nhiên, đăng ký có thể dựa trên trạng thái rảnh/bận và thời gian nhiệm vụ có thể thay đổi khi dự án tiếp tục.</span><span class="sxs-lookup"><span data-stu-id="b1666-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="b1666-323">Do đó, việc kết hợp lỏng lẻo đăng ký và phân công mang đến sự linh hoạt.</span><span class="sxs-lookup"><span data-stu-id="b1666-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="b1666-324">PSA có tab **Điều hòa** cho phép người quản lý dự án điều hòa đăng ký và phân công của thành viên nhóm cho dự án.</span><span class="sxs-lookup"><span data-stu-id="b1666-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Tab Điều hòa](media/Resource-Management-image56.png)

<span data-ttu-id="b1666-326">Tab **Điều hòa** hiển thị đăng ký và phân công đến mức phân công nhiệm vụ cá nhân cho từng thành viên nhóm.</span><span class="sxs-lookup"><span data-stu-id="b1666-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="b1666-327">Tab này hiển thị giờ trong các ô thể hiện cho khoảng thời gian từ tháng đến ngày.</span><span class="sxs-lookup"><span data-stu-id="b1666-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="b1666-328">Tab này cũng hiển thị tổng số ròng tổng thể cho dự án, cùng với cột tổng.</span><span class="sxs-lookup"><span data-stu-id="b1666-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="b1666-329">Đối với mỗi nguồn lực, tab này tính toán khác biệt giữa đăng ký của thành viên nhóm và tổng số phân công nhiệm vụ của thành viên nhóm đó.</span><span class="sxs-lookup"><span data-stu-id="b1666-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="b1666-330">Khác biệt lý tưởng nhất là 0 (không).</span><span class="sxs-lookup"><span data-stu-id="b1666-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="b1666-331">Nói cách khác, không nên có sự khác biệt giữa đăng ký và phân công.</span><span class="sxs-lookup"><span data-stu-id="b1666-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="b1666-332">Khác biệt được tô và đánh bóng để dễ thấy 2 trạng thái:</span><span class="sxs-lookup"><span data-stu-id="b1666-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="b1666-333">**Thiếu đăng ký** – Thiếu đăng ký xảy ra khi nguồn lực có nhiều phân công hơn đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b1666-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="b1666-334">Do năng lực này không được đăng ký trước nên người quản lý dự án có thể chỉnh sửa trạng thái này bằng cách mở rộng đăng ký nguồn lực để trang trải thâm hụt.</span><span class="sxs-lookup"><span data-stu-id="b1666-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="b1666-335">**Đăng ký vượt mức** – Đăng ký vượt mức có thể xảy ra khi nguồn lực được đăng ký cho dự án nhưng không được phân công cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="b1666-336">Trạng thái này có thể chấp nhận được trong các trường hợp nguồn lực được đăng ký cho dự án trước khi phân công nhiệm vụ diễn ra.</span><span class="sxs-lookup"><span data-stu-id="b1666-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="b1666-337">Tuy nhiên, trong các trường hợp khác, nguồn lực không được lên kế hoạch để được phân công nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="b1666-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="b1666-338">Trong những trường hợp này, người quản lý dự án nên xem xét hủy bỏ các đăng ký của nguồn lực để năng lực đó có thể dùng cho dự án khác.</span><span class="sxs-lookup"><span data-stu-id="b1666-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="b1666-339">Trong một số trường hợp, khi thấy mức thời gian cao hơn mức ngày (ví dụ: mức tháng), bạn có thể thấy khác biệt thực 0 cho nguồn lực (nói cách khác là đăng ký = phân công).</span><span class="sxs-lookup"><span data-stu-id="b1666-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="b1666-340">Tuy nhiên, nếu thấy thời gian ở mức tuần, bạn có thể thấy phân công 0 giờ hoặc đăng ký 40 giờ trong tuần đầu tiên nhưng phân công 40 giờ và đăng ký 0 giờ trong tuần thứ hai.</span><span class="sxs-lookup"><span data-stu-id="b1666-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="b1666-341">Nhìn chung, đăng ký và phân công được điều hòa nhưng khác nhau giữa một tuần và tuần tiếp theo.</span><span class="sxs-lookup"><span data-stu-id="b1666-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="b1666-342">Khi bạn thấy thời gian ở các mức cao hơn, các ô trong tab **Điều hòa** có chỉ báo để báo cho bạn biết rằng có sự khác biệt ở các mức thấp hơn.</span><span class="sxs-lookup"><span data-stu-id="b1666-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="b1666-343">Bằng cách bấm đúp vào một ô, bạn có thể phóng to để xem sự khác biệt.</span><span class="sxs-lookup"><span data-stu-id="b1666-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="b1666-344">Sau đó, bạn có thể bấm chuột phải để thu nhỏ. Bằng cách chọn một nguồn lực, sau đó dùng điều khiển **Khác biệt tiếp theo** trên thanh công cụ lưới, bạn có thể chuyển đến khác biệt tiếp theo giữa đăng ký và phân công cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="b1666-345">Sau đó, bạn có thể dùng điều khiển **Khác biệt trước đó** để quay lại.</span><span class="sxs-lookup"><span data-stu-id="b1666-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="b1666-346">Bạn cũng có thể tắt chỉ báo khác biệt và hành vi điều hướng trong **Cài đặt**.</span><span class="sxs-lookup"><span data-stu-id="b1666-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Chỉ báo khác biệt](media/Resource-Management-image57.png)

<span data-ttu-id="b1666-348">Nếu bạn có phân công nhiệm vụ cho nguồn lực nhưng không có đăng ký, trên trang **Dự án**, trên tab **Điều hòa**, hãy chọn thiếu đăng ký rồi chọn **Mở rộng đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="b1666-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="b1666-349">Hộp thoại **Mở rộng đăng ký** xuất hiện và hiển thị đăng ký cần thiết để khắc phục tình trạng thiếu của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b1666-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="b1666-350">Hộp thoại này cũng hiển thị đăng ký hiện có của nguồn lực trên tất cả dự án hoặc các thực thể có thể lập lịch khác.</span><span class="sxs-lookup"><span data-stu-id="b1666-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="b1666-351">Nếu chọn **OK** để tạo đăng ký cho nguồn lực, bất kể trạng thái rảnh/bận của nguồn lực, bạn có thể gây ra tình trạng đăng ký vượt mức.</span><span class="sxs-lookup"><span data-stu-id="b1666-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Hộp thoại Mở rộng đăng ký](media/Resource-Management-image58.png)

<span data-ttu-id="b1666-353">Người quản lý dự án hoặc người quản lý nguồn lực có thể dùng Bảng lịch trình để quản lý mọi tình huống nguồn lực bị đăng ký quá mức so với năng lực của họ.</span><span class="sxs-lookup"><span data-stu-id="b1666-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
