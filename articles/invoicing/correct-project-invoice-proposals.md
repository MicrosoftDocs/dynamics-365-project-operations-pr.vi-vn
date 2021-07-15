---
title: Chỉnh sửa kế toán trên các đề xuất hóa đơn dự án nháp
description: Chủ đề này giải thích cách điều chỉnh thông tin liên quan đến kế toán trên một đề xuất hóa đơn nháp.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251294"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Chỉnh sửa kế toán trên các đề xuất hóa đơn dự án nháp

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

*Chi tiết hoạt động* đối với các hóa đơn dự án được quản lý dự án duy trì trên hóa đơn ước giá. Những chi tiết này bao gồm quyết định về giờ giấc, chi phí, vật liệu hoặc các mốc quan trọng phải lập hóa đơn, mức giá và việc áp dụng số tiền tạm ứng và trả trước. Sau khi xác nhận hóa đơn ước giá ban đầu, bạn có thể điều chỉnh chi tiết hoạt động bằng cách tạo và xác nhận [hóa đơn ước giá hiệu chỉnh](../proforma-invoicing/corrective-invoices.md).

*Chi tiết kế toán* đối với các hóa đơn dự án được duy trì trong một tài liệu hóa đơn giao cho khách hàng. Những chi tiết này bao gồm cách tính thuế bán hàng và các thông số tài chính được áp dụng cho hóa đơn. Chủ đề này cung cấp chi tiết về cách điều chỉnh các chi tiết kế toán này trên một đề xuất hóa đơn nháp.

## <a name="adjust-sales-tax"></a>Điều chỉnh thuế bán hàng

Nhóm thuế bán hàng lập hóa đơn mặc định và nhóm thuế bán hàng mặt hàng có thể được điều chỉnh trực tiếp trên tài liệu đề xuất hóa đơn. Để điều chỉnh các nhóm này, hãy chọn **Chỉnh sửa**, sau đó, trên mỗi dòng đề xuất hóa đơn dự án, hãy nhập một giá trị mới vào trường **Nhóm thuế bán hàng** hoặc **Nhóm thuế bán hàng mặt hàng**.

## <a name="adjust-financial-dimensions"></a>Điều chỉnh các thông số tài chính

Các thông số tài chính không thể được chỉnh sửa trực tiếp trên dòng đề xuất hóa đơn dự án. Thay vào đó, hãy làm theo các bước sau để điều chỉnh các thông số tài chính trên một đề xuất hóa đơn dự án.

1. Trên đề xuất hóa đơn dự án, hãy chọn **Xóa hết** để loại bỏ các dòng đề xuất hóa đơn dự án.

    > [!NOTE]
    > Nút **Xóa hết** chỉ khả dụng sau khi quản trị viên hệ thống bật tính năng **Xóa các dòng đề xuất hóa đơn khi sử dụng Project Operations cho các tình huống dựa trên tài nguyên/không có kho** trong không gian làm việc **Quản lý tính năng**.

2. Điều chỉn các thông số tài chính:

    - **Giao dịch trên tài khoản (các mốc thanh toán):** Đi đến **Tất cả các dự án** \> **Quản lý** \> **Giao dịch trên tài khoản** và chọn cột mốc cần điều chỉnh. Sau đó, trên tab **Thông số tài chính**, hãy cập nhật các giá trị theo yêu cầu.
    - **Các giao dịch về thời gian, chi phí và vật liệu:** Trên trang **Các giao dịch dự án đã kết sổ**, chọn **Điều chỉnh kế toán** để cập nhật các thông số tài chính.

3. Sau khi bạn điều chỉnh xong các giá trị thông số tài chính, hãy chuyển đến **Quản lý dự án và kế toán** \> **Định kỳ** \> **Tích hợp Project Operations** và chọn **Nhập từ bảng tách chuyển** để chạy quy trình định kỳ. Quy trình đó sử dụng các giá trị thông số tài chính được cập nhật để tạo lại các dòng đề xuất hóa đơn dự án. Sau đó, các giá trị cập nhật được sử dụng trong sổ phụ của dự án và sổ cái chung khi hóa đơn dự án được kết sổ.
