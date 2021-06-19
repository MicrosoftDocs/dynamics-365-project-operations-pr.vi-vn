---
title: Mục đặt trước và mục chỉ định
description: Chủ đề này cung cấp thông tin về sự khác biệt giữa đặt trước nguồn lực và chỉ định nguồn lực.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012792"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="ebbec-103">Mục đặt trước và mục chỉ định</span><span class="sxs-lookup"><span data-stu-id="ebbec-103">Bookings vs assignments</span></span>

<span data-ttu-id="ebbec-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="ebbec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ebbec-105">Đăng ký là việc phân bổ nguồn lực cho dự án theo cách chắc chắn hoặc không chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="ebbec-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="ebbec-106">Đăng ký chắc chắn chiếm năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="ebbec-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="ebbec-107">Bookings trình bày những ý tưởng của tổ chức cho các nhóm để họ có thể hiểu các nguồn lực sẽ tham gia vào những dự án khác nhau như thế nào.</span><span class="sxs-lookup"><span data-stu-id="ebbec-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="ebbec-108">Dynamics 365 Project Operations xem lượt đăng ký là một khái niệm ở cấp dự án.</span><span class="sxs-lookup"><span data-stu-id="ebbec-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="ebbec-109">Khác với các lượt đăng ký, nhiệm vụ là cam kết về nguồn lực cho những tác vụ dự án trong lịch trình dự án.</span><span class="sxs-lookup"><span data-stu-id="ebbec-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="ebbec-110">Các nguồn lực có thể chung chung hoặc được đặt tên.</span><span class="sxs-lookup"><span data-stu-id="ebbec-110">The resources can be named or generic.</span></span>  <span data-ttu-id="ebbec-111">Khi một yêu cầu nguồn lực có nguồn gốc từ các phân công nhiệm vụ dự án, Project Operations sử dụng phân phối giờ làm việc trong phân công nguồn lực để xây dựng phân phối giờ làm việc trong chi tiết yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="ebbec-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="ebbec-112">Tuy nhiên, tham chiếu đến các phân công nguồn lực không được duy trì.</span><span class="sxs-lookup"><span data-stu-id="ebbec-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="ebbec-113">Nội dung cập nhật đối với lượt đăng ký bắt nguồn từ yêu cầu nguồn lực sẽ không cập nhật bất kỳ phân công nguồn lực nào.</span><span class="sxs-lookup"><span data-stu-id="ebbec-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="ebbec-114">Thông thường, tổng số lượt đăng ký cho một nguồn lực sẽ bằng tổng các nhiệm vụ của một hoặc nhiều tác vụ được chỉ định cho nguồn lực đó.</span><span class="sxs-lookup"><span data-stu-id="ebbec-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="ebbec-115">Tuy nhiên, Project Operations không đảm bảo sự thống nhất này.</span><span class="sxs-lookup"><span data-stu-id="ebbec-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="ebbec-116">Dạng xem **Điều hòa** cho Người quản lý dự án thấy các vị trí mà lượt đăng ký và nhiệm vụ của nguồn lực không thống nhất với nhau.</span><span class="sxs-lookup"><span data-stu-id="ebbec-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]