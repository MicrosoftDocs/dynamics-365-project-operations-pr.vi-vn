---
title: Sử dụng loại giao dịch làm thông số định giá
description: Bài viết này cung cấp thông tin về việc sử dụng danh mục giao dịch làm thứ nguyên định giá.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915762"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Sử dụng loại giao dịch làm thông số định giá

[!include [banner](../includes/psa-now-project-operations.md)]

Bài viết này cho biết cách sử dụng danh mục giao dịch làm thứ nguyên định giá. Trước khi bạn bắt đầu, nếu chưa tạo giải pháp thông số định giá, bạn cần tạo một giải pháp mới. Nếu đã có giải pháp cho thông số định giá, bạn có thể thay đổi giải pháp đó. Nếu bạn chưa tạo giải pháp thứ nguyên đặt giá mới cho tổ chức của mình, hãy hoàn tất các thủ tục trong [Tạo các trường và thực thể tùy chỉnh](create-custom-fields-entities.md) bài báo.

## <a name="add-transaction-category-to-forms-and-views"></a>Thêm loại giao dịch vào biểu mẫu và chế độ xem
Để làm cho loại giao dịch hiển thị trong giao diện người dùng trong giải pháp thông số định giá, bạn cần tìm hiểu tất cả các biểu mẫu và chế độ xem của các thực thể chính và thêm các trường này vào biểu mẫu cũng như chế độ xem của các thực thể đó.
Bảng sau đây cung cấp danh sách toàn diện các biểu mẫu và dạng xem có sẵn, theo thực thể sẽ cần phải được cập nhật với các trường mới. Nếu có bất kỳ chế độ xem hoặc biểu mẫu bổ sung nào trong tùy chỉnh của mình trên các thực thể này, hãy thêm các trường mới vào các mục đó.

|  Thực thể        | Biểu mẫu     |Dạng xem        |
| ------------------------------|---------------------------------|----------------------------------|
|  Giá Vai trò|• Thông tin |• Giá danh mục nguồn lực hoạt động<br> • Chế độ xem liên kết của Giá danh mục nguồn lực|
|  Tăng giá theo Vai trò|• Thông tin|• Tăng giá theo vai trò hiện hoạt<br>• Chế độ xem liên kết tăng giá theo vai trò|
|  Chi tiết mô tả báo giá|• Thông tin dự án<br>• Tạo nhanh dự án|• Chi tiết mô tả báo giá hiện hoạt<br>• Chi tiết mô tả báo giá kết hợp<br>• Dạng xem liên kết chi tiết mô tả báo giá|
|  Chi tiết mô tả hợp đồng dự án|• Thông tin dự án<br>• Tạo nhanh dự án|• Chi tiết mô tả hợp đồng kết hợp<br>• Chi tiết mô tả hợp đồng hiện hoạt<br>• Chế độ xem liên kết chi tiết mô tả hợp đồng|
|  Nhiệm vụ dự án|• Thông tin<br>• Biểu mẫu mới||
|  Thành viên Nhóm Dự án|• Thông tin<br>• Biểu mẫu mới|• Thành viên nhóm dự án hiện hoạt<br>• Thành viên nhóm dự án<br>• Chế độ xem liên kết cho thành viên nhóm dự án|
|  Mục nhập Thời gian|• Thông tin<br>• Tạo mục nhập thời gian|• Mục nhập thời gian theo ngày của tôi<br>• Mục nhập thời gian của tôi trong tuần này<br>• Mục nhập thời gian để phê duyệt|
|  Dòng Nhật ký Kế toán|• Thông tin<br>• Tạo nhanh|• Dòng nhật ký kế toán hiện hoạt<br>• Chế độ xem liên kết dòng nhật ký kế toán|
|  Chi tiết Mô tả Hóa đơn|• Thông tin<br>• Tạo nhanh|• Chi tiết mô tả hóa đơn hiện hoạt<br>• Giao dịch hóa đơn có thể tính phí<br>• Giao dịch hóa đơn miễn phí<br>• Dạng xem liên kết chi tiết mô tả hóa đơn<br>• Giao dịch hóa đơn không thể tính phí|
|  Thực tế|• Thông tin<br>• Thực tế hiện hoạt|• Dạng xem liên kết thực tế|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Thiết lập loại giao dịch làm thông số định giá

1. Trong giao diện web, hãy đi tới phần **Project Service** > **Cài đặt** > **Thông số**. 
2. Trên trang **Thông số**, trên tab **Thông số định giá dựa trên số lượng**, lưu ý rằng lưới trên tab hiển thị các bản ghi trong thực thể **Thông số định giá**.
3. Thêm **loại giao dịch** vào danh sách này và đặt các trường **Áp dụng cho chi phí** và **Áp dụng cho doanh số** thành **Có**.
4. Trong trường **Loại thông số**, hãy chọn **Dựa trên số lượng**, sau đó chọn mức ưu tiên cho **loại giao dịch** liên quan đến chi phí và doanh số.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
