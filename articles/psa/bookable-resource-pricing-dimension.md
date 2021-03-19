---
title: Sử dụng tài nguyên có thể đặt lịch làm phương diện giá
description: Chủ đề này cung cấp thông tin về cách sử dụng nguồn lực có thể đặt lịch làm phương diện định giá.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d3f5ed7da5972cec5b22524bdcb3dc34a83eee28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290970"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Sử dụng tài nguyên có thể đặt lịch làm phương diện giá

[!include [banner](../includes/psa-now-project-operations.md)]

Chủ đề này cung cấp thông tin về cách sử dụng nguồn lực có thể đặt lịch làm phương diện định giá. Trước khi bạn bắt đầu, nếu chưa tạo giải pháp thông số định giá, bạn cần tạo một giải pháp mới. Nếu đã có giải pháp cho thông số định giá, bạn có thể thay đổi giải pháp đó. Nếu bạn chưa tạo giải pháp thông số định giá mới cho tổ chức của mình, hãy hoàn tất quy trình trong chủ đề [Tạo trường và thực thể tùy chỉnh](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Thêm nguồn lực có thể đặt lịch vào biểu mẫu và dạng xem
Để làm cho các trường hiển thị trong giao diện người dùng trong giải pháp phương diện định giá, bạn sẽ cần tìm hiểu tất cả các biểu mẫu và chế độ xem của các thực thể Project Service chính và thêm các trường này vào biểu mẫu cũng dạng xem của các thực thể đó.
Bảng sau đây cung cấp một danh sách toàn diện các biểu mẫu và dạng xem sẵn dùng, liệt kê theo thực thể sẽ cần phải được cập nhật. Nếu có bất kỳ dạng xem bổ sung hoặc biểu mẫu nào trong tùy chỉnh của mình trên các thực thể này, hãy thêm các trường mới vào các mục đó.
Mở Solution Explorer cho giải pháp phương diện định giá rồi nhấp vào **Phát hành tất cả tùy chỉnh**.


|   Thực thể        | Biểu mẫu   |Dạng xem        |
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

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Thiết lập tài nguyên có thể đặt lịch làm phương diện giá

1. Trong giao diện web, hãy đi tới phần **Project Service** > **Cài đặt** > **Thông số**. Trên trang **Tham số**, trên tab **Phương diện định giá dựa trên số lượng**, lưu ý rằng lưới trên tab hiển thị các bản ghi trong thực thể phương diện định giá. 
2. Thêm **Nguồn lực có thể đặt lịch** và danh sách phương diện định giá này dưới dạng **msdyn_bookableresource**. 
3. Cho biết bối cảnh mà nguồn lực có thể đặt lịch hoạt động như một phương diện định giá và đặt các giá trị **Áp dụng cho chi phí** và **Áp dụng cho bán hàng**.
4. Trong trường **Loại phương diện**, chọn **Dựa trên số lượng**. 
5. Chọn ưu tiên chi phí và bán hàng cho nguồn lực có thể đặt lịch. Thông thường, khi bao gồm như là một phương diện định giá, một nguồn lực có thể đặt lịch có ưu tiên cao nhất, nên việc đặt thành **1** (hoặc **0** tùy thuộc vào cách bạn đếm ưu tiên) sẽ đảm bảo hành vi đó.

## <a name="set-up-pricing-dimension-field-names"></a>Thiết lập tên trường phương diện định giá

Khi tên trường của một phương diện định giá trong bảng **Giá theo vai trò** khác với tên trường trong bất kỳ thực thể nào khác, trong đó giá mặc định cần để làm việc, thì bản ghi phương diện định giá phải cho biết các tên khác nhau.    
Đối với nguồn lực có thể đặt chỗ, thực thể **Thành viên nhóm dự án** có tên trường hơi khác một chút (**msdyn_bookableresourceid**) so với trên thực thể **Giá theo vai trò** (**msdyn_bookableresource**). Bản ghi phương diện định giá cho **msydn_bookableresource** phải thể hiện điều này. 
1. Để thực hiện việc này, nhấp đúp vào hàng trong lưới **Phương diện định giá** để mở trang phương diện của **msdyn_bookableresource**.
2. Trên trang phương diện, trên tab **Liên quan**, nhấp vào **Tên trường phương diện định giá**.

 ![Tab tên trường phương diện định giá](media/PD-fieldname.png)

4. Trên dạng xem liên kết mở ra, nhấp vào **Thêm tên trường phương diện định giá mới**.

 ![Thêm tên trường phương diện định giá mới](media/Add-NewPD-fieldname.png)


Thao tác này sẽ mở ra trang **Tên trường phương diện định giá mới** cho **msdyn_bookableresource**. 

5. Thêm **msdyn_projectteam** vào trường **Tên logic thực thể** và **msdyn_bookableresourceid** vào trường **Tên trường**. Lưu bản ghi.

 ![Biểu mẫu tên trường phương diện định giá mới](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]