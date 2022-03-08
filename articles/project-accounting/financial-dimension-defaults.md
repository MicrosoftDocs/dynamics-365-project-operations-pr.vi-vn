---
title: Giá trị mặc định cho thông số tài chính
description: Chủ đề này cung cấp thông tin về cách thiết lập các giá trị mặc định cho thông số tài chính.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eec85b83cad4cd8fb6e0ec9c026c6a571bccf7f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287399"
---
# <a name="financial-dimension-defaults"></a>Giá trị mặc định cho thông số tài chính

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations dùng khung [Thông số tài chính](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) trong Dynamics 365 Finance để cung cấp thêm thông tin chi tiết về các giao dịch trong sổ cái phụ và sổ cái chung của dự án.

Các thông số tài chính mặc định có thể được đặt theo khách hàng, nguồn tài trợ dự án, mốc, phần mô tả hợp đồng dự án hoặc dự án.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Xác định các thông số tài chính mặc định cho khách hàng

Các giá trị mặc định của thông số khách hàng được chỉ định trong Finance. Hoàn tất các bước sau để thiết lập giá trị mặc định cho thông số.

1. Chuyển đến **Khoản phải thu** > **Khách hàng** > **Tất cả khách hàng**.
2. Trên trang **Khách hàng**, ở tab **Thông số tài chính**, hãy đặt các giá trị của thông số tài chính cho khách hàng cụ thể.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Xác định thông số tài chính mặc định cho các hợp đồng dự án

Hợp đồng dự án được tạo và duy trì trong Common Data Service (CDS). Các thuộc tính kế toán của hợp đồng dự án được đặt ở mô-đun **Kế toán và quản lý dự án** trong Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Đặt các thông số tài chính cho nguồn tài trợ dự án

1. Chuyển đến **Kế toán và quản lý dự án** > **Dự án** > **Hợp đồng dự án**.
2. Chọn hồ sơ bạn muốn cập nhật, trên tab **Hợp đồng dự án**, chọn **Hiển thị giá trị kế toán mặc định**.
3. Mở rộng **Thông tin liên quan** rồi chọn tab **Nguồn tài trợ**.
4. Đặt các giá trị mặc định cho thông số tài chính. Lưu ý rằng các thông số tài chính lấy giá trị mặc định từ tài khoản khách hàng.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Đặt các thông số tài chính cho phần mô tả hợp đồng dự án

1. Chuyển đến **Kế toán và quản lý dự án** > **Dự án** > **Hợp đồng dự án**.
2. Chọn hồ sơ bạn muốn cập nhật, trên tab **Hợp đồng dự án**, chọn **Hiển thị giá trị kế toán mặc định**.
3. Mở rộng **Thông tin liên quan** rồi chọn tab **Nguồn tài trợ**.
4. Đặt các giá trị mặc định cho thông số tài chính. Các giá trị mặc định của thông số tài chính được áp dụng và chỉ có thể dùng với các dòng mô tả hợp đồng có Giá cố định (mốc).

Các giá trị mặc định này được sử dụng cho các giao dịch trên tài khoản và các dòng mô tả hóa đơn có liên quan của dự án.

## <a name="define-default-financial-dimensions-for-projects"></a>Xác định thông số tài chính mặc định cho các dự án

Dự án được tạo và duy trì trong CDS. Các thuộc tính kế toán của dự án được đặt ở mô-đun **Kế toán và quản lý dự án** trong Finance.

1. Chuyển đến **Kế toán và quản lý dự án** > **Dự án** > **Tất cả dự án**.
2. Chọn hồ sơ bạn muốn cập nhật, trên tab **Dự án**, chọn **Hiển thị giá trị kế toán mặc định**.
3. Mở rộng **Thông tin liên quan** rồi chọn tab **Thiết lập**.
4. Đặt các giá trị mặc định cho thông số tài chính. Lưu ý rằng các thông số tài chính lấy giá trị mặc định từ tài khoản khách hàng. Nếu dự án được liên kết với phần mô tả hợp đồng có nhiều khách hàng trong hợp đồng dự án, thì khách hàng chính được sử dụng làm thông số tài chính mặc định.

Các thông số tài chính mặc định của dự án được sử dụng để đặt các giá trị mặc định về thời gian, chi phí và phí giao dịch cho dòng nhật ký kế toán trong **Nhật ký tích hợp Project Operations** và trên các dòng mô tả hóa đơn dự án có liên quan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]