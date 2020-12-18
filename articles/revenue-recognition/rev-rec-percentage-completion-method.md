---
title: Dự án ước tính doanh thu giá cố định
description: Chủ đề này cung cấp thông tin về doanh thu giá cố định trong dự án.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531594"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="e435e-103">Dự án ước tính doanh thu giá cố định</span><span class="sxs-lookup"><span data-stu-id="e435e-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="e435e-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="e435e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e435e-105">Khi bạn tạo một dòng hợp đồng với những thuộc tính sau trong Dynamics 365 Project Operations trên Microsoft Dataverse, hệ thống sẽ tự động tạo dự án ước tính doanh thu giá cố định.</span><span class="sxs-lookup"><span data-stu-id="e435e-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="e435e-106">Thông tin trong dự án này sẽ dựa trên:</span><span class="sxs-lookup"><span data-stu-id="e435e-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="e435e-107">Phương thức thanh toán theo giá cố định.</span><span class="sxs-lookup"><span data-stu-id="e435e-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="e435e-108">Dự án liên kết.</span><span class="sxs-lookup"><span data-stu-id="e435e-108">An associated project.</span></span>
  - <span data-ttu-id="e435e-109">Ít nhất một mốc được xác định trên tab **Lịch trình hóa đơn** của trang **Dòng hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="e435e-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="e435e-110">Xem xét dự án ước tính doanh thu theo giá cố định</span><span class="sxs-lookup"><span data-stu-id="e435e-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="e435e-111">Để xem xét dự án ước tính doanh thu theo giá cố định, hãy hoàn tất các bước sau:</span><span class="sxs-lookup"><span data-stu-id="e435e-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="e435e-112">Trong môi trường Dynamics 365 Finance, hãy đi tới **Quản lý dự án và kế toán** > **Dự án** > **Dự án ước tính doanh thu theo giá cố định**.</span><span class="sxs-lookup"><span data-stu-id="e435e-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="e435e-113">Chọn dự án bạn muốn xem rồi bấm đúp vào **ID dự án ước tính** để mở bản ghi và xem xét chi tiết dự án.</span><span class="sxs-lookup"><span data-stu-id="e435e-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="e435e-114">Mở rộng tab **Dự án**. Bạn sẽ thấy một dự án trong lưới **Dự án đã chọn**.</span><span class="sxs-lookup"><span data-stu-id="e435e-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="e435e-115">Hệ thống sẽ dùng dự án này làm dự án mặc định vì đó là dự án liên kết với dòng hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="e435e-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="e435e-116">Để thay đổi mối liên kết này, hãy chọn các dự án bổ sung rồi thêm chúng vào lưới **Dự án đã chọn**.</span><span class="sxs-lookup"><span data-stu-id="e435e-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="e435e-117">Nếu có nhiều dự án được chọn trong lưới này, mức phần trăm hoàn thành dự án và ước tính doanh thu sẽ được tính toán cùng lúc cho tất cả dự án đã chọn.</span><span class="sxs-lookup"><span data-stu-id="e435e-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="e435e-118">Bạn có thể thiết lập chi phí dự án, hồ sơ doanh thu, mẫu chi phí và mã chu kỳ theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="e435e-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="e435e-119">Nếu không đặt được theo cách thủ công, giá trị ước tính mặc định trong lần tính toán đầu tiên của dự án sẽ áp dụng các quy tắc như trong cấu hình hồ sơ doanh thu và chi phí dự án.</span><span class="sxs-lookup"><span data-stu-id="e435e-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

