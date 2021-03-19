---
title: Ghi chú của nhà phát triển dành cho giai đoạn Phê duyệt
description: Chủ đề này cung cấp thông tin bổ sung của nhà phát triển về cách xử lý giai đoạn phê duyệt.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290295"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="d6a3e-103">Ghi chú của nhà phát triển dành cho giai đoạn Phê duyệt</span><span class="sxs-lookup"><span data-stu-id="d6a3e-103">Developer notes for Approvals</span></span>

<span data-ttu-id="d6a3e-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="d6a3e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d6a3e-105">Dynamics 365 Project Operations bao gồm logic xác thực đảm bảo chuyển bản ghi chính xác qua các giai đoạn được phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="d6a3e-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="d6a3e-106">Quá trình chuyển tiếp hồ sơ chính xác đảm bảo:</span><span class="sxs-lookup"><span data-stu-id="d6a3e-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="d6a3e-107">Tất cả các hàng hỗ trợ được tạo trong các bảng liên quan, chẳng hạn như nhật ký và thực tế.</span><span class="sxs-lookup"><span data-stu-id="d6a3e-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="d6a3e-108">Trước khi tiếp tục, người phê duyệt được đánh dấu trong dự án là **Người phê duyệt dự án**.</span><span class="sxs-lookup"><span data-stu-id="d6a3e-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]