---
title: Sử dụng loại giao dịch làm thông số định giá
description: Chủ đề này cung cấp thông tin về cách sử dụng loại giao dịch làm thông số định giá.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757126"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Sử dụng loại giao dịch làm thông số định giá
Chủ đề này trình bày cách sử dụng loại giao dịch làm thông số định giá. Trước khi bạn bắt đầu, nếu chưa tạo giải pháp thông số định giá, bạn cần tạo một giải pháp mới. Nếu đã có giải pháp cho thông số định giá, bạn có thể thay đổi giải pháp đó. Nếu bạn chưa tạo giải pháp thông số định giá mới cho tổ chức của mình, hãy hoàn tất quy trình trong chủ đề [Tạo trường và thực thể tùy chỉnh](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Thêm loại giao dịch vào biểu mẫu và chế độ xem
Để làm cho loại giao dịch hiển thị trong giao diện người dùng trong giải pháp thông số định giá, bạn cần tìm hiểu tất cả các biểu mẫu và chế độ xem của các thực thể chính và thêm các trường này vào biểu mẫu cũng như chế độ xem của các thực thể đó.
Bảng sau đây cung cấp danh sách toàn diện các biểu mẫu và dạng xem có sẵn, theo thực thể sẽ cần phải được cập nhật với các trường mới. Nếu có bất kỳ chế độ xem hoặc biểu mẫu bổ sung nào trong tùy chỉnh của mình trên các thực thể này, hãy thêm các trường mới vào các mục đó.

|  Thực thể        | Biểu mẫu     |Dạng xem        |
| ------------------------------|---------------------------------|----------------------------------|
|  Giá Vai trò|• Thông tin |• Giá danh mục nguồn lực hoạt động<br> • Chế độ xem liên kết của Giá danh mục nguồn lực|
|  Tăng giá theo Vai trò|• Thông tin|• Tăng giá theo vai trò hiện hoạt<br>• Chế độ xem liên kết tăng giá theo vai trò|
|  Chi tiết mô tả báo giá|• Thông tin dự án<br>• Tạo nhanh dự án|• Chi tiết mô tả báo giá hiện hoạt<br>• Chi tiết mô tả báo giá kết hợp<br>• Dạng xem liên kết chi tiết mô tả báo giá|
|  Chi tiết mô tả hợp đồng dự án|• Thông tin dự án<br>• Tạo nhanh dự án|• Chi tiết mô tả hợp đồng kết hợp<br>• Chi tiết mô tả hợp đồng hiện hoạt<br>• Chế độ xem liên kết chi tiết mô tả hợp đồng|
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
