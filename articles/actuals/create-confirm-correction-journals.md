---
title: Tạo và xác nhận nhật ký Chỉnh sửa
description: Bài viết này cung cấp thông tin về cách tạo và xác nhận một nhật ký sửa chữa.
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

Đôi khi, mục nhập thời gian hoặc chi phí có thể được nhập không chính xác. Ví dụ, một nhà tư vấn có thể chọn sai ngày khi họ tạo mục nhập thời gian hoặc họ có thể chọn sai dự án khi nhập chi phí. Nếu một nhà tư vấn không thể cập nhật các mục đã gửi, một quản trị viên phụ có thể trực tiếp sửa các thông số kỹ thuật cho một dự án.

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

7. Sau khi bạn xác nhận nhật ký sửa chữa, hãy quay lại dự án hoặc các dự án mà bạn đã cập nhật để xem các thay đổi của bạn.

8. Trên trang dự án, trên **Thực tế** tab, xem lại **Chế độ xem được liên kết thực tế** danh sách. Các mục nhập ban đầu và mục nhập đã chỉnh sửa đều được liệt kê.


## <a name="correct-approved-material-usage-logs"></a>Chính xác nhật ký sử dụng vật liệu đã được phê duyệt

Hoàn thành các bước sau để sửa một hoặc nhiều mục nhật ký sử dụng vật liệu.

1. Bên trong **Việc bán hàng** khu vực, trong ngăn điều hướng bên trái, bên dưới **Giao dịch**, lựa chọn **Thực tế**.

2. Bên trong **Thực tế** danh sách, sử dụng bộ lọc cột để chọn **Vật chất** lớp giao dịch, để chỉ hiển thị các hướng dẫn thực tế cho vật liệu. Sử dụng các bộ lọc cột khác để hạn chế hơn nữa các thực tế được hiển thị. Sau khi bạn có thể tìm thấy tập hợp các hành động mong muốn, hãy chọn các hành động đó, sau đó chọn **Các mục nhập chính xác**. Một nhật ký sửa chữa mới được tạo tự động và **Hiệu chỉnh vật liệu** loại được chỉ định.

3. Trên **Tạp chí Mới** trang, trong **Sự mô tả**, hãy nhập mô tả cho việc sửa chữa. Sau đó, trên **Hiệu chỉnh vật liệu** tab, trong **Giá trị mới cho vật liệu**, chọn các trường dữ liệu để sửa cho các dòng nguyên liệu đã chọn. Ví dụ: bạn có thể chỉ định vật liệu cho một dự án khác, hoặc sửa sản phẩm, ngày vật liệu hoặc hợp đồng phụ.

4. Chọn **Xem trước**. Sau đó, trong hộp thoại, hãy chọn **ĐƯỢC RỒI**.

5. Trên **Dòng nhật ký** tab, xác minh các sửa chữa. Bạn có thể xem danh sách các thao tác ban đầu có liên quan đến các mục nhập vật liệu đã chọn đã được đảo ngược và các dòng tương ứng đã được chỉnh sửa đã được tạo.

6. Nếu các giá trị chỉnh sửa xuất hiện như mong đợi, hãy chọn **Xác nhận**. Sau đó, trong hộp thoại, hãy chọn **ĐƯỢC RỒI**. Nếu các giá trị không như mong đợi, hãy chọn **Hủy bỏ** để trở lại **Thực tế** danh sách. Sau đó lặp lại các bước từ 2 đến 5.

7. Sau khi bạn xác nhận nhật ký sửa chữa, hãy quay lại dự án hoặc các dự án mà bạn đã cập nhật để xem các thay đổi của bạn.

8. Trên trang dự án, trên **Thực tế** tab, xem lại **Chế độ xem được liên kết thực tế** danh sách. Các mục nhập ban đầu và mục nhập đã chỉnh sửa đều được liệt kê.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
