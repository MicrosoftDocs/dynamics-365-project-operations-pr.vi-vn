---
title: Các khái niệm chính về quản lý nguồn lực
description: Chủ đề này cung cấp thông tin về chức năng quản lý nguồn lực trong Microsoft Dynamics Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 124d9bad5cc0c16955417a8213db047a2d8bae1d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897567"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="5de0d-103">Các khái niệm chính về quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="5de0d-103">Resource management key concepts</span></span>

<span data-ttu-id="5de0d-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="5de0d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5de0d-105">Nguồn lực là tài sản quan trọng nhất của tổ chức dựa trên dịch vụ.</span><span class="sxs-lookup"><span data-stu-id="5de0d-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="5de0d-106">Khả năng tìm đúng nguồn lực vào đúng thời gian, đặt những nguồn lực đó vào các dự án và tiếp tục sử dụng các nguồn lực giúp các tổ chức đạt mục tiêu doanh thu và mục tiêu hài lòng của khách hàng.</span><span class="sxs-lookup"><span data-stu-id="5de0d-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="5de0d-107">Bạn có thể dùng chức năng cung cấp nguồn lực cho dự án trong Dynamics 365 Project Operations để làm những nhiệm vụ sau:</span><span class="sxs-lookup"><span data-stu-id="5de0d-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="5de0d-108">Tạo nhóm dự án bằng cách đăng ký các nguồn lực sẵn có và đủ điều kiện.</span><span class="sxs-lookup"><span data-stu-id="5de0d-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="5de0d-109">Tạo hồ sơ thành viên nhóm chung và xác định vai trò cũng như đơn vị tổ chức nguồn lực của họ.</span><span class="sxs-lookup"><span data-stu-id="5de0d-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="5de0d-110">Tạo yêu cầu nguồn lực cho các thành viên nhóm chung từ phân công nhiệm vụ của họ.</span><span class="sxs-lookup"><span data-stu-id="5de0d-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="5de0d-111">Khớp kỹ năng bằng cách xác định các kỹ năng được nêu trên nhu cầu nguồn lực so với các kỹ năng nguồn lực sẵn có.</span><span class="sxs-lookup"><span data-stu-id="5de0d-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="5de0d-112">Thay thế nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="5de0d-112">Substitute resources.</span></span>
- <span data-ttu-id="5de0d-113">Căn chỉnh các phân bổ lịch trình dự án và đăng ký nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="5de0d-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="5de0d-114">Điều hòa sự khác biệt trong đăng ký và phân công.</span><span class="sxs-lookup"><span data-stu-id="5de0d-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="5de0d-115">Thay đổi đăng ký nguồn lực để phản hồi trạng thái ngoài văn phòng.</span><span class="sxs-lookup"><span data-stu-id="5de0d-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="5de0d-116">Cộng tác giữa người quản lý dự và người quản lý nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="5de0d-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="5de0d-117">Xem lịch sử của thời gian làm việc của nguồn lực so với mục tiêu, bao gồm cả lỗi về cách sử dụng thời gian của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="5de0d-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="5de0d-118">Duy trì kho lưu trữ kỹ năng và mức độ thành thạo.</span><span class="sxs-lookup"><span data-stu-id="5de0d-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="5de0d-119">Bạn có thể bố trí nhân viên cho dự án bằng nhóm nguồn lực chung hoặc có tên trong Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5de0d-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="5de0d-120">Bạn có thể dùng nhiều phương pháp khác nhau để thêm và phân công các thành viên nhóm và để quản ký đăng ký cũng như phân công của bạn.</span><span class="sxs-lookup"><span data-stu-id="5de0d-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
