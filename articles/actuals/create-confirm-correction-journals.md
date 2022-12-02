---
title: Tạo và xác nhận nhật ký Chỉnh sửa
description: Bài viết này cung cấp thông tin về cách tạo và xác nhận nhật ký chỉnh sửa.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928090"
---
# <a name="create-and-confirm-correction-journals"></a>Tạo và xác nhận nhật ký Chỉnh sửa

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Đôi khi, một mục nhập thời gian hoặc chi phí có thể bị nhập sai. Ví dụ: tư vấn viên có thể chọn sai ngày khi tạo mục nhập thời gian hoặc họ có thể chọn nhầm dự án khi nhập một khoản chi phí. Nếu tư vấn viên không thể cập nhật các mục nhập đã gửi, một quản trị viên phụ trợ có thể trực tiếp chỉnh sửa các số liệu thực tế cho một dự án.

## <a name="correct-approved-time-entries"></a>Chỉnh sửa mục nhập thời gian đã phê duyệt     

Hoàn thành các bước sau để chỉnh sửa một hoặc nhiều mục nhập thời gian cho dự án.

1. Trong vùng **Bán hàng**, hãy chọn **Giao dịch**, sau đó chọn **Thời gian Đã phê duyệt**. 

2. Trong danh sách **Thời gian Đã phê duyệt**, hãy tìm và chọn một hoặc nhiều mục nhập thời gian cần chỉnh sửa. Bạn có thể sử dụng bộ lọc để tìm các mục nhập liên quan. Ví dụ: bạn có thể lọc trên ID Dự án và chọn tất cả các mục nhập thời gian đã phê duyệt với ID Dự án đó.

3. Chọn **Sửa chữa các mục nhập**. Hệ thống tự động tạo một nhật ký chỉnh sửa mới, với loại được gán là **Sửa chữa thời gian**. Các mục nhập bạn đã chọn được thêm vào nhật ký. 

4. Trên trang **Nhật ký Mới**, hãy nhập **Mô tả** cho nhật ký chỉnh sửa của bạn rồi chọn tab **Sửa chữa Mục nhập Thời gian**.  

5. Trong phần **Các giá trị mới cho Mục nhập Thời gian**, hãy cập nhật các trường với thông tin chính xác nếu cần. Ví dụ: bạn có thể thay đổi dự án đã gán hoặc nguồn lực có thể đăng ký.

6. Chọn **Xem trước**. Trong hộp thoại, hãy chọn **OK**. Trên tab **Dòng nhật ký kế toán**, bạn có thể xem danh sách dữ liệu thực tế ban đầu có liên quan đến các mục nhập thời gian bạn chọn đã bị hủy bỏ và các dòng tương ứng đã chỉnh sửa được tạo. Nếu cần chỉnh sửa thêm, hãy lặp lại bước 5 và 6. 

    > [!NOTE]
    > Tất cả dữ liệu thực tế đã chỉnh sửa sẽ có cùng giá trị với giá trị mà bạn đã chọn trong phần **Các giá trị mới cho Mục nhập Thời gian**.

7. Nếu các giá trị chỉnh sửa xuất hiện như mong đợi, hãy chọn **Xác nhận**. Trong hộp thoại, hãy chọn **OK**.

8. Quay lại vùng **Bán hàng**, chọn **Dự án** rồi mở dự án mà bạn vừa cập nhật các mục nhập thời gian. 

9. Trên trang **Dự án**, trên tab **Dữ liệu thực tế**, hãy xem các thay đổi mà bạn đã thực hiện. 

    > [!NOTE]
    > Nếu tab **Dữ liệu thực tế** không hiển thị, hãy chọn **Có liên quan** > **Dữ liệu thực tế**.  

10. Trong danh sách **Dạng xem Liên kết Thực tế**, bạn có thể thấy rằng các mục nhập thời gian ban đầu đã hủy bỏ vẫn có trong danh sách, cũng như các mục nhập thời gian tương ứng đã chỉnh sửa. 

 
## <a name="correct-approved-expense-entries"></a>Chỉnh sửa mục nhập chi phí đã phê duyệt

Hoàn thành các bước sau để chỉnh sửa một hoặc nhiều mục nhập chi phí. 

1. Trong vùng **Bán hàng**, trong ngăn điều hướng bên trái, trong phần **Giao dịch**, hãy chọn **Chi phí Đã phê duyệt**.

2. Trong danh sách **Chi phí Đã phê duyệt**, hãy chọn dự án bạn muốn chỉnh sửa rồi chọn **Sửa chữa các mục nhập**. Hệ thống tự động tạo một nhật ký chỉnh sửa mới, với loại được gán là **Sửa chữa chi phí**. 

