---
title: Dự án và ước tính doanh số
description: Chủ đề này cung cấp thông tin về cách tận dụng lịch trình và ước tính trong quá trình bán hàng.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 87dc72b76ec4f88684ef2c702718e1ab631ff936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283934"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="3331a-103">Dự án và ước tính doanh số</span><span class="sxs-lookup"><span data-stu-id="3331a-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3331a-104">Trong quá trình bán hàng, bạn có thể tạo ước tính bán hàng bằng cách liên kết một dự án với báo giá bán hàng.</span><span class="sxs-lookup"><span data-stu-id="3331a-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="3331a-105">Bằng cách này, có thể ước tính xác định trong quá trình bán hàng để tận dụng việc lập lịch dự án và năng lực ước tính.</span><span class="sxs-lookup"><span data-stu-id="3331a-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="3331a-106">Sau khi quá trình bán hàng thành công, lịch trình đã dùng cho mục đích ước tính bán hàng có thể dùng làm cơ sở để sàng lọc thêm kế hoạch dự án.</span><span class="sxs-lookup"><span data-stu-id="3331a-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="3331a-107">Liên kết dự án với mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="3331a-107">Linking a project to a quote line</span></span>

<span data-ttu-id="3331a-108">Khi tạo một mô tả báo giá dựa trên dự án, bạn có thể tạo một dự án mới hoặc liên kết dự án hiện tại trên trang **Mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="3331a-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Biểu mẫu mô tả báo giá](media/project-8.png)
 
<span data-ttu-id="3331a-110">Khi tạo một dự án mới từ chi tiết mô tả báo giá, bạn có thể tận dụng các mẫu dự án.</span><span class="sxs-lookup"><span data-stu-id="3331a-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="3331a-111">Mẫu dự án là các dự án mẫu đại diện cho kế hoạch dự án và ước tính tài chính tiêu chuẩn tiêu biểu trong một tổ chức.</span><span class="sxs-lookup"><span data-stu-id="3331a-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="3331a-112">Mẫu dự án cũng đại diện cho các bản sao kế hoạch và ước tính dự án từ các dự án trước đó.</span><span class="sxs-lookup"><span data-stu-id="3331a-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Chi tiết dòng báo giá](media/project-9.png)
  
<span data-ttu-id="3331a-114">Khi tạo dự án từ báo giá, dự án tự động được liên kết với mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="3331a-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="3331a-115">Các thành phần của ước tính trong một dự án</span><span class="sxs-lookup"><span data-stu-id="3331a-115">Components of estimates in a project</span></span>

<span data-ttu-id="3331a-116">Một lịch trình cho phép bạn chia công việc thành các nhiệm vụ, duy trì một hệ thống cấp bậc của nhiệm vụ, xác định các nguồn lực cần thiết để hoàn thành nhiệm vụ và chỉ định ước tính của nhân lực cần thiết để hoàn thành nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="3331a-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="3331a-117">Bạn có thể xác định nhân công công việc và ước tính lịch trình bằng cách dùng các trường trên tab **Lịch trình** của trang **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="3331a-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="3331a-118">Vì bảng giá liên kết với dự án, ước tính tài chính được tính bằng cách dùng chi phí và giá bán được xác định trong bảng giá.</span><span class="sxs-lookup"><span data-stu-id="3331a-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="3331a-119">Nhập ước tính từ dự án vào báo giá</span><span class="sxs-lookup"><span data-stu-id="3331a-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="3331a-120">Sau khi xác định ước tính dự án, bạn có thể nhập các ước tính đó vào mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="3331a-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="3331a-121">Trên trang **Chi tiết mô tả báo giá**, hãy chọn **Nhập từ ước tính** trên ruy băng để tóm tắt ước tính dự án theo loại giao dịch, vai trò hoặc cấp nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="3331a-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]