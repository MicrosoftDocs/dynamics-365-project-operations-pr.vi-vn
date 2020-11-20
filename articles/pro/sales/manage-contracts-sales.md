---
title: Quản lý hợp đồng dự án
description: Chủ đề này cung cấp thông tin về cách xem các hợp đồng dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177357"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="13301-103">Quản lý hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="13301-103">Manage project contracts</span></span>

<span data-ttu-id="13301-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="13301-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="13301-105">Các hợp đồng dự án trong Dynamics 365 Project Operations ghi lại và quản lý các cam kết đã thỏa thuận theo hợp đồng và các chi tiết thanh toán của dự án.</span><span class="sxs-lookup"><span data-stu-id="13301-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="13301-106">Cấu trúc của một hợp đồng dự án trong Project Operations được điều chỉnh cho công việc dựa trên dự án có các thành phần sau:</span><span class="sxs-lookup"><span data-stu-id="13301-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="13301-107">Mô tả hợp đồng xác định các thành phần riêng biệt của công việc sẽ được trình bày dưới dạng các thành phần cấp cao trên hóa đơn dự án.</span><span class="sxs-lookup"><span data-stu-id="13301-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="13301-108">Các chi tiết mô tả hợp đồng xác định và ước tính công việc cho từng thành phần cấp cao hoặc mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="13301-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="13301-109">Số liệu ước tính bao gồm lịch và các khía cạnh tài chính của công việc được liên kết với phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="13301-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="13301-110">Các mô hình hợp đồng và thành phần có thể tính phí được thiết lập cho từng mô tả hợp đồng giúp duy trì thỏa thuận thanh toán cho từng mô tả hợp đồng cũng như cả hợp đồng nói chung.</span><span class="sxs-lookup"><span data-stu-id="13301-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="13301-111">Xem tất cả các hợp đồng dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="13301-111">View all project-based contracts</span></span>

<span data-ttu-id="13301-112">Trang danh sách **Hợp đồng** hiển thị danh sách tất cả các hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="13301-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="13301-113">Chuyển đến **Bán hàng** > **Hợp đồng**.</span><span class="sxs-lookup"><span data-stu-id="13301-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="13301-114">Danh sách tất cả các Hợp đồng dự án của bạn có trong hệ thống sẽ hiển thị.</span><span class="sxs-lookup"><span data-stu-id="13301-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="13301-115">Chọn **Bộ chuyển dạng xem** (mũi tên thả xuống bên cạnh tên của dạng xem) để chọn các chế độ đã lọc khác.</span><span class="sxs-lookup"><span data-stu-id="13301-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="13301-116">Bạn có thể tạo dạng xem của riêng mình bằng các tiêu chí lọc tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="13301-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="13301-117">Các hợp đồng có thể được tạo hoặc xóa khỏi trang danh sách này hay các trang chi tiết.</span><span class="sxs-lookup"><span data-stu-id="13301-117">Contracts can be created or deleted from this list page or detail pages.</span></span>
