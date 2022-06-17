---
title: Ghi chú của nhà phát triển dành cho giai đoạn Phê duyệt
description: Bài viết này cung cấp thông tin bổ sung cho nhà phát triển về cách làm việc với các phê duyệt.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924778"
---
# <a name="developer-notes-for-approvals"></a>Ghi chú của nhà phát triển dành cho giai đoạn Phê duyệt

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations bao gồm logic xác thực đảm bảo chuyển bản ghi chính xác qua các giai đoạn được phê duyệt. Quá trình chuyển tiếp hồ sơ chính xác đảm bảo: 

  - Tất cả các hàng hỗ trợ được tạo trong các bảng liên quan, chẳng hạn như nhật ký và thực tế.
  - Trước khi tiếp tục, người phê duyệt được đánh dấu trong dự án là **Người phê duyệt dự án**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]