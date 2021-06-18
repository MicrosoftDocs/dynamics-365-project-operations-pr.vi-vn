---
title: Đơn đặt hàng dự án cho dự án thời gian và vật tư
description: Chủ đề này giải thích cách tạo đơn đặt hàng dự án đối với dự án thời gian và vật tư.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009687"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="d769a-103">Đơn đặt hàng dự án cho dự án thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="d769a-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d769a-104">Chủ đề này mô tả cách tạo đơn đặt hàng cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="d769a-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="d769a-105">Đơn đặt hàng chỉ có thể được tạo cho các dự án loại **thời gian và vật tư**.</span><span class="sxs-lookup"><span data-stu-id="d769a-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="d769a-106">Nếu một dự án thời gian và vật tư có nhiều nguồn tài trợ trong hợp đồng dự án, bạn phải bật tham số **Cho phép đơn đặt hàng đối với các dự án có nhiều nguồn tài trợ** trên trang **Tham số quản lý dự án và kế toán**.</span><span class="sxs-lookup"><span data-stu-id="d769a-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="d769a-107">Tính năng hỗ trợ cho các đơn đặt hàng dự án có nhiều nguồn tài trợ được cung cấp từ bản phát hành ứng dụng 10.0.2 trở lên.</span><span class="sxs-lookup"><span data-stu-id="d769a-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="d769a-108">Tham số cho phép hỗ trợ đơn đặt hàng dự án có nhiều nguồn tài trợ sẽ bị xóa trong đợt phát hành tháng 4 năm 2020, sau đó chức năng này sẽ luôn được bật.</span><span class="sxs-lookup"><span data-stu-id="d769a-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="d769a-109">Bạn có thể tạo đơn đặt hàng dựa trên dự án theo hai cách:</span><span class="sxs-lookup"><span data-stu-id="d769a-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="d769a-110">Truy cập vào chính dự án.</span><span class="sxs-lookup"><span data-stu-id="d769a-110">Go to the project itself.</span></span> <span data-ttu-id="d769a-111">Trên Ngăn hành động, chọn **Quản lý > Nhiệm vụ mặt hàng > Đơn đặt hàng**.</span><span class="sxs-lookup"><span data-stu-id="d769a-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="d769a-112">Thông tin dự án sẽ mặc định theo đơn đặt hàng từ dự án.</span><span class="sxs-lookup"><span data-stu-id="d769a-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="d769a-113">Nếu hợp đồng dự án có nhiều nguồn tài trợ, bạn sẽ cần chọn nguồn tài trợ để thiết lập khách hàng cho đơn đặt hàng.</span><span class="sxs-lookup"><span data-stu-id="d769a-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="d769a-114">Nếu chỉ có một nguồn tài trợ cho dự án, khách hàng sẽ được tự động thiết lập.</span><span class="sxs-lookup"><span data-stu-id="d769a-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="d769a-115">Đi đến trang danh sách **Tất cả đơn đặt hàng** và tạo đơn đặt hàng mới.</span><span class="sxs-lookup"><span data-stu-id="d769a-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="d769a-116">Bạn sẽ cần phải chọn dự án cho đơn đặt hàng.</span><span class="sxs-lookup"><span data-stu-id="d769a-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="d769a-117">Sau khi dự án được chọn, khách hàng sẽ được thiết lập từ nguồn tài trợ hoặc bạn sẽ cần chọn nguồn tài trợ nếu hợp đồng dự án có nhiều nguồn vốn.</span><span class="sxs-lookup"><span data-stu-id="d769a-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]