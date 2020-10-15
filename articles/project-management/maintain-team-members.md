---
title: Duy trì thành viên nhóm
description: Chủ đề này cung cấp thông tin về cách đặt nguồn lực có tên cho nhóm dự án và phân công tác vụ.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961973"
---
# <a name="maintain-team-members"></a><span data-ttu-id="c8882-103">Duy trì thành viên nhóm</span><span class="sxs-lookup"><span data-stu-id="c8882-103">Maintain team members</span></span>

<span data-ttu-id="c8882-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="c8882-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c8882-105">Bạn có thể thêm nguồn lực được đặt tên vào nhóm dự án của mình bằng cách đặt lịch trực tiếp họ vào nhóm.</span><span class="sxs-lookup"><span data-stu-id="c8882-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="c8882-106">Trong Dynamics 365 Project Operations, chuyển đến **Dự án**, sau đó chọn mở dự án mà bạn đặt lịch.</span><span class="sxs-lookup"><span data-stu-id="c8882-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="c8882-107">Trên trang **Dự án**, trên tab **Nhóm**, hãy chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="c8882-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="c8882-108">Trong hộp thoại **Tạo nhanh thành viên nhóm dự án**, chọn nguồn lực có thể đặt lịch.</span><span class="sxs-lookup"><span data-stu-id="c8882-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="c8882-109">Trường **Vai trò** sẽ điền bằng vai trò mặc định của nguồn lực nếu họ được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="c8882-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="c8882-110">Bạn có thể thay đổi vai trò này.</span><span class="sxs-lookup"><span data-stu-id="c8882-110">You can change the role.</span></span> 
4. <span data-ttu-id="c8882-111">Chọn ngày bắt đầu và kết thúc mà nguồn lực sẽ cần và chọn phương pháp phân bổ năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="c8882-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="c8882-112">Nếu bạn muốn thành viên nhóm là người phê duyệt dự án, hãy chọn **Có** trong trường **Người phê duyệt dự án**.</span><span class="sxs-lookup"><span data-stu-id="c8882-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="c8882-113">Thành viên nhóm có thể phê duyệt các mục nhập thời gian và chi phí đã gửi cho dự án này.</span><span class="sxs-lookup"><span data-stu-id="c8882-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="c8882-114">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="c8882-114">Select **Save**.</span></span>

<span data-ttu-id="c8882-115">Bây giờ bạn có thể gán nguồn lực đã đặt cho các nhiệm vụ dự án.</span><span class="sxs-lookup"><span data-stu-id="c8882-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="c8882-116">Trên trang **Dự án**, trên tab **Lên lịch**, hãy gán nhiệm vụ cho nguồn lực mới.</span><span class="sxs-lookup"><span data-stu-id="c8882-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="c8882-117">Bộ chọn nguồn lực được khởi chạy từ trường **Nguồn lực** trong lưới nhiệm vụ sẽ hiển thị các thành viên nhóm mà bạn có thể chọn.</span><span class="sxs-lookup"><span data-stu-id="c8882-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="c8882-118">Trong Project Operations, việc đăng ký nguồn lực và gán nhiệm vụ không kết hợp chặt chẽ với nhau.</span><span class="sxs-lookup"><span data-stu-id="c8882-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="c8882-119">Khi bạn sử dụng bộ chọn nguồn lực trong lịch trình, bạn có thể gán nhiệm vụ cho các thành viên trong nhóm trong nhiều giờ hơn so với đặt lịch của họ trên dự án.</span><span class="sxs-lookup"><span data-stu-id="c8882-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="c8882-120">Điểm khác biệt giữa gán và đăng ký thành viên nhóm được hiển thị trên các tab **Nhóm** và **Điều hòa nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="c8882-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="c8882-121">Bạn cũng có thể điều chỉnh điểm khác biệt giữa đăng ký và gán cho các nguồn lực ở mức chi tiết hơn.</span><span class="sxs-lookup"><span data-stu-id="c8882-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="c8882-122">Sử dụng bộ chọn nguồn lực trên tab **Lên lịch** để tìm kiếm và chọn các nguồn lực có thể đặt lịch không phải là một phần của nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="c8882-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="c8882-123">Những nguồn lực này được hiển thị trong bộ chọn nguồn lực dưới dạng **Nguồn lực khác**.</span><span class="sxs-lookup"><span data-stu-id="c8882-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="c8882-124">Khi bạn chọn, nguồn lực đó sẽ được thêm vào nhóm dự án và phân công tác vụ, nhưng không tạo đặt lịch.</span><span class="sxs-lookup"><span data-stu-id="c8882-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="c8882-125">Bạn có thể sử dụng khả năng đặt lịch mở rộng của tab **Hợp nhất** hoặc **Bảng lịch trình** để đặt lịch năng lực của nguồn lực cho dự án.</span><span class="sxs-lookup"><span data-stu-id="c8882-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="c8882-126">Sau khi một thành viên nhóm được đặt lịch trên dự án của bạn, bạn có thể sử dụng **Duy trì đăng ký** hoặc sử dụng **Bảng lịch trình** để trực tiếp quản lý đăng ký của họ.</span><span class="sxs-lookup"><span data-stu-id="c8882-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
