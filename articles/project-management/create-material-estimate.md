---
title: Dự toán tài chính về vật tư cho dự án
description: Chủ đề này cung cấp thông tin về việc xác định hoặc ước tính các vật tư dựa trên dự án.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 768da6adb83b4593a227f60182179b3036f4c040
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002712"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Dự toán tài chính về vật tư cho dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations cho phép Người quản lý dự án xác định chi phí vật tư dựa trên dự án cho từng dự án hoặc nhiệm vụ. Mỗi ước tính vật tư có thể được liên kết với một nhiệm vụ cụ thể của dự án. Các khoản chi phí được phân thành các thể loại chi phí khác nhau, được xác định ở cấp độ tổ chức. Giá và chi phí cho từng thể loại chi phí được xác định trong bảng giá. 

Hoàn thành các bước sau để xem, thêm hoặc xóa giá trị ước tính về vật tư của dự án.

1. Đi đến **Dự án** rồi chọn dự án bạn muốn cập nhật.
2. Trên tab **Ước tính vật tư**, hãy xem danh sách ước tính vật tư của dự án.
3. Chọn **Giá trị ước tính mới về vật tư** để tạo một giá trị ước tính mới về vật tư. Hoặc, chọn một giá trị ước tính về vật tư để xóa, sau đó chọn **Xóa giá trị ước tính về vật tư**.

Bảng sau cung cấp thông tin về các trường trên **Dòng Ước tính vật tư** của một dự án. 

| **Trường** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- |
| Tác vụ | Một danh sách các nhiệm vụ trong dự án. Danh sách này bao gồm các nhiệm vụ tóm tắt và nhiệm vụ nút lá. | Khi bạn chọn một nhiệm vụ cho dòng ước tính vật tư, chi phí vật tư ước tính và doanh số bán hàng của vật tư ước tính cho một nhiệm vụ sẽ bị ảnh hưởng. Nếu để trống trường này, chi phí ước tính về vật tư chỉ được theo dõi và tóm tắt ở cấp độ dự án. |
| Chọn sản phẩm |  Bạn có thể chỉ định dòng ước tính này là cho một sản phẩm (danh mục) hiện có hay cho một sản phẩm chọn thêm. | Trường này xác định xem bạn chọn một sản phẩm từ danh mục hay một sản phẩm chọn thêm. |
| Sản phẩm | ID của sản phẩm từ danh mục sản phẩm. Khi bạn chọn một ID sản phẩm, giá trị trong trường **Chọn sản phẩm** tự động cập nhật thành **Sản phẩm hiện có**. ID được dùng để truy xuất giá vốn và giá bán từ bảng giá. | Không có tác động xuôi tuyến đối với trường này. |
| Mô tả sản phẩm chọn thêm | Trường văn bản để viết tên của sản phẩm. Trường này chỉ được dùng khi bạn chọn **Chọn thêm** bên trong trường **Chọn sản phẩm**.| Không có tác động xuôi tuyến đối với trường này. |
| Ngày bắt đầu | Ngày dự báo sẽ sử dụng vật tư. | Không có tác động xuôi tuyến đối với trường này. |
| Nhóm đơn vị đo | Giá trị mặc định trong trường này đến từ nhóm đơn vị mặc định trên sản phẩm danh mục. Bạn có thể cập nhật trường này để chọn một nhóm đơn vị khác. | Không có tác động xuôi tuyến đối với trường này. |
| Đơn vị | Giá trị trong trường là từ đơn vị mặc định của sản phẩm đã chọn. Bạn có thể cập nhật trường này để chọn một đơn vị khác. | Việc thay đổi đơn vị sẽ dẫn đến một đơn giá và chi phí mặc định khác. |
| Số lượng | Số lượng ước tính của sản phẩm sẽ được dùng trong dự án. | Không có tác động xuôi tuyến đối với trường này. |
| Chi phí đơn vị | Chi phí đơn vị của tổ hợp đơn vị và sản phẩm đã chọn như được thiết lập trong bảng giá vốn áp dụng. | Chi phí đơn vị luôn hiển thị theo đơn vị tiền tệ chi phí của dự án. Nếu chưa thiết lập chi phí đơn vị cho tổ hợp sản phẩm và đơn vị được thiết lập trong bảng giá, thì chi phí đơn vị sẽ mặc định là 0,00. |
| Đơn giá | Giá của tổ hợp đơn vị và sản phẩm đã chọn như được thiết lập trong bảng giá bán hàng áp dụng. | Đơn giá luôn hiển thị theo đơn vị tiền tệ bán hàng của dự án. Nếu chưa thiết lập đơn giá cho tổ hợp sản phẩm và đơn vị được thiết lập trong bảng giá, thì giá sẽ mặc định là 0,00.|
| Tổng chi phí | Số tiền chi phí được tính theo công thức số lượng \* chi phí đơn vị.| Số tiên chi phí luôn hiển thị theo đơn vị tiền tệ chi phí của dự án. |
| Tổng doanh thu | Số tiền bán hàng được tính theo công thức số lượng \* đơn giá. | Số tiền bán hàng luôn hiển thị theo đơn vị tiền tệ bán hàng của dự án. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
