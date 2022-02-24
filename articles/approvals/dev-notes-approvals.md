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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483974"
---
# <a name="developer-notes-for-approvals"></a>Ghi chú của nhà phát triển dành cho giai đoạn Phê duyệt

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations bao gồm logic xác thực giúp đảm bảo quá trình chuyển tiếp hồ sơ chính xác qua các giai đoạn phê duyệt. Quá trình chuyển tiếp hồ sơ chính xác đảm bảo: 

  - Tất cả các hàng hỗ trợ được tạo trong các bảng liên quan, chẳng hạn như nhật ký và thực tế.
  - Trước khi tiếp tục, người phê duyệt được đánh dấu trong dự án là **Người phê duyệt dự án**.
