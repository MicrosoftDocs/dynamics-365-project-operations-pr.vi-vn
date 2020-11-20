---
title: Mục đặt trước và mục chỉ định
description: Chủ đề này cung cấp thông tin về sự khác biệt giữa đặt trước nguồn lực và chỉ định nguồn lực.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130244"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="bb177-103">Mục đặt trước và mục chỉ định</span><span class="sxs-lookup"><span data-stu-id="bb177-103">Bookings vs assignments</span></span>

<span data-ttu-id="bb177-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="bb177-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bb177-105">Đăng ký là việc phân bổ nguồn lực cho dự án theo cách chắc chắn hoặc không chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="bb177-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="bb177-106">Đăng ký chắc chắn chiếm năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="bb177-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="bb177-107">Bookings trình bày những ý tưởng của tổ chức cho các nhóm để họ có thể hiểu các nguồn lực sẽ tham gia vào những dự án khác nhau như thế nào.</span><span class="sxs-lookup"><span data-stu-id="bb177-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="bb177-108">Dynamics 365 Project Operations xem lượt đăng ký là một ý tưởng ở cấp dự án.</span><span class="sxs-lookup"><span data-stu-id="bb177-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="bb177-109">Khác với các lượt đăng ký, nhiệm vụ là cam kết về nguồn lực cho những tác vụ dự án trong lịch trình dự án.</span><span class="sxs-lookup"><span data-stu-id="bb177-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="bb177-110">Các nguồn lực có thể chung chung hoặc được đặt tên.</span><span class="sxs-lookup"><span data-stu-id="bb177-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="bb177-111">Thông thường, tổng số lượt đăng ký cho một nguồn lực sẽ bằng tổng các nhiệm vụ của một hoặc nhiều tác vụ được chỉ định cho nguồn lực đó.</span><span class="sxs-lookup"><span data-stu-id="bb177-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="bb177-112">Tuy nhiên, Project Operations không đảm bảo sự thống nhất này.</span><span class="sxs-lookup"><span data-stu-id="bb177-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="bb177-113">Dạng xem **Điều hòa** cho Người quản lý dự án thấy các vị trí mà lượt đăng ký và nhiệm vụ của nguồn lực không thống nhất với nhau.</span><span class="sxs-lookup"><span data-stu-id="bb177-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
