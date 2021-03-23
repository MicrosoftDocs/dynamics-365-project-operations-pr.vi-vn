---
title: Tổng quan về lập hóa đơn liên công ty
description: Chủ đề này cung cấp thông tin và ví dụ về cách lập hóa đơn liên công ty cho các dự án.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287354"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="6e08f-103">Tổng quan về lập hóa đơn liên công ty</span><span class="sxs-lookup"><span data-stu-id="6e08f-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="6e08f-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="6e08f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6e08f-105">Tổ chức của bạn có thể có nhiều bộ phận, công ty con và pháp nhân khác chuyển sản phẩm và dịch vụ cho nhau trong các dự án.</span><span class="sxs-lookup"><span data-stu-id="6e08f-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="6e08f-106">Pháp nhân cung cấp sản phẩm hoặc dịch vụ được gọi là *pháp nhân cho thuê*.</span><span class="sxs-lookup"><span data-stu-id="6e08f-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="6e08f-107">Pháp nhân nhận sản phẩm hoặc dịch vụ được gọi là *pháp nhân đi thuê*.</span><span class="sxs-lookup"><span data-stu-id="6e08f-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="6e08f-108">Hình sau minh họa trường hợp thường gặp, đó là khi Contoso Robotics USA (pháp nhân đi thuê) và Contoso Robotics UK (pháp nhân cho thuê) chia sẻ nguồn lực để thực hiện dự án cho khách hàng Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="6e08f-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="6e08f-109">Trong tình huống này, Contoso Robotics USA đã ký hợp đồng thực hiện công việc cho Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="6e08f-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Lập hóa đơn liên công ty](./media/IntercompanyScenario.png) 

<span data-ttu-id="6e08f-111">Dynamics 365 Project Operations dùng quy trình sau để xử lý các giao dịch liên công ty:</span><span class="sxs-lookup"><span data-stu-id="6e08f-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="6e08f-112">Nguồn lực của pháp nhân cho thuê ghi lại các giao dịch thời gian hoặc chi phí liên công ty bằng cách đăng ký thời gian và chi phí đối với các dự án trong pháp nhân đi thuê.</span><span class="sxs-lookup"><span data-stu-id="6e08f-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="6e08f-113">Giá thời gian và chi phí được ghi lại trong công ty cho thuê bằng cách dùng bảng giá chi phí đơn vị của công ty đi thuê.</span><span class="sxs-lookup"><span data-stu-id="6e08f-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="6e08f-114">Giao dịch bán hàng liên công ty chưa thanh toán được ghi lại trong công ty cho thuê bằng cách dùng bảng giá chi phí đơn vị của công ty đi thuê.</span><span class="sxs-lookup"><span data-stu-id="6e08f-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="6e08f-115">Doanh thu chưa thanh toán được ghi lại trong công ty đi thuê bằng cách dùng bảng giá bán hàng theo hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="6e08f-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="6e08f-116">Khách hàng có thể được lập hóa đơn khi doanh thu chưa thanh toán được ghi lại.</span><span class="sxs-lookup"><span data-stu-id="6e08f-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="6e08f-117">Khách hàng không phải đợi đến khi quy trình xử lý hóa đơn liên công ty hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="6e08f-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="6e08f-118">Hóa đơn khách hàng liên công ty được tạo theo định kỳ trong công ty cho thuê.</span><span class="sxs-lookup"><span data-stu-id="6e08f-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="6e08f-119">Các hóa đơn được tạo theo cách thủ công hoặc bằng cách dùng quy trình tự động hóa theo định kỳ.</span><span class="sxs-lookup"><span data-stu-id="6e08f-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="6e08f-120">Bạn có thể tạo một hóa đơn riêng lẻ cho từng pháp nhân đi thuê hoặc tạo các hóa đơn tách biệt theo dự án.</span><span class="sxs-lookup"><span data-stu-id="6e08f-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="6e08f-121">Khi hóa đơn khách hàng liên công ty được đăng trong pháp nhân cho thuê, hóa đơn nhà cung cấp tương ứng đang ở trạng thái chờ xử lý sẽ được tạo trong pháp nhân đi thuê.</span><span class="sxs-lookup"><span data-stu-id="6e08f-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="6e08f-122">Các chi phí trong hóa đơn nhà cung cấp đang chờ xử lý sẽ được ghi lại vào sổ cái phụ của dự án khi hóa đơn đó được đăng.</span><span class="sxs-lookup"><span data-stu-id="6e08f-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="6e08f-123">Sơ đồ sau minh họa quy trình lập hóa đơn liên công ty vì quy trình này có liên quan đến các sự kiện kế toán và những lần đăng dự kiến vào sổ cái chung.</span><span class="sxs-lookup"><span data-stu-id="6e08f-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Quy trình liên công ty](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="6e08f-125">Tài nguyên bổ sung</span><span class="sxs-lookup"><span data-stu-id="6e08f-125">Additional resources</span></span>

- [<span data-ttu-id="6e08f-126">Đặt cấu hình hoạt động lập hóa đơn liên công ty</span><span class="sxs-lookup"><span data-stu-id="6e08f-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="6e08f-127">Ghi lại giao dịch liên công ty</span><span class="sxs-lookup"><span data-stu-id="6e08f-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="6e08f-128">Lập hóa đơn cho nhà cung cấp và khách hàng liên công ty</span><span class="sxs-lookup"><span data-stu-id="6e08f-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]