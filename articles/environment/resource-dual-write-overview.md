---
title: Tích hợp ghi kép của Project Operations
description: Chủ đề này cung cấp tổng quan về tích hợp ghi kép của Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998707"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="9f1e7-103">Tổng quan về tích hợp ghi kép của Project Operations</span><span class="sxs-lookup"><span data-stu-id="9f1e7-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="9f1e7-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="9f1e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9f1e7-105">Project Operations sử dụng [tính năng ghi kép](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) để đồng bộ hóa dữ liệu trên Microsoft Dataverse và Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9f1e7-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="9f1e7-106">Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa như một phần của tích hợp này giữa Dataverse và Tài chính.</span><span class="sxs-lookup"><span data-stu-id="9f1e7-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Tổng quan về luồng dữ liệu của Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="9f1e7-108">Project Operations trên Dataverse cung cấp giao diện người dùng (UI) hiện đại và khả năng mở rộng dễ dàng không mã/ít mã bằng cách sử dụng tính năng Power Platform.</span><span class="sxs-lookup"><span data-stu-id="9f1e7-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="9f1e7-109">Người quản lý dự án, Người quản lý nguồn lực, thành viên nhóm Dự án và các nhân viên văn phòng khác thực hiện các hoạt động của họ trong Project Operations trên Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9f1e7-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="9f1e7-110">Project Operations trong Tài chính cung cấp hỗ trợ kế toán dự án và ghi nhận doanh thu.</span><span class="sxs-lookup"><span data-stu-id="9f1e7-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="9f1e7-111">Project Operations kết hợp với khuôn khổ tài chính trong Tài chính để tính thuế bán hàng, tỷ giá hối đoái, báo cáo lĩnh vực tài chính, v.v.</span><span class="sxs-lookup"><span data-stu-id="9f1e7-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="9f1e7-112">Kinh nghiệm của kế toán viên Dự án chủ yếu dựa trên Tài chính.</span><span class="sxs-lookup"><span data-stu-id="9f1e7-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="9f1e7-113">Tích hợp Project Operations bao gồm tích hợp thành phần sau:</span><span class="sxs-lookup"><span data-stu-id="9f1e7-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="9f1e7-114">Tích hợp dữ liệu cấu hình và thiết lập Project Operations</span><span class="sxs-lookup"><span data-stu-id="9f1e7-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="9f1e7-115">Giá trị ước tính và thực tế của dự án</span><span class="sxs-lookup"><span data-stu-id="9f1e7-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="9f1e7-116">Hóa đơn dự án</span><span class="sxs-lookup"><span data-stu-id="9f1e7-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="9f1e7-117">Quản lý chi phí</span><span class="sxs-lookup"><span data-stu-id="9f1e7-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="9f1e7-118">Hóa đơn của nhà cung cấp</span><span class="sxs-lookup"><span data-stu-id="9f1e7-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
