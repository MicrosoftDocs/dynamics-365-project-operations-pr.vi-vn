---
title: Ghi chú của nhà phát triển dành cho giai đoạn Phê duyệt
description: Chủ đề này cung cấp thông tin bổ sung của nhà phát triển về cách xử lý giai đoạn phê duyệt.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996817"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="2f342-103">Ghi chú của nhà phát triển dành cho giai đoạn Phê duyệt</span><span class="sxs-lookup"><span data-stu-id="2f342-103">Developer notes for Approvals</span></span>

<span data-ttu-id="2f342-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="2f342-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2f342-105">Dynamics 365 Project Operations bao gồm logic xác thực đảm bảo chuyển bản ghi chính xác qua các giai đoạn được phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="2f342-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="2f342-106">Quá trình chuyển tiếp hồ sơ chính xác đảm bảo:</span><span class="sxs-lookup"><span data-stu-id="2f342-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="2f342-107">Tất cả các hàng hỗ trợ được tạo trong các bảng liên quan, chẳng hạn như nhật ký và thực tế.</span><span class="sxs-lookup"><span data-stu-id="2f342-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="2f342-108">Trước khi tiếp tục, người phê duyệt được đánh dấu trong dự án là **Người phê duyệt dự án**.</span><span class="sxs-lookup"><span data-stu-id="2f342-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]