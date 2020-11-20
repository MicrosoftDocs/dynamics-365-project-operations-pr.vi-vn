---
title: Cập nhật giá trị ước tính lúc hoàn thành
description: Chủ đề này cung cấp thông tin về việc cập nhật dự đoán về công sức dành cho một dự án.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127229"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="a7826-103">Cập nhật giá trị ước tính lúc hoàn thành</span><span class="sxs-lookup"><span data-stu-id="a7826-103">Update estimate at completion</span></span>

<span data-ttu-id="a7826-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a7826-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a7826-105">Người quản lý dự án thường có thể sửa đổi ước tính ban đầu cho một nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="a7826-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="a7826-106">Lên kế hoạch lại dự án là khả năng ước tính của người quản lý dự án, dựa trên hiện trạng dự án.</span><span class="sxs-lookup"><span data-stu-id="a7826-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="a7826-107">Tuy nhiên, người quản lý dự án không nên thay đổi các chỉ số ban đầu vì chỉ số ban đầu của dự án đại diện cho nguồn tin cậy đã được thiết lập đối với lịch trình và ước tính chi phí của dự án. Tất cả bên liên quan của dự án phải đồng ý với các chỉ số ban đầu.</span><span class="sxs-lookup"><span data-stu-id="a7826-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="a7826-108">Người quản lý dự án có thể lên kế hoạch lại nhân công cho nhiệm vụ bằng 2 cách:</span><span class="sxs-lookup"><span data-stu-id="a7826-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="a7826-109">Thay thế mục ước tính hoàn thành (ETC) mặc định bằng ước tính mới của nhân công còn lại thực tế trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="a7826-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="a7826-110">Thay thế phần trăm tiến trình mặc định bằng ước tính mới của tiến trình đúng trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="a7826-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="a7826-111">Mỗi cách tiếp cận này mang đến một phép tính lại ETC, EAC (ước tính hoàn thành) và phần trăm tiến trình của nhiệm vụ cũng như chênh lệch nhân công dự kiến trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="a7826-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="a7826-112">EAC, ETC và phần trăm tiến trình trên các nhiệm vụ tóm tắt được tính toán lại và cung cấp dự kiến mới về chênh lệch nhân công.</span><span class="sxs-lookup"><span data-stu-id="a7826-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