3. Trên trang **Nhật ký Mới**, hãy nhập **Mô tả** cho thao tác điều chỉnh, và trên tab **Sửa chữa Chi phí**, trong phần **Các giá trị mới cho Chi phí**, hãy chọn các trường dữ liệu mà bạn muốn chỉnh sửa cho các dòng chi phí đã chọn. Ví dụ: bạn có thể gán chi phí cho một **Dự án** khác hoặc chỉnh sửa **Loại Chi phí**, **Ngày phát sinh Chi phí** hoặc **Nguồn lực Có thể đăng ký**.

4. Chọn **Xem trước**. Trong hộp thoại, hãy chọn **OK**. 

5. Xác minh các giá trị chỉnh sửa trên tab **Dòng nhật ký kế toán**. Bạn có thể xem danh sách dữ liệu thực tế ban đầu có liên quan đến các mục nhập chi phí bạn chọn đã bị hủy bỏ và các dòng tương ứng đã chỉnh sửa được tạo.

6. Nếu các giá trị chỉnh sửa xuất hiện như mong đợi, hãy chọn **Xác nhận**. Trong hộp thoại, hãy chọn **OK.** Nếu các giá trị không hiển thị như mong đợi, hãy chọn **Hủy** để quay lại danh sách **Chi phí Đã phê duyệt**. Lặp lại các bước từ 2 đến 5. 

7. Sau khi bạn xác nhận nhật ký chỉnh sửa, hãy trở lại dự án hoặc các dự án mà bạn đã cập nhật để xem các thay đổi mà bạn đã thực hiện.

8. Trên trang dự án, trên tab **Dữ liệu thực tế**, hãy xem lại danh sách **Dạng xem Liên kết Thực tế**. Các mục nhập ban đầu và mục nhập đã chỉnh sửa đều được liệt kê.


## <a name="correct-approved-material-usage-logs"></a>Sửa nhật ký sử dụng vật tư đã phê duyệt

Hoàn thành các bước sau để chỉnh sửa một hoặc nhiều mục nhập nhật ký sử dụng vật tư.

1. Trong vùng **Bán hàng**, trong ngăn điều hướng bên trái, trong phần **Giao dịch**, hãy chọn **Thực tế**.

2. Trong danh sách **Thực tế**, sử dụng bộ lọc cột để chọn lớp giao dịch **Vật tư** sao cho chỉ các số liệu thực tế cho vật tư được hiển thị. Sử dụng các bộ lọc cột khác để hạn chế hơn nữa các số liệu thực tế được hiển thị. Sau khi bạn có thể tìm thấy bộ các số liệu thực tế mong muốn, hãy chọn số liệu thực tế, sau đó chọn **Sửa mục nhập**. Hệ thống tự động tạo một nhật ký chỉnh sửa mới và loại **Chỉnh sửa vật tư** được chỉ định.

3. Trên trang **Nhật ký mới**, trong trường **Mô tả**, nhập mô tả của nhật ký để chỉnh sửa. Sau đó, trên tab **Chỉnh sửa vật tư**, trong phần **Giá trị mới cho vật tư**, chọn các trường dữ liệu để sửa cho các mô tả vật tư đã chọn. Ví dụ: bạn có thể chỉ định vật tư cho một dự án khác hoặc sửa sản phẩm, ngày vật tư hoặc hợp đồng phụ.

4. Chọn **Xem trước**. Sau đó, trong hộp thoại, hãy chọn **OK**.

5. Trên tab **Dòng nhật ký kế toán**, xác minh các chi tiết chỉnh sửa. Bạn có thể xem danh sách dữ liệu thực tế ban đầu có liên quan đến các mục nhập vật tư bạn chọn đã bị hủy bỏ và các dòng tương ứng đã chỉnh sửa được tạo.

6. Nếu các giá trị chỉnh sửa xuất hiện như mong đợi, hãy chọn **Xác nhận**. Sau đó, trong hộp thoại, hãy chọn **OK**. Nếu các giá trị không hiển thị như mong đợi, hãy chọn **Hủy** để quay lại danh sách **Thực tế**. Sau đó, lặp lại các bước từ 2 đến 5.

7. Sau khi bạn xác nhận nhật ký chỉnh sửa, hãy trở lại dự án hoặc các dự án mà bạn đã cập nhật để xem các thay đổi mà bạn đã thực hiện.

8. Trên trang dự án, trên tab **Dữ liệu thực tế**, hãy xem lại danh sách **Dạng xem Liên kết Thực tế**. Các mục nhập ban đầu và mục nhập đã chỉnh sửa đều được liệt kê.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
