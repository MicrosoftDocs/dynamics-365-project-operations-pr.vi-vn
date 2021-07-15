---
title: Tổng quan về việc triển khai Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất
description: Chủ đề này cung cấp thông tin về loại hình triển khai, Project Operations cho các tình huống dựa trên sản xuất/hàng trữ kho.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 71fd9d3ae30147c3c03202a54f74477a95838eb9
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369537"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="2fe7e-103">Tổng quan về việc triển khai Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất</span><span class="sxs-lookup"><span data-stu-id="2fe7e-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="2fe7e-104">_**Áp dụng cho:** Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_</span><span class="sxs-lookup"><span data-stu-id="2fe7e-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="2fe7e-105">Loại hình triển khai này mang lại các khả năng sau cho các công ty dựa trên dự án:</span><span class="sxs-lookup"><span data-stu-id="2fe7e-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="2fe7e-106">Lập kế hoạch dự án bằng cách sử dụng [Cấu trúc phân tích công việc](work-breakdown-structures.md)</span><span class="sxs-lookup"><span data-stu-id="2fe7e-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="2fe7e-107">Mua và tiêu thụ hàng tồn kho cho các dự án</span><span class="sxs-lookup"><span data-stu-id="2fe7e-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="2fe7e-108">Quản lý bán hàng dựa trên dự án bằng cách sử dụng mô-đun **Bán hàng và tiếp thị** trong ứng dụng Dynamics 365 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2fe7e-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="2fe7e-109">Định giá dự án và chi phí bằng cách sử dụng cấu hình tỷ lệ hóa đơn và tỷ lệ chi phí trong ứng dụng Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2fe7e-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="2fe7e-110">Quản lý nguồn lực của các dự án trong ứng dụng Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2fe7e-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="2fe7e-111">Theo dõi thời gian và tiến độ của dự án trong ứng dụng Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2fe7e-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="2fe7e-112">Giải pháp quản lý chi phí cơ bản đối với các chi phí thuộc dự án và không thuộc dự án có ghi lại biên nhận bằng cách sử dụng các tính năng OCR</span><span class="sxs-lookup"><span data-stu-id="2fe7e-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="2fe7e-113">Lập hóa đơn bằng cách sử dụng hệ thống liên quan đến thuế bán hàng cấp doanh nghiệp và tỷ giá hối đoái có hiệu lực theo ngày</span><span class="sxs-lookup"><span data-stu-id="2fe7e-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="2fe7e-114">Các nhóm dự án có thể đặt cấu hình cho các khoản cộng dồn và hoạt động kế toán WIP</span><span class="sxs-lookup"><span data-stu-id="2fe7e-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="2fe7e-115">Ghi nhận doanh thu dự án</span><span class="sxs-lookup"><span data-stu-id="2fe7e-115">Project revenue recognition</span></span>

<span data-ttu-id="2fe7e-116">Loại hình triển khai này cũng giúp mở rộng chức năng được các ứng dụng Dynamics 365 Finance và Dynamics 365 Supply Chain Management cung cấp.</span><span class="sxs-lookup"><span data-stu-id="2fe7e-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="2fe7e-117">Chọn loại hình triển khai này để sử dụng Dynamics 365 Project Operations trong toàn bộ vòng đời dự án, bao gồm cả những yêu cầu quan trọng sau:</span><span class="sxs-lookup"><span data-stu-id="2fe7e-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="2fe7e-118">Một Hệ thống quản lý dự án mở rộng quản lý các hạng mục đã kiểm kê và chi phí công việc/đơn đặt hàng sản xuất cho các dự án nội bộ và phải thanh toán đối với các vấn đề về lịch trình và tài chính.</span><span class="sxs-lookup"><span data-stu-id="2fe7e-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="2fe7e-119">Tổ chức đã có các ứng dụng Dynamics 365 Finance hoặc Dynamics 365 Supply Chain and Manufacturing và việc tích hợp các giao dịch dựa trên dự án sẽ đơn giản hóa nhu cầu truy cập và báo cáo dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="2fe7e-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="2fe7e-120">Một Hệ thống quản lý chi phí đầy đủ chức năng, bao gồm việc thực thi chính sách và bồi hoàn để theo dõi các chi phí thuộc dự án và không thuộc dự án.</span><span class="sxs-lookup"><span data-stu-id="2fe7e-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="2fe7e-121">Một công cụ cho tỷ giá hối đoái và thuế bán hàng cấp doanh nghiệp để tạo hóa đơn dành cho khách hàng của dự án.</span><span class="sxs-lookup"><span data-stu-id="2fe7e-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="2fe7e-122">Hệ thống ghi nhận doanh thu và kế toán của dự án tuân thủ Tiêu chuẩn báo cáo tài chính quốc tế (IFRS).</span><span class="sxs-lookup"><span data-stu-id="2fe7e-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]