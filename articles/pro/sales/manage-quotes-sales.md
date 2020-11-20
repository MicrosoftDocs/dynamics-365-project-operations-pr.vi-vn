---
title: Quản lý báo giá dự án
description: Chủ đề này cung cấp thông tin về các báo giá dự án.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177852"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="a3180-103">Quản lý báo giá dự án</span><span class="sxs-lookup"><span data-stu-id="a3180-103">Manage project quotes</span></span>

<span data-ttu-id="a3180-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a3180-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a3180-105">Trong Dynamics 365 Project Operations, báo giá dự án được thiết kế để giúp xây dựng các đề xuất cho công việc dự án.</span><span class="sxs-lookup"><span data-stu-id="a3180-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="a3180-106">Cấu trúc của báo giá dự án trong Project Operations được tạo cho các đề xuất dự án có các thành phần sau:</span><span class="sxs-lookup"><span data-stu-id="a3180-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="a3180-107">Mô tả báo giá xác định các thành phần riêng của công việc sẽ được trình bày như các thành phần cấp cao.</span><span class="sxs-lookup"><span data-stu-id="a3180-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="a3180-108">Thông tin chi tiết mô tả báo giá xác định và ước tính công việc cho từng thành phần cấp cao hoặc mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="a3180-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="a3180-109">Các ước tính về lịch trình hoặc ngày và các khía cạnh tài chính của công việc gắn liền với mô tả báo giá đó.</span><span class="sxs-lookup"><span data-stu-id="a3180-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="a3180-110">Các mô hình thầu và thành phần phải thanh toán được thiết lập cho mỗi mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="a3180-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="a3180-111">Thiết lập này giúp ước tính mức chênh lệch doanh thu, chi tiêu và lợi nhuận cho từng mô tả báo giá và báo giá tổng thể.</span><span class="sxs-lookup"><span data-stu-id="a3180-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="a3180-112">Xem tất cả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="a3180-112">View all project-based quotes</span></span>

<span data-ttu-id="a3180-113">Danh sách tất cả báo giá dự án có trên trang danh sách **Báo giá**.</span><span class="sxs-lookup"><span data-stu-id="a3180-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="a3180-114">Chuyển tới **Bán hàng** > **Báo giá**.</span><span class="sxs-lookup"><span data-stu-id="a3180-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="a3180-115">Danh sách tất cả các báo giá dự án của bạn trong hệ thống được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="a3180-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="a3180-116">Sử dụng **Bộ chuyển dạng xem** để chọn các chế độ đã lọc khác của báo giá.</span><span class="sxs-lookup"><span data-stu-id="a3180-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="a3180-117">Sử dụng tiêu chí bộ lọc tùy chỉnh, bạn có thể định cấu hình các dạng xem và tùy chọn điều hướng của riêng mình.</span><span class="sxs-lookup"><span data-stu-id="a3180-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="a3180-118">Có thể tạo hoặc xóa báo giá khỏi trang danh sách này hoặc các trang chi tiết.</span><span class="sxs-lookup"><span data-stu-id="a3180-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
