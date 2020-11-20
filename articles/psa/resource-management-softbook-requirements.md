---
title: Đăng ký không chắc chắn yêu cầu
description: Chủ đề này cung cấp thông tin về cách đăng ký không chắc chắn yêu cầu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124124"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="f5852-103">Đăng ký không chắc chắn yêu cầu</span><span class="sxs-lookup"><span data-stu-id="f5852-103">Soft-book requirements</span></span>

<span data-ttu-id="f5852-104">Yêu cầu nguồn lực có thể được đăng ký chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="f5852-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="f5852-105">Đăng ký chắc chắn tạo ra đề xuất chiếm năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="f5852-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="f5852-106">Sau đó, đề xuất này được gửi lại cho người yêu cầu để phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="f5852-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="f5852-107">Đăng ký không chắc chắn dự định bổ sung nguồn lực vào nhóm dự án và có trạng thái khác trên Bảng lịch trình nhưng không chiếm năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="f5852-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="f5852-108">Để đăng ký không chắc chắn nguồn lực từ Bảng lịch trình, hãy đặt trường **Trạng thái đăng ký** thành **Không chắc chắn**.</span><span class="sxs-lookup"><span data-stu-id="f5852-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Trạng thái đăng ký được đặt thành Không chắc chắn](media/Resource-Management-image77.png)

<span data-ttu-id="f5852-110">Khi tab **Nhóm** ở trong dạng xem **Thành viên nhóm có tên**, nguồn lực xuất hiện ở đó.</span><span class="sxs-lookup"><span data-stu-id="f5852-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="f5852-111">Giờ đăng ký không chắc chắn được báo cáo trong cột **Giờ đăng ký không chắc chắn**.</span><span class="sxs-lookup"><span data-stu-id="f5852-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Giờ đăng ký không chắc chắn trong dạng xem Thành viên nhóm có tên](media/Resource-Management-image78.png)

<span data-ttu-id="f5852-113">Có thể phân công nhiệm vụ cho các thành viên nhóm được đăng ký không chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="f5852-113">Soft-booked team members can be assigned to tasks.</span></span>

![Thành viên nhóm được đăng ký không chắc chắn được phân công nhiệm vụ](media/Resource-Management-image79.png)

<span data-ttu-id="f5852-115">Trên tab **Điều hòa**, không có đăng ký hiển thị cho nguồn lực được đăng ký không chắc chắn do tab **Điều hòa** chỉ xem xét các đăng ký chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="f5852-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Nguồn lực được đăng ký không chắc chắn không có đăng ký trên tab Điều hòa](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="f5852-117">Bạn không thể đăng ký không chắc chắn nguồn lực từ yêu cầu do thành viên nhóm chung tạo.</span><span class="sxs-lookup"><span data-stu-id="f5852-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="f5852-118">Trên Bảng lịch trình, tô màu khác nhau được dùng cho đăng ký chắc chắn cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="f5852-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Đăng ký không chắc chắn trên Bảng lịch trình](media/Resource-Management-image81.png)

<span data-ttu-id="f5852-120">Để chuyển đổi đăng ký không chắc chắn thành đăng ký chắc chắn, trên Bảng lịch trình, hãy bấm chuột phải vào đăng ký chắc chắn rồi chọn **Thay đổi trạng thái** \> **Đăng ký chắc chắn** \> **Chắc chắn**.</span><span class="sxs-lookup"><span data-stu-id="f5852-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Thay đổi trạng thái đăng ký thành Chắc chắn](media/Resource-Management-image82.png)

<span data-ttu-id="f5852-122">Đăng ký thay đổi và trạng thái được thay đổi trên Bảng lịch trình.</span><span class="sxs-lookup"><span data-stu-id="f5852-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="f5852-123">Vì trạng thái đăng ký hiện là **Chắc chắn**, nên nguồn lực hiển thị ở trạng thái đã đăng ký và năng lực cũng như trạng thái rảnh/bận của nguồn lực được điều chỉnh.</span><span class="sxs-lookup"><span data-stu-id="f5852-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="f5852-124">Bạn có thể dùng cùng một phương pháp để đăng ký chắc chắn hoặc không chắc chắn từ Bảng lịch trình.</span><span class="sxs-lookup"><span data-stu-id="f5852-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="f5852-125">Để chuyển đổi nguồn lực được đăng ký không chắc chắn thành đăng ký chắc chắn trên tab **Nhóm**, hãy chọn nguồn lực rồi chọn **Xác nhận**.</span><span class="sxs-lookup"><span data-stu-id="f5852-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Lệnh xác nhận](media/Resource-Management-image83.png)
