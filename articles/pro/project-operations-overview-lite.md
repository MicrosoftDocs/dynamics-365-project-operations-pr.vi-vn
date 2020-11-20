---
title: Tổng quan về triển khai Lite
description: Chủ đề này cung cấp thông tin về việc triển khai Lite của Dynamics 365 Project Operations.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b66b3656d1ef5266ede1f62657dbe9b8a63c863a
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365670"
---
# <a name="lite-deployment-overview"></a><span data-ttu-id="95e4a-103">Tổng quan về triển khai Lite</span><span class="sxs-lookup"><span data-stu-id="95e4a-103">Lite deployment overview</span></span>

<span data-ttu-id="95e4a-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="95e4a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="95e4a-105">Loại hình triển khai Lite của Dynamics 365 Project Operations có các tính năng sau cho những công ty dựa trên dự án:</span><span class="sxs-lookup"><span data-stu-id="95e4a-105">The Lite deployment type of Dynamics 365 Project Operations has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="95e4a-106">Lập kế hoạch dự án bằng Microsoft Project dành cho web</span><span class="sxs-lookup"><span data-stu-id="95e4a-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="95e4a-107">Định giá và chi phí đa chiều cho nguồn lực lao động</span><span class="sxs-lookup"><span data-stu-id="95e4a-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="95e4a-108">Định giá dựa trên thể loại cho các thể loại chi phí</span><span class="sxs-lookup"><span data-stu-id="95e4a-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="95e4a-109">Quản lý bán hàng dựa trên dự án bằng các tính năng của Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="95e4a-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="95e4a-110">Universal resource scheduling hợp với các ứng dụng khác như Dynamics 365 Field Service và Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="95e4a-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="95e4a-111">Theo dõi thời gian và tiến độ dự án</span><span class="sxs-lookup"><span data-stu-id="95e4a-111">Project progress and time tracking</span></span>
- <span data-ttu-id="95e4a-112">Theo dõi chi phí cơ bản cho các chi phí dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="95e4a-112">Basic expense tracking for project-based expenses</span></span>
- <span data-ttu-id="95e4a-113">Hóa đơn ước giá có thể được xem xét và gửi đến hệ thống tài chính để xử lý</span><span class="sxs-lookup"><span data-stu-id="95e4a-113">Proforma invoicing that can be reviewed and sent to a financial system for processing</span></span>
- <span data-ttu-id="95e4a-114">Khả năng mở rộng thông qua Power Platform</span><span class="sxs-lookup"><span data-stu-id="95e4a-114">Extensibility through the Power Platform</span></span>

<span data-ttu-id="95e4a-115">Sử dụng loại hình triển khai này nếu điều bạn kỳ vọng ở Project Operations là sử dụng toàn bộ vòng đời của dự án, bao gồm cả những yêu cầu sau:</span><span class="sxs-lookup"><span data-stu-id="95e4a-115">Use this deployment type if your expectation from Project Operations is to use the full project lifecycle, including the following requirements:</span></span>

- <span data-ttu-id="95e4a-116">Khả năng quản lý bán hàng dựa trên dự án thông qua các loại hình bán hàng khác bằng các tính năng trong ứng dụng Sales.</span><span class="sxs-lookup"><span data-stu-id="95e4a-116">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="95e4a-117">Một hệ thống tích hợp giúp quản lý các dự án nội bộ và dự án phải thanh toán đối với các vấn đề liên quan đến lịch trình và tài chính, từ bán hàng cho đến lập hóa đơn của dự án.</span><span class="sxs-lookup"><span data-stu-id="95e4a-117">An integrated system that manages internal and billable projects for schedules and financials from project sales to invoicing.</span></span>
- <span data-ttu-id="95e4a-118">Hoạch định nguồn lực doanh nghiệp bên thứ ba (Hệ thống kế toán tài chính/ERP để tích hợp với Project Operations).</span><span class="sxs-lookup"><span data-stu-id="95e4a-118">A third-party Enterprise resource planning (ERP/Financial accounting system to integrate with Project Operations.</span></span>
- <span data-ttu-id="95e4a-119">Một hệ thống bên thứ ba để xử lý các khoản thuế bán hàng, tỷ giá hối đoái, hoàn trả chi phí và chi phí không thuộc dự án.</span><span class="sxs-lookup"><span data-stu-id="95e4a-119">A third-party system to work with sales taxes, exchange rates, expense reimbursements, and non-project expenses.</span></span>
