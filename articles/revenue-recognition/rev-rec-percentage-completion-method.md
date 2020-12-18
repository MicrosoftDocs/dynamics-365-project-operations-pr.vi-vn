---
title: Dự án ước tính doanh thu giá cố định
description: Chủ đề này cung cấp thông tin về doanh thu giá cố định trong dự án.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531594"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Dự án ước tính doanh thu giá cố định 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Khi bạn tạo một dòng hợp đồng với những thuộc tính sau trong Dynamics 365 Project Operations trên Microsoft Dataverse, hệ thống sẽ tự động tạo dự án ước tính doanh thu giá cố định. Thông tin trong dự án này sẽ dựa trên:

  - Phương thức thanh toán theo giá cố định.
  - Dự án liên kết.
  - Ít nhất một mốc được xác định trên tab **Lịch trình hóa đơn** của trang **Dòng hợp đồng dự án**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Xem xét dự án ước tính doanh thu theo giá cố định
Để xem xét dự án ước tính doanh thu theo giá cố định, hãy hoàn tất các bước sau:

1. Trong môi trường Dynamics 365 Finance, hãy đi tới **Quản lý dự án và kế toán** > **Dự án** > **Dự án ước tính doanh thu theo giá cố định**.
2. Chọn dự án bạn muốn xem rồi bấm đúp vào **ID dự án ước tính** để mở bản ghi và xem xét chi tiết dự án.
3. Mở rộng tab **Dự án**. Bạn sẽ thấy một dự án trong lưới **Dự án đã chọn**. Hệ thống sẽ dùng dự án này làm dự án mặc định vì đó là dự án liên kết với dòng hợp đồng dự án. 
4. Để thay đổi mối liên kết này, hãy chọn các dự án bổ sung rồi thêm chúng vào lưới **Dự án đã chọn**. Nếu có nhiều dự án được chọn trong lưới này, mức phần trăm hoàn thành dự án và ước tính doanh thu sẽ được tính toán cùng lúc cho tất cả dự án đã chọn.

  Bạn có thể thiết lập chi phí dự án, hồ sơ doanh thu, mẫu chi phí và mã chu kỳ theo cách thủ công. Nếu không đặt được theo cách thủ công, giá trị ước tính mặc định trong lần tính toán đầu tiên của dự án sẽ áp dụng các quy tắc như trong cấu hình hồ sơ doanh thu và chi phí dự án.

