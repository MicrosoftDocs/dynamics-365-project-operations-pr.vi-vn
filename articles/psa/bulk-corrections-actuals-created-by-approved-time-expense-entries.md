---
title: Chỉnh sửa hàng loạt dữ liệu thực tế được tạo bởi các mục nhập thời gian và chi phí đã phê duyệt
description: Chủ đề này giải thích cách quản trị viên có thể thực hiện chỉnh sửa từng phần hoặc hàng loạt đối với các mục nhập thời gian hoặc chi phí đã phê duyệt trước đó nếu chưa hoàn tất thanh toán.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: c6d849e4be9e3687396cd6a0c4158d92f25c7879
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012072"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Chỉnh sửa hàng loạt dữ liệu thực tế được tạo bởi các mục nhập thời gian và chi phí đã phê duyệt

[!include [banner](../includes/psa-now-project-operations.md)]

Đôi khi, một mục nhập thời gian hoặc chi phí có thể bị nhập sai. Ví dụ: tư vấn viên có thể chọn sai ngày khi tạo mục nhập thời gian hoặc họ có thể đổi chỗ các số khi nhập chi phí. Nếu tư vấn viên không thể cập nhật các mục nhập đã gửi, thì quản trị viên có thể trực tiếp chỉnh sửa mục nhập đó cho dự án.

Để hoàn thành các quy trình trong chủ đề này, bạn sẽ cần các quyền của Quản trị viên.

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

Ví dụ: trong hình ảnh sau, có hai mục hàng với số lượng 8 có khoản ghi nợ được liệt kê trong cột Số tiền. Ngoài ra, có hai mục hàng với số lượng -8 hiển thị số tiền đã ghi có trong cột Số tiền. Những giá trị chỉnh sửa này đã đưa số lượng về 0.

![Danh sách dạng xem liên kết thực tế](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Chỉnh sửa mục nhập chi phí đã phê duyệt

Hoàn thành các bước sau để chỉnh sửa một hoặc nhiều mục nhập chi phí. 

1. Trong vùng **Bán hàng**, trong ngăn điều hướng bên trái, trong phần **Giao dịch**, hãy chọn **Chi phí Đã phê duyệt**.

2. Trong danh sách **Chi phí Đã phê duyệt**, hãy chọn dự án bạn muốn chỉnh sửa rồi chọn **Sửa chữa các mục nhập**. Hệ thống tự động tạo một nhật ký chỉnh sửa mới, với loại được gán là **Sửa chữa chi phí**. 

3. Trên trang **Nhật ký Mới**, hãy nhập **Mô tả** cho thao tác điều chỉnh, và trên tab **Sửa chữa Chi phí**, trong phần **Các giá trị mới cho Chi phí**, hãy chọn các trường dữ liệu mà bạn muốn chỉnh sửa cho các dòng chi phí đã chọn. Ví dụ: bạn có thể gán chi phí cho một **Dự án** khác hoặc chỉnh sửa **Loại Chi phí**, **Ngày phát sinh Chi phí** hoặc **Nguồn lực Có thể đăng ký**.

4. Chọn **Xem trước**. Trong hộp thoại, hãy chọn **OK**. 

5. Xác minh các giá trị chỉnh sửa trên tab **Dòng nhật ký kế toán**. Bạn có thể xem danh sách dữ liệu thực tế ban đầu có liên quan đến các mục nhập chi phí bạn chọn đã bị hủy bỏ và các dòng tương ứng đã chỉnh sửa được tạo.

6. Nếu các giá trị chỉnh sửa xuất hiện như mong đợi, hãy chọn **Xác nhận**. Trong hộp thoại, hãy chọn **OK.** Nếu các giá trị không hiển thị như mong đợi, hãy chọn **Hủy** để quay lại danh sách **Chi phí Đã phê duyệt**. Lặp lại các bước từ 2 đến 5. 

> [!NOTE]
> Dữ liệu thực tế đã chỉnh sửa sẽ có cùng giá trị với giá trị mà bạn đã chọn trong phần **Các giá trị mới cho Chi phí**.

7. Sau khi bạn xác nhận nhật ký chỉnh sửa, hãy quay lại dự án hoặc các dự án mà bạn đã cập nhật để xem các thay đổi mà bạn đã thực hiện.  

8. Trong trang dự án, trên tab **Dữ liệu thực tế**, hãy xem lại **Dạng xem Liên kết Thực tế**. Các mục nhập ban đầu và mục nhập đã chỉnh sửa đều được liệt kê. Hình ảnh sau đây cho thấy số tiền trong mục nhập chi phí ban đầu và số tiền trong mục nhập chi phí tương ứng đã điều chỉnh. 

![Expense_actuals](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]