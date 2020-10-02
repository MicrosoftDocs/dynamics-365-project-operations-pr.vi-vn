---
title: Cập nhật giá trị ước tính lúc hoàn thành
description: Chủ đề này cung cấp thông tin về việc cập nhật dự đoán về công sức dành cho một dự án.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897792"
---
# <a name="update-estimate-at-completion"></a>Cập nhật giá trị ước tính lúc hoàn thành

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Người quản lý dự án thường có thể sửa đổi ước tính ban đầu cho một nhiệm vụ. Lên kế hoạch lại dự án là khả năng ước tính của người quản lý dự án, dựa trên hiện trạng dự án. Tuy nhiên, người quản lý dự án không nên thay đổi các chỉ số ban đầu vì chỉ số ban đầu của dự án đại diện cho nguồn tin cậy đã được thiết lập đối với lịch trình và ước tính chi phí của dự án. Tất cả bên liên quan của dự án phải đồng ý với các chỉ số ban đầu.

Người quản lý dự án có thể lên kế hoạch lại nhân công cho nhiệm vụ bằng 2 cách:

- Thay thế mục ước tính hoàn thành (ETC) mặc định bằng ước tính mới của nhân công còn lại thực tế trên nhiệm vụ. 
- Thay thế phần trăm tiến trình mặc định bằng ước tính mới của tiến trình đúng trên nhiệm vụ.

Mỗi cách tiếp cận này mang đến một phép tính lại ETC, EAC (ước tính hoàn thành) và phần trăm tiến trình của nhiệm vụ cũng như chênh lệch nhân công dự kiến trên nhiệm vụ. EAC, ETC và phần trăm tiến trình trên các nhiệm vụ tóm tắt được tính toán lại và cung cấp dự kiến mới về chênh lệch nhân công.
