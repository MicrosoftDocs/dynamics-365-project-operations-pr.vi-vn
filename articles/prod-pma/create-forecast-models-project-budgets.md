---
title: Tạo mô hình dự báo cho ngân sách dự án
description: Chủ đề này mô tả cách tạo mô hình dự báo cho ngân sách còn lại.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: c4467bc1c687b028f1cce8280c3cf0b5ef492b6fd1a024d49f001ce5ff8a34cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986022"
---
# <a name="create-forecast-models-for-project-budgets"></a>Tạo mô hình dự báo cho ngân sách dự án 

[!include [banner](../includes/banner.md)]

Chủ đề này mô tả cách tạo mô hình dự báo cho ngân sách còn lại. Một dự án được kiểm soát ngân sách sẽ sử dụng hai loại ngân sách: ngân sách ban đầu và ngân sách còn lại. Khi tạo ngân sách dự án, bạn phải chỉ định mô hình dự báo ngân sách ban đầu và ngân sách còn lại đã được tạo ở trang **Mô hình dự báo**. Ngân sách dự án dựa trên mô hình đã chỉ định sẽ được tạo khi bạn cam kết ngân sách dự án.

> [!NOTE]
> Mô hình dự báo dùng để kiểm soát ngân sách không được có mô hình con và không được dùng làm mô hình con.

1. Chọn **Quản lý dự án và kế toán** > **Thiết lập** > **Dự báo**  > **Mô hình dự báo**.
2. Chọn **Mới** để tạo mô hình dự báo mới, rồi nhập số ID mô hình và tên cho mô hình mới. 
3. Đặt tùy chọn **Đã dừng** thành **Có** để ngăn chặn mọi sự thay đổi đối với dòng dự báo cho mô hình dự báo. 
4. Nếu mô hình được liên kết với các dòng dự báo sẽ tạo ra dự báo dòng tiền trong sổ cái, hãy đặt **Đưa vào dự báo dòng tiền** thành **Có**. 
5. Để sử dụng ngày dự án làm ngày lập hóa đơn, hãy đặt **Dự báo ngày lập hóa đơn** thành **Có**. 
6. Ở trường **Loại ngân sách**, hãy chọn một trong các loại mô hình sau:

   - **Ngân sách ban đầu**: Sử dụng số tiền ngân sách ban đầu đã cam kết khi ngân sách ban đầu được tạo và phê duyệt.
   - **Ngân sách còn lại**: Sử dụng số tiền ngân sách còn lại trong suốt vòng đời của dự án. Số dư trong mô hình dự báo này bị giảm đi do các giao dịch thực tế và tăng hoặc giảm theo các mục sửa đổi ngân sách.
   - **Chuyển tiếp**: Sử dụng số tiền ngân sách chuyển tiếp cho dự án. Chuyển tiếp là một quy trình không bắt buộc, có thể được chạy để chuyển số tiền ngân sách chưa sử dụng từ năm tài chính này sang năm tài chính khác.

7. Đặt các tùy chọn sau theo yêu cầu:

   - Kích hoạt **Dự báo ngày lập hóa đơn** để sử dụng ngày dự án làm ngày lập hóa đơn.
   - Kích hoạt **Dự báo với WIP** để dự báo dựa trên công việc đang tiến hành (WIP), sau đó chọn loại WIP. 
   - Bạn có thể giữ **Loại ngân sách** mặc định là **Không có** hoặc nhập một loại mới. Bạn không thể thay đổi loại ngân sách sau khi thay đổi bản ghi.     
    > [!NOTE]
    > Nếu bạn thay đổi loại ngân sách mặc định, thì tất cả các tùy chọn khác sẽ không có sẵn để cập nhật và bạn không thể sử dụng lại mô hình dự báo này. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]