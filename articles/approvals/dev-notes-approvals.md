---
title: Ghi chú của nhà phát triển dành cho giai đoạn Phê duyệt
description: Chủ đề này cung cấp thông tin bổ sung của nhà phát triển về cách xử lý giai đoạn phê duyệt.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579746"
---
# <a name="developer-notes-for-approvals"></a>Ghi chú của nhà phát triển dành cho giai đoạn Phê duyệt

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations bao gồm logic xác thực đảm bảo chuyển bản ghi chính xác qua các giai đoạn được phê duyệt. Quá trình chuyển tiếp hồ sơ chính xác đảm bảo: 

  - Tất cả các hàng hỗ trợ được tạo trong các bảng liên quan, chẳng hạn như nhật ký và thực tế.
  - Trước khi tiếp tục, người phê duyệt được đánh dấu trong dự án là **Người phê duyệt dự án**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]