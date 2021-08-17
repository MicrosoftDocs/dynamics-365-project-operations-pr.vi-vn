---
title: Nhập và duy trì các giao dịch thẻ tín dụng
description: Chủ đề này giải thích cách nhập và duy trì các giao dịch thẻ tín dụng liên quan đến chi phí. Bạn có thể thiết lập để các giao dịch này được nhập tự động theo lịch trình định kỳ hoặc được nhập thủ công khi cần.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c3a53d2ae4eae411364aaf68ac806b55335c75d4870a24715954ccae327f4358
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995877"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Nhập và duy trì các giao dịch thẻ tín dụng

Các giao dịch thẻ tín dụng liên quan đến chi phí có thể được thiết lập để tự động nhập vào theo lịch trình định kỳ. Ngoài ra, có thể nhập giao dịch theo cách thủ công khi cần. Các giao dịch thẻ tín dụng được nhập thông qua thực thể dữ liệu giao dịch thẻ tín dụng.

Để biết thêm thông tin về thực thể dữ liệu, hãy xem [Thực thể dữ liệu](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Nhập giao dịch thẻ tín dụng

1. Trên trang **Giao dịch thẻ tín dụng**, chọn **Nhập giao dịch**. Nếu bạn mở tác vụ quản lý dữ liệu lần đầu tiên, hệ thống phải cập nhật danh sách các thực thể dữ liệu trước khi bạn có thể tiếp tục.
2. Trong trường **Tên**, nhập mô tả riêng của tác vụ nhập.
3. Trong trường **Định dạng dữ liệu nguồn**, chọn định dạng của tệp chứa giao dịch thẻ tín dụng để nhập.
4. Chọn **Tải lên** rồi tìm và chọn tệp để nhập.
5. Sau khi tệp đã được tải lên, hãy xác thực ánh xạ của tệp giao dịch thẻ tín dụng và các cột của thực thể dữ liệu giao dịch thẻ tín dụng bằng cách chọn liên kết **Xem bản đồ** trên ngăn xếp. Nếu có lỗi ánh xạ hoặc nếu bạn phải thay đổi ánh xạ, hãy thực hiện các thay đổi về ánh xạ trong tab **Trực quan hóa ánh xạ** hoặc tab **Chi tiết ánh xạ**.
6. Để tự động hóa các giao dịch thẻ tín dụng, hãy chọn **Tạo tác vụ dữ liệu định kỳ**. Sau đó, bạn có thể đặt mức lặp lại để xác định tần suất nhập giao dịch thẻ tín dụng. Sau khi hoàn tất, hãy chọn **OK**.
7. Để nhập tệp đã chọn ngay bây giờ, hãy chọn **Nhập**.
8. Nếu lỗi xảy ra trong quá trình nhập, bạn có thể xem nhật ký thực thi hoặc dữ liệu giai đoạn, tại đó có các lỗi mà bạn phải sửa để đảm bảo quá trình nhập diễn ra thành công.

> [!NOTE]
> Nếu bạn phải nhập nhiều định dạng tệp, bạn phải tạo tác vụ nhập riêng cho từng loại định dạng.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Chỉ định lại giao dịch thẻ tín dụng cho nhân viên bị chấm dứt hồ sơ

Sau khi hồ sơ nhân viên bị chấm dứt, tài khoản Dịch vụ miền Active Directory (AD DS) của nhân viên đó sẽ bị vô hiệu hóa. Tuy nhiên, có thể có các giao dịch thẻ tín dụng đang hoạt động vẫn phải được chi tiêu và hoàn trả. Từ trang **Giao dịch thẻ tín dụng**, bạn có thể chỉ định lại nhân viên cho bất kỳ giao dịch thẻ tín dụng nào mà nhân viên liên quan đã bị chấm dứt hồ sơ.

Chọn một hoặc nhiều giao dịch thẻ tín dụng, sau đó chọn **Chỉ định lại giao dịch**. Sau đó, bạn có thể chọn một nhân viên khác để chỉ định giao dịch thẻ tín dụng. Sau khi chỉ định lại giao dịch thẻ tín dụng, bạn có thể chọn các giao dịch đó cho báo cáo chi phí và được thanh toán theo quy trình hoàn trả báo cáo chi phí thông thường.


[!INCLUDE[footer-include](../includes/footer-banner.md)]