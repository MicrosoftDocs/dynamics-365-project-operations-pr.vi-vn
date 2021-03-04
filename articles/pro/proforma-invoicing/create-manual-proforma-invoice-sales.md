---
title: Tạo hóa đơn ước giá thủ công - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc tạo hóa đơn ước giá thủ công trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764529"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="e3b3b-103">Tạo hóa đơn ước giá thủ công - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="e3b3b-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="e3b3b-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="e3b3b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e3b3b-105">Trong Dynamics 365 Project Operations, hóa đơn ước giá có thể được tạo theo cách thủ công nếu cần.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="e3b3b-106">Bạn có thể tạo thủ công hóa đơn ước giá từ trang danh sách **Hợp đồng dự án** hoặc từ trang chi tiết **Hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="e3b3b-107">Trang danh sách Hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="e3b3b-107">Project Contracts list page</span></span>

<span data-ttu-id="e3b3b-108">Ở trang danh sách **Hợp đồng dự án**, chọn một hoặc nhiều hợp đồng dự án và tạo hóa đơn cho tất cả các bản ghi được chọn.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="e3b3b-109">Hệ thống kiểm tra xem hợp đồng dự án nào đã chọn có mục tồn đọng **Đã sẵn sàng để lập hóa đơn** được đề ngày trước ngày hôm nay.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="e3b3b-110">Từ những hợp đồng đó, hệ thống tạo ra hóa đơn ước giá nháp.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="e3b3b-111">Nếu hợp đồng dự án có nhiều khách hàng, thì mỗi khách hàng có thể được tạo một hóa đơn và có thể có nhiều hóa đơn cho một hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="e3b3b-112">Tất cả các hóa đơn dự án đã tạo đều có sẵn trên trang **Hóa đơn** ở phần **Thanh toán** của khu vực **Bán hàng**.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="e3b3b-113">Trang chi tiết Hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="e3b3b-113">Project Contract details page</span></span>

<span data-ttu-id="e3b3b-114">Hóa đơn ước giá cũng có thể được tạo từ trang chi tiết **Hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="e3b3b-115">Hệ thống xác minh hợp đồng dự án có mục tồn đọng **Đã sẵn sàng để lập hóa đơn** được đề ngày trước ngày hôm nay.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="e3b3b-116">Từ các hợp đồng này, hệ thống tạo hóa đơn ước giá nháp dựa trên số lượng khách hàng trên mỗi mục mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="e3b3b-117">Khi có một hóa đơn ước giá được tạo,trang **Hóa đơn** sẽ mở ra.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="e3b3b-118">Nếu có nhiều hóa đơn được tạo cho hợp đồng dự án đó, trang danh sách **Hóa đơn** mở ra để hiển thị tất cả các hóa đơn đã tạo.</span><span class="sxs-lookup"><span data-stu-id="e3b3b-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
