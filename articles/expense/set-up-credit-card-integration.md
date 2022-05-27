---
title: Thiết lập phần tích hợp thẻ tín dụng
description: Chủ đề này giải thích cách làm việc với các giao dịch thẻ tín dụng liên quan đến chi phí.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c9d993f1999b0be24794bbe828afa8eb74744e9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577109"
---
# <a name="set-up-credit-card-integration"></a>Thiết lập phần tích hợp thẻ tín dụng

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các giao dịch thẻ tín dụng liên quan đến chi phí có thể được thiết lập để tự động nhập vào theo lịch trình định kỳ. Ngoài ra, có thể nhập giao dịch theo cách thủ công khi cần. Các giao dịch thẻ tín dụng được nhập thông qua thực thể dữ liệu giao dịch thẻ tín dụng.

## <a name="import-credit-card-transactions"></a>Nhập giao dịch thẻ tín dụng

Để nhập giao dịch thẻ tín dụng, hãy làm theo các bước sau:

1. Trên trang **Giao dịch thẻ tín dụng**, chọn **Nhập giao dịch**. Nếu bạn đang mở quản lý dữ liệu lần đầu tiên, hệ thống phải cập nhật danh sách các thực thể dữ liệu trước khi bạn có thể tiếp tục.
2. Trong trường **Tên**, hãy nhập một thông tin mô tả duy nhất cho công việc nhập.
3. Trong trường **Định dạng dữ liệu nguồn**, chọn định dạng của tệp chứa giao dịch thẻ tín dụng để nhập.
4. Chọn **Tải lên** rồi tìm và chọn tệp để nhập.
5. Sau khi tệp đã được tải lên, hãy xác thực quá trình ánh xạ tệp giao dịch thẻ tín dụng và các cột của thực thể dữ liệu giao dịch thẻ tín dụng bằng cách chọn liên kết **Xem bản đồ** trên ngăn xếp. Nếu có lỗi ánh xạ hoặc nếu bạn phải thay đổi ánh xạ, hãy thực hiện các thay đổi về ánh xạ trong tab **Trực quan hóa ánh xạ** hoặc tab **Chi tiết ánh xạ**.
6. Để tự động hóa các giao dịch thẻ tín dụng, hãy chọn **Tạo tác vụ dữ liệu định kỳ**. Sau đó, bạn có thể đặt mức lặp lại để xác định tần suất nhập giao dịch thẻ tín dụng. Khi bạn hoàn thành, hãy chọn **ĐƯỢC RỒI**.
7. Để nhập tệp đã chọn ngay bây giờ, hãy chọn **Nhập**.
8. Nếu xảy ra lỗi trong quá trình nhập, bạn có thể xem nhật ký thực thi hoặc dữ liệu phân đoạn để xem các lỗi mà bạn phải sửa để giúp đảm bảo nhập thành công.

> [!NOTE]
> Nếu cần nhập nhiều định dạng tệp, bạn phải tạo các lệnh nhập riêng cho từng loại định dạng.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Chỉ định lại giao dịch thẻ tín dụng cho nhân viên bị chấm dứt hồ sơ

Sau khi hồ sơ nhân viên bị chấm dứt, tài khoản Dịch vụ miền Active Directory (AD DS) của nhân viên sẽ bị vô hiệu hóa. Tuy nhiên, có thể có các giao dịch thẻ tín dụng đang hoạt động vẫn phải được chi tiêu và hoàn trả. Trên trang **Giao dịch thẻ tín dụng**, bạn có thể chỉ định lại nhân viên cho bất kỳ giao dịch thẻ tín dụng nào mà nhân viên được liên kết đã bị chấm dứt.

Chọn một hoặc nhiều giao dịch thẻ tín dụng, sau đó chọn **Chỉ định lại giao dịch**. Sau đó, bạn có thể chọn một nhân viên khác để chỉ định giao dịch thẻ tín dụng. Sau khi chỉ định lại giao dịch thẻ tín dụng, bạn có thể chọn các giao dịch đó cho báo cáo chi phí và được thanh toán theo quy trình hoàn trả báo cáo chi phí thông thường.

## <a name="delete-credit-card-transactions"></a>Xóa các giao dịch thẻ tín dụng 

Đôi khi, sau khi nhập xong các giao dịch thẻ tín dụng, bạn có thể cần xóa một số giao dịch. Điều này có thể là do các giao dịch bị trùng lặp hoặc do dữ liệu không chính xác. Quản trị viên có thể sử dụng tính năng **"Xóa giao dịch thẻ tín dụng"** để chọn và xóa các giao dịch thẻ tín dụng **không đính kèm** với báo cáo chi phí. 

1. Đi đến **Nhiệm vụ định kỳ** > **Xóa giao dịch thẻ tín dụng**.
2. Chọn **Bộ lọc** và cung cấp thông tin để xác định các bản ghi cần đưa vào.
3. Chọn **OK** để xóa các bản ghi. 

## <a name="storing-credit-card-numbers"></a>Lưu trữ số thẻ tín dụng

Ba tùy chọn có sẵn để lưu trữ số thẻ tín dụng. Số thẻ tín dụng được lưu trữ trên **Các thông số quản lý chi phí** trang.

- **Ngăn nhập số thẻ** - Số thẻ tín dụng không được lưu trữ.
- **Số thẻ băm (lưu trữ bốn chữ số cuối cùng)** - Bốn chữ số cuối của số thẻ tín dụng được lưu trữ ở định dạng mã hóa.
- **Lưu trữ số thẻ** - Số thẻ tín dụng được lưu trữ ở định dạng không mã hóa. Tùy chọn này không tuân thủ Tiêu chuẩn bảo mật dữ liệu của ngành thẻ thanh toán (PCI) (DSS). Do đó, để giữ cho tổ chức của họ tuân thủ các quy định của PCI DSS, quản trị viên của tổ chức nên chọn không lưu trữ số thẻ tín dụng hoặc lưu trữ số thẻ băm.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
