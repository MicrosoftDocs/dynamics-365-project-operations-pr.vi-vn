---
title: Cung cấp dự toán công việc cho một dự án trong quá trình bán hàng
description: Làm cách nào để cung cấp ước tính công việc cho dự án trong quy trình bán hàng ở Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283574"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="15c3d-103">Cung cấp ước tính công việc cho dự án trong quy trình bán hàng (Project Service)</span><span class="sxs-lookup"><span data-stu-id="15c3d-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="15c3d-104">Trong quá trình bán hàng, bạn có thể tạo ước tính bán hàng từ đầu với mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="15c3d-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="15c3d-105">Các chức năng [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trong [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] cung cấp cách dự toán doanh số một cách khoa học và chính xác hơn bằng cách chia nhỏ mục công việc và kết hợp các thuộc tính có liên quan góp phần vào ước tính cho dự án trong cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="15c3d-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="15c3d-106">Sau khi giành được việc bán hàng, bạn có thể sử dụng cấu trúc phân tích công việc có liên quan trong kế hoạch, điều chỉnh khi cần để hoàn thành thành công dự án của bạn.</span><span class="sxs-lookup"><span data-stu-id="15c3d-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="15c3d-107">Liên kết dự án với mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="15c3d-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="15c3d-108">Khi tạo một mô tả báo giá dựa trên dự án, bạn có thể tạo một dự án mới từ mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="15c3d-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="15c3d-109">Sau đó, bạn có thể sử dụng mẫu dự án, là các kế hoạch tiêu chuẩn cấu hình sẵn và ước tính tài chính chung trong tổ chức của bạn hoặc bản sao kế hoạch dự án và ước tính từ dự án trước.</span><span class="sxs-lookup"><span data-stu-id="15c3d-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="15c3d-110">Khi bạn tạo một dự án, việc chọn một mẫu dự án sẽ cung cấp cơ sở điều chỉnh kế hoạch dự án, ước tính và yêu cầu vai trò.</span><span class="sxs-lookup"><span data-stu-id="15c3d-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="15c3d-111">Bằng cách tạo dự án của bạn từ báo giá, dự án tự động được kết hợp với mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="15c3d-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="15c3d-112">Thành phần ước tính của dự án</span><span class="sxs-lookup"><span data-stu-id="15c3d-112">Project estimate components</span></span>  
 <span data-ttu-id="15c3d-113">Cấu trúc phân tích công việc trong một dự án cung cấp cách để phân chia công việc thành các nhiệm vụ, duy trì một hệ thống phân cấp nhiệm vụ và gán ước tính nỗ lực cần thiết để hoàn thành mỗi nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="15c3d-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="15c3d-114">Bạn cũng có thể kết hợp các vai trò với một nhiệm vụ để chỉ ra một ước tính loại nguồn lực cần thiết để hoàn thành nhiệm vụ và lịch trình.</span><span class="sxs-lookup"><span data-stu-id="15c3d-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="15c3d-115">Cấu trúc phân tích công việc giúp bạn xác định nỗ lực làm việc và ước tính lịch trình.</span><span class="sxs-lookup"><span data-stu-id="15c3d-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="15c3d-116">Theo mặc định, dự án sử dụng bảng giá mặc định mà bạn đã xác định trước đó.</span><span class="sxs-lookup"><span data-stu-id="15c3d-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="15c3d-117">Chi phí và giá bán được xác định trong bảng giá giúp quyết định ước tính tài chính cho phân tích công việc của dự án.</span><span class="sxs-lookup"><span data-stu-id="15c3d-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="15c3d-118">Nếu dự án của bạn được liên kết với một báo giá và báo giá có bảng giá khác với bảng giá mặc định, bảng giá của báo giá được sử dụng cho ước tính tài chính.</span><span class="sxs-lookup"><span data-stu-id="15c3d-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="15c3d-119">Nhập ước tính từ dự án vào báo giá</span><span class="sxs-lookup"><span data-stu-id="15c3d-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="15c3d-120">Sau khi có ước tính dự án trong dự án, bạn có thể nhập những ước tính này vào mô tả báo giá:</span><span class="sxs-lookup"><span data-stu-id="15c3d-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="15c3d-121">Trong **Chi tiết mô tả báo giá**, bấm vào **Nhập từ ước tính**.</span><span class="sxs-lookup"><span data-stu-id="15c3d-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="15c3d-122">Chọn nhập ước tính dự án được tóm tắt theo loại giao dịch, vai trò hoặc cấp độ nút cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="15c3d-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="15c3d-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="15c3d-123">See Also</span></span>  
 [<span data-ttu-id="15c3d-124">Hướng dẫn của Quản lý Dự án</span><span class="sxs-lookup"><span data-stu-id="15c3d-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]