---
title: điều chỉnh dự án
description: Bài viết này cung cấp thông tin về các điều chỉnh dự án.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788378"
---
# <a name="project-adjustments"></a>điều chỉnh dự án

_**Áp dụng cho:** Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_

## <a name="adjustments-overview"></a>Tổng quan về điều chỉnh

Bạn có thể định cấu hình Microsoft Dynamics 365 Project Operations để người dùng có thể thay đổi các giao dịch đã đăng. Bạn có thể điều chỉnh các giao dịch dự án riêng lẻ hoặc bạn có thể chọn nhiều giao dịch cùng một lúc trong danh sách tất cả các giao dịch dự án. Ví dụ, các điều chỉnh dự án được sử dụng để cập nhật hàng loạt trạng thái có thể lập hóa đơn, tính toán lại chi phí sau khi thay đổi cấu hình hoặc cập nhật các nguồn tài trợ.

Người dùng có thể truy cập chức năng điều chỉnh dự án theo nhiều cách:

- Bằng cách sử dụng trang **Điều chỉnh giao dịch** có thể truy cập từ **Quản lý dự án và kế toán** \> **Thiết lập**.
- Bằng cách sử dụng nút **Điều chỉnh** trên trang **Giao dịch dự án đã đăng** có thể được truy cập từ **Quản lý dự án và kế toán** \> **Giao dịch**.
- Bằng cách sử dụng nút **Điều chỉnh** trên trang **Giao dịch dự án đã đăng** trong ngữ cảnh của dự án. Có thể truy cập trang này từ **Quản lý dự án và kế toán** \> **Tất cả dự án**.

To allow for adjustments you must enable one or more transaction statuses from **Project Management and accounting** \> **Project Management and accounting paramaters** on the **General** tab under the section **Allow adjustment of transaction status**. Ví dụ về trạng thái giao dịch bao gồm giao dịch đã đăng, giao dịch đã lập hóa đơn hoặc giao dịch đã loại bỏ. Bất kỳ trạng thái giao dịch nào được đặt thành **Không** sẽ có các giao dịch ở trạng thái đó sẽ không xuất hiện trong quy trình điều chỉnh dưới dạng có thể chọn để điều chỉnh.

Tùy chọn cấu hình có tên **Luôn tạo giao dịch điều chỉnh** hiện có sẵn trong thông số kế toán và quản lý dự án. Bạn có thể tắt tùy chọn này để cập nhật giao dịch ban đầu thay vì tạo giao dịch mới trong quá trình điều chỉnh trong một tập hợp con các tình huống. Chúng tôi đã thông báo rằng thông số này sẽ không còn được dùng nữa trước ngày 1 tháng 3 năm 2023. Sau ngày 1 tháng 3 năm 2023, hệ thống sẽ luôn hoạt động như thể tùy chọn được bật.

## <a name="adjustments-process-flow"></a>Luồng quy trình điều chỉnh

Các bước sau đây cho thấy quy trình điển hình để xử lý các điều chỉnh.

1. Mở trang **Điều chỉnh dự án** .
2. Chọn **Chọn** để tìm kiếm các giao dịch đáp ứng tiêu chí điều chỉnh dự kiến.
3. Trong danh sách các giao dịch, hãy chọn tất cả các giao dịch hoặc một tập hợp con của các giao dịch để điều chỉnh.
4. Chọn **Điều chỉnh** và sửa đổi các thuộc tính trên dòng. Ngoài ra, nếu các giá trị được chỉ định thủ công trong quá trình nhập giao dịch, bạn có thể chọn nhập các giá trị hệ thống mặc định.
5. Danh sách các giao dịch được trả về và một dấu kiểm xuất hiện trong cột **Điều chỉnh đang chờ xử lý** để cho biết nơi các thay đổi đã được thực hiện. Mọi điều chỉnh có thay đổi đang chờ xử lý sẽ được hiển thị ở nửa dưới của trang. Ở đó, bạn có thể thực hiện các thay đổi chi tiết bổ sung ngoài những gì được hiển thị trên trang trước.
6. Chọn **Đăng** để đăng các giao dịch điều chỉnh.

Tùy thuộc vào cấu hình, các giao dịch mới thường được tạo để điều chỉnh.

- Trường **Trạng thái hóa đơn** của giao dịch ban đầu được đặt thành **Đã điều chỉnh**.
- Giao dịch đảo ngược được tạo để đảo ngược giao dịch ban đầu và trường **Trạng thái** được đặt thành **Đã điều chỉnh**.
- Một giao dịch mới được tạo có những thay đổi đã được thực hiện trong quá trình điều chỉnh.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Chọn nhiều giao dịch dự án đã đăng tại một thời điểm để điều chỉnh và ghi chú tín dụng

Một tính năng mới được giới thiệu trong bản phát hành 10.0.30 cho phép lựa chọn nhiều giao dịch để điều chỉnh cùng một lúc từ trang **Giao dịch dự án đã đăng** .

Trước khi bạn có thể sử dụng tính năng này, nó phải được bật trong hệ thống của bạn. Quản trị viên có thể sử dụng không gian làm việc **Quản lý tính năng** để kiểm tra trạng thái của tính năng và bật tính năng này nếu cần. Trong không gian làm việc **Quản lý tính năng**, tìm kiếm và chọn **Chọn nhiều giao dịch dự án đã đăng để điều chỉnh và ghi chú tín dụng**, rồi chọn **Bật ngay bây giờ**.

Tính năng này kích hoạt các chức năng chính sau:

- Nó có thể được truy cập từ trang giao dịch đã đăng trong một dự án bằng cách sử dụng nút **Điều chỉnh** hiện có.
- Nó cho phép kiểm soát chọn nhiều hàng trên trang **Giao dịch dự án đã đăng** . Bạn có thể áp dụng bộ lọc cho trang danh sách và chọn bản ghi của mình trước khi bắt đầu điều chỉnh.
- Nó sẽ tắt nút **Điều chỉnh** nếu không thể điều chỉnh bất kỳ giao dịch đơn lẻ nào hoặc nếu bạn chọn kết hợp ghi chú tín dụng và nhật ký cùng nhau thay vì riêng lẻ.
- Do có thêm điều khiển chọn nhiều hàng, liên kết **Chi phí cam kết** trong dải băng không còn bị tắt nếu nhiều hàng được chọn.
- Nó thêm thông báo cảnh báo sau: "Bạn đã chọn nhiều hơn (số đã chọn) bản ghi để điều chỉnh. Tiếp tục với hành động này có thể mất một thời gian. Bạn có chắc chắn muốn tiếp tục với hành động này không?"

Tính năng này cũng loại bỏ bước 2 khỏi dòng quy trình đã được mô tả trước đó trong bài viết này. Do đó, bất kỳ giao dịch nào được chọn trước khi trang **Điều chỉnh giao dịch** được mở sẽ được đưa vào danh sách các giao dịch để điều chỉnh. Bạn không cần phải sử dụng nút **Chọn** để tìm kiếm chúng.

> [!NOTE] 
> Ngay cả khi tính năng này bị tắt, bạn vẫn có thể chọn nhiều bản ghi để điều chỉnh. Tuy nhiên, chỉ một bản ghi sẽ *được chọn* và hộp thoại **Chọn giao dịch** sẽ xuất hiện ngay sau khi bạn chọn điều chỉnh mở.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Trạng thái giao dịch điều chỉnh có thể được bật hoặc tắt để điều chỉnh

Bạn có thể bật hoặc tắt các trạng thái sau trên tab **Chung** của trang **Thông số kế toán và quản lý dự án** :

- Đã đăng
- Đề xuất hóa đơn
- Đã xuất hóa đơn
- Ước tính
- Loại bỏ
- Số dư đầu kỳ (giờ)

## <a name="adjustment-parameters"></a>Thông số điều chỉnh

Các thông số này được liệt kê trên trang **Thông số kế toán và quản lý dự án** trên tab **Chung** trong phần **Adjustment** group và sẽ sửa đổi hành vi đối với cách xử lý các điều chỉnh. 

| Tên tham số | Description |
|----------------|-------------
| Luôn tạo giao dịch điều chỉnh | Nếu bật tham số này, quá trình điều chỉnh sẽ luôn tạo giao dịch đảo ngược mới và giao dịch điều chỉnh mới khi có tác động tài chính hoặc báo cáo. Nếu tham số bị vô hiệu hóa, quá trình điều chỉnh sẽ cập nhật giao dịch ban đầu thay vì tạo giao dịch đảo ngược và giao dịch mới cho một kịch bản chẳng hạn như cập nhật văn bản giao dịch. |
| Trường tự động cập nhật | Nếu kích hoạt tham số này, hệ thống sẽ tính lại giá vốn và giá bán. |
| Sử dụng ngày điều chỉnh làm dự án mới | Tham số này được sử dụng để chuyển giao dịch sang tương lai kỳ tài chính trước khi hệ thống hỗ trợ chức năng này. Chúng tôi khuyên bạn không nên sử dụng nó vì nó thay đổi ngày làm việc của giao dịch và sẽ không được dùng nữa trong bản phát hành trong tương lai. |
| Cho phép các hoạt động đã đóng | Thông thường, không thể tạo giao dịch cho các hoạt động đã đóng. Nếu tham số này được bật, hành vi đó sẽ bị ghi đè. Do đó, có thể tạo các điều chỉnh cho các hoạt động đã đóng. |
