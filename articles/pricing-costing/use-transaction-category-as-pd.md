---
title: Sử dụng Thể loại giao dịch làm thông số định giá
description: Bài viết này cung cấp thông tin về cách sử dụng trường Thể loại giao dịch làm thông số định giá.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911735"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Sử dụng Thể loại giao dịch làm thông số định giá


_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Bài viết này giải thích cách dùng trường **Thể loại giao dịch** làm thông số định giá. 

## <a name="prerequisites"></a>Điều kiện tiên quyết
Trước khi hoàn thành các quy trình trong bài viết này, bạn phải có một giải pháp thông số định giá mới cho tổ chức của mình. Nếu chưa tạo giải pháp như vậy, hãy xem [Tạo các trường và thực thể tùy chỉnh dưới dạng thông số định giá](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Thêm trường Thể loại giao dịch vào các biểu mẫu và dạng xem
Để trường **Thể loại giao dịch** hiển thị trong giải pháp thông số định giá, bạn phải thêm trường này vào tất cả biểu mẫu và dạng xem như một thực thể.

Bảng sau liệt kê tất cả mọi biểu mẫu và dạng xem sẵn dùng, theo thực thể. Bạn cũng phải thêm trường mới vào biểu mẫu hoặc dạng xem bổ sung bất kỳ trong các thực thể đã tùy chỉnh.

|  Thực thể        | Biểu mẫu     |Dạng xem        |
| ------------------------------|---------------------------------|----------------------------------|
|  Giá Vai trò| Thông tin |- Giá danh mục nguồn lực đang hoạt động<br> - Giá danh mục nguồn lực có liên kết |
|  Tăng giá theo Vai trò| Thông tin|- Phần tăng giá theo vai trò đang hoạt động<br>- Phần tăng giá theo vai trò có liên kết |
|  Chi tiết Mô tả Báo giá|- Thông tin dự án<br>- Tạo nhanh dự án| - Chi tiết về dòng báo giá đang hoạt động<br>- Chi tiết về dòng báo giá kết hợp<br>- Chi tiết về dòng báo giá có liên kết |
|  Chi tiết Mô tả Hợp đồng Dự án|- Thông tin dự án<br>- Tạo nhanh dự án|- Chi tiết về dòng hợp đồng kết hợp<br>- Chi tiết về dòng hợp đồng đang hoạt động<br>- Chi tiết về dòng hợp đồng có liên kết |
|  Nhiệm vụ dự án|- Thông tin<br>- Biểu mẫu mới| &nbsp; |
|  Thành viên Nhóm Dự án|- Thông tin<br>- Biểu mẫu mới|- Thành viên nhóm dự án đang hoạt động<br>- Thành viên nhóm dự án<br>- Thành viên nhóm dự án có liên kết |
|  Mục nhập Thời gian|- Thông tin<br>- Tạo mục thời gian|- Mục thời gian của tôi theo ngày<br>- Mục thời gian của tôi cho tuần này<br>- Mục thời gian cần để phê duyệt|
|  Dòng nhật ký kế toán|- Thông tin<br>- Tạo nhanh|- Dòng nhật ký kế toán hiện hoạt<br>- Dòng nhật ký kế toán có liên kết|
|  Chi tiết Mô tả Hóa đơn|- Thông tin<br>- Tạo nhanh|- Chi tiết về dòng hóa đơn hiện hoạt<br>- Giao dịch hóa đơn có thể tính phí<br>- Giao dịch hóa đơn miễn phí<br>- Chi tiết về dòng hóa đơn có liên kết <br>- Giao dịch hóa đơn không thể tính phí|
|  Thực tế|- Thông tin<br>- Trường hợp thực tế hiện hoạt| Thực tế có liên kết |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Thiết lập trường Thể loại giao dịch làm thông số định giá

1. Đi tới **Cài đặt** > **Tham số**. 
2. Trên trang **Tham số**, trên tab **Thông số định giá dựa trên số tiền**, hãy xác minh rằng lưới này hiển thị các bản ghi trong thực thể **Thông số định giá**.
3. Thêm **Thể loại giao dịch** vào danh sách này rồi đặt các trường **Áp dụng cho chi phí** và **Áp dụng cho doanh số** thành **Có**.
4. Trong trường **Loại thông số**, hãy chọn **Dựa trên số tiền**, sau đó chọn mức ưu tiên cho **Thể loại giao dịch** có liên quan đến chi phí và doanh số.


[!INCLUDE[footer-include](../includes/footer-banner.md)]