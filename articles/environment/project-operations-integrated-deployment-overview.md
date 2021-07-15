---
title: Tổng quan về triển khai Project Operations cho các tình huống dựa trên nguồn lực/hàng không trữ kho
description: Chủ đề này cung cấp thông tin về loại hình triển khai, Project Operations cho các tình huống dựa trên nguồn lực/hàng không trữ kho.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 3648bf6c5e00fe701f309392bd09819f84bf574d
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368727"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="e46e5-103">Tổng quan về triển khai Project Operations cho các tình huống dựa trên nguồn lực/hàng không trữ kho</span><span class="sxs-lookup"><span data-stu-id="e46e5-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="e46e5-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="e46e5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e46e5-105">Loại hình triển khai, Dynamics 365 Project Operations cho các trường hợp dựa trên nguồn lực/hàng không trữ kho có các tính năng sau dành cho những công ty dựa trên dự án:</span><span class="sxs-lookup"><span data-stu-id="e46e5-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="e46e5-106">Lập kế hoạch dự án bằng Microsoft Project dành cho web</span><span class="sxs-lookup"><span data-stu-id="e46e5-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="e46e5-107">Định giá và chi phí đa chiều cho nguồn lực lao động</span><span class="sxs-lookup"><span data-stu-id="e46e5-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="e46e5-108">Định giá dựa trên thể loại cho các thể loại chi phí</span><span class="sxs-lookup"><span data-stu-id="e46e5-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="e46e5-109">Quản lý bán hàng dựa trên dự án bằng các tính năng của Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="e46e5-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="e46e5-110">Universal resource scheduling hợp với các ứng dụng khác như Dynamics 365 Field Service và Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="e46e5-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="e46e5-111">Theo dõi thời gian và tiến độ dự án</span><span class="sxs-lookup"><span data-stu-id="e46e5-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="e46e5-112">Giải pháp quản lý chi phí cơ bản và đầy đủ đối với các chi phí thuộc dự án và không thuộc dự án, bao gồm cả ghi lại biên nhận bằng cách sử dụng các tính năng OCR</span><span class="sxs-lookup"><span data-stu-id="e46e5-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="e46e5-113">Việc lập hóa đơn mở rộng từ nền tảng ước giá cho đến nền tảng dành cho khách hàng và được hỗ trợ bởi thuế bán hàng cấp doanh nghiệp cũng như hệ thống tỷ giá hối đoái có hiệu lực theo ngày.</span><span class="sxs-lookup"><span data-stu-id="e46e5-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="e46e5-114">Chi phí dự án có thể đặt cấu hình, hồ sơ doanh thu và quy tắc cho hoạt động kế toán và khoản dồn tích trong công việc đang thực hiện (WIP)</span><span class="sxs-lookup"><span data-stu-id="e46e5-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="e46e5-115">Ghi nhận doanh thu dự án</span><span class="sxs-lookup"><span data-stu-id="e46e5-115">Project revenue recognition</span></span>
- <span data-ttu-id="e46e5-116">Khả năng mở rộng thông qua Power Platform</span><span class="sxs-lookup"><span data-stu-id="e46e5-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="e46e5-117">Loại hình triển khai này giúp mở rộng chức năng được các ứng dụng Dynamics 365 Finance và Dynamics 365 Supply Chain Management cung cấp.</span><span class="sxs-lookup"><span data-stu-id="e46e5-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="e46e5-118">Nên chọn loại hình triển khai này nếu điều kỳ vọng ở Project Operations là sử dụng toàn bộ vòng đời của dự án có các yêu cầu sau:</span><span class="sxs-lookup"><span data-stu-id="e46e5-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="e46e5-119">Khả năng quản lý bán hàng dựa trên dự án thông qua các loại hình bán hàng khác bằng các tính năng trong ứng dụng Sales.</span><span class="sxs-lookup"><span data-stu-id="e46e5-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="e46e5-120">Một hệ thống quản lý dự án tích hợp giúp quản lý các dự án nội bộ và dự án phải thanh toán đối với các vấn đề liên quan đến lịch trình và tài chính, từ bán hàng cho đến kế toán của dự án.</span><span class="sxs-lookup"><span data-stu-id="e46e5-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="e46e5-121">Một hệ thống quản lý chi phí bao gồm việc thực thi chính sách và bồi hoàn để theo dõi các chi phí thuộc dự án và không thuộc dự án.</span><span class="sxs-lookup"><span data-stu-id="e46e5-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="e46e5-122">Yêu cầu một công cụ hiệu quả cho tỷ giá hối đoái và thuế bán hàng cấp doanh nghiệp để tạo hóa đơn dành cho khách hàng của dự án.</span><span class="sxs-lookup"><span data-stu-id="e46e5-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="e46e5-123">Hệ thống ghi nhận doanh thu và kế toán của dự án tuân thủ Tiêu chuẩn báo cáo tài chính quốc tế (IFRS).</span><span class="sxs-lookup"><span data-stu-id="e46e5-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="e46e5-124">Các ứng dụng Finance hoặc Supply Chain Management và sự tích hợp các giao dịch dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="e46e5-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]