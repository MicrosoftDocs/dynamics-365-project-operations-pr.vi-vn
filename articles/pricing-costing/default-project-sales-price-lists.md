---
title: Bảng giá mặc định
description: Bài viết này cung cấp thông tin về danh sách giá bán và chi phí mặc định trong Hoạt động Dự án.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410289"
---
# <a name="default-price-lists"></a>Bảng giá mặc định

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

## <a name="sales-price-lists"></a>Bảng giá bán hàng

Mọi báo giá dự án và hợp đồng trong Dynamics 365 Project Operations chứa một bảng giá bán hàng mặc định. 

### <a name="price-list-default-on-project-quotes"></a>Bảng giá mặc định trên báo giá dự án
Hệ thống hoàn tất quá trình sau để xác định bảng giá nào được đặt mặc định trên báo giá dự án:

1. Hệ thống xem xét các bảng giá được đính kèm với bảng giá dự án của tài khoản. 
1. Nếu không có bảng giá dự án nào kèm theo hồ sơ tài khoản, hệ thống tra cứu các bảng giá bán kèm theo thông số dự án khớp với đơn vị tiền tệ báo giá dự án.
1. Tiếp theo, hệ thống kiểm tra khoảng ngày hiệu lực của các bảng giá khớp với phạm vi ngày của báo giá dự án. Cụ thể là ngày tạo báo giá.
1. Nếu có nhiều bảng giá có hiệu lực đối với ngày của báo giá dự án, thì tất cả các bảng giá đó đều được đặt mặc định trên báo giá dự án.
1. Nếu không có bảng giá nào có hiệu lực đối với ngày của báo giá dự án, thì sẽ không có bảng giá dự án mặc định nào trên báo giá dự án. Một thông báo cảnh báo sẽ xuất hiện trên báo giá dự án. Thông báo cho biết các giá trị thực tế và ước tính trên dự án sẽ không được định giá vì không có bảng giá dự án nào được đính kèm.

### <a name="price-list-default-on-project-contracts"></a>Bảng giá mặc định trên hợp đồng dự án 
Hệ thống hoàn tất quá trình sau để xác định bảng giá nào được đặt mặc định trên hợp đồng dự án:

1. Nếu hợp đồng được tạo từ báo giá, thì các bảng giá dự án trên báo giá sẽ được sao chép riêng và được đính kèm với hợp đồng dự án.
1. Nếu hợp đồng được tạo từ đầu, thì hệ thống sẽ xem xét các bảng giá được đính kèm với bảng giá dự án của tài khoản. Nếu không có bảng giá dự án nào được đính kèm với bản ghi tài khoản, thì hệ thống sẽ tìm các bảng giá bán hàng được đính kèm với tham số dự án khớp với đơn vị tiền tệ trong hợp đồng dự án.
1. Tiếp theo, hệ thống kiểm tra khoảng ngày hiệu lực của các bảng giá khớp với phạm vi ngày của hợp đồng dự án. Cụ thể là ngày tạo hợp đồng.
1. Nếu có nhiều bảng giá có hiệu lực đối với ngày của hợp đồng, thì tất cả các bảng giá đó đều được đặt mặc định trên hợp đồng.
1. Nếu không có bảng giá nào có hiệu lực đối với ngày của hợp đồng, thì sẽ không có bảng giá dự án nào được đặt mặc định trên hợp đồng. Một thông báo cảnh báo sẽ xuất hiện trên hợp đồng dự án. Thông báo cho biết các giá trị thực tế và ước tính trên dự án sẽ không được định giá vì không có bảng giá dự án nào được đính kèm.

## <a name="cost-price-lists"></a>Bảng giá vốn

Bảng giá vốn không được đặt mặc định cho bất kỳ thực thể nào trong Project Operations. Việc xác định bảng giá chi phí sử dụng cho các chi phí của dự án luôn được thực hiện trên cơ sở từng giao dịch. Hệ thống hoàn tất quá trình sau để xác định bảng giá sẽ dùng cho chi phí dự án:

1. Hệ thống tra cứu các bảng giá được đơn vị tổ chức nhận thầu của công trình kèm theo.
1. Tiếp theo, hệ thống sẽ xem xét tính hiệu quả theo ngày của các bảng giá khớp với ngày trong bối cảnh ước tính hoặc bối cảnh thực tế.

    - *Ước tính bối cảnh* đề cập đến bất kỳ bối cảnh nào trong ba bối cảnh ước tính trong Hoạt động dự án:

        - Dòng ước tính dự án
        - Chi tiết mô tả báo giá
        - Chi tiết mô tả hợp đồng

    - *Bối cảnh thực tế* đề cập đến bất kỳ nguồn nào trong ba nguồn về thực tế trong Hoạt động Dự án:

       - Nhập các dòng nhật ký được tạo thủ công hoặc các dòng nhật ký sửa được tạo trong nhật ký sửa
       - Các dòng nhật ký được tạo trong quá trình gửi nhật ký sử dụng thời gian, chi phí hoặc vật liệu
       - Chi tiết dòng hóa đơn

    Khi Hoạt động Dự án khớp với hiệu quả ngày của dòng nhật ký đến hoặc chi tiết dòng hóa đơn trong *bối cảnh thực tế*, nó sử dụng **Ngày Giao dịch** đồng ruộng.

    - Nếu nhiều danh sách giá có hiệu lực cho ngày ngữ cảnh ước tính đến hoặc ngữ cảnh thực tế, thì danh sách giá được tạo gần đây nhất sẽ được chọn.
    - Nếu không có bảng giá nào được đính kèm với đơn vị tổ chức nhận thầu của dự án, hệ thống sẽ tìm kiếm bảng giá được đính kèm với các thông số của dự án phù hợp với đơn vị tiền tệ của dự án.

## <a name="enable-multi-currency-cost-price-list"></a>Bật bảng giá vốn theo nhiều loại tiền tệ

Cài đặt này có thể được tìm thấy tại **Cài đặt** \> **Thông số**. Giá trị mặc định là **Không**.

Khi cài đặt này được bật (nghĩa là, giá trị được đặt thành **Đúng**), hệ thống hoạt động theo cách sau:

- Nó cho phép các bảng giá chi phí bằng bất kỳ đơn vị tiền tệ nào được liên kết với đơn vị tổ chức. Ví dụ: bảng giá chi phí bằng đơn vị tiền tệ EUR có thể được đính kèm với một đơn vị tổ chức bằng đơn vị tiền tệ USD. Hệ thống sẽ tiếp tục xác nhận rằng các bảng giá chi phí được đính kèm với một đơn vị tổ chức không có hiệu lực trùng lặp về ngày tháng.
- Nó xác nhận rằng các bảng giá chi phí được đính kèm với các thông số dự án không có hiệu lực ngày trùng lặp, ngay cả khi chúng có các đơn vị tiền tệ khác nhau. Hành vi này khác với hành vi mặc định (nghĩa là, hành vi khi giá trị được đặt thành **Không**). Trong hành vi mặc định, chỉ những danh sách giá vốn có **tương tự** đơn vị tiền tệ được xác thực về tính hiệu quả của ngày tháng không trùng lặp.
- Đối với bối cảnh giao dịch đến, nó xác định bảng giá chi phí chỉ dựa trên tính hiệu quả của ngày. Hành vi này khác với hành vi mặc định, trong đó hệ thống chọn bảng giá chi phí phù hợp với cả đơn vị tiền tệ của dự án và tính hiệu quả của ngày tháng.

Do những thay đổi trong hành vi này, khách hàng của Bộ phận Vận hành Dự án sẽ có thể duy trì một bảng giá chi phí toàn cầu phù hợp với toàn công ty. Họ sẽ không phải có bảng giá theo từng đơn vị tiền tệ hoạt động. Danh sách giá toàn cầu sẽ có hiệu lực theo ngày và sẽ cho phép thiết lập tỷ lệ chi phí bằng bất kỳ đơn vị tiền tệ nào cho sự kết hợp cụ thể của các giá trị thứ nguyên đặt giá. Đơn vị tiền tệ của danh sách giá vốn chỉ được sử dụng để nhập các giá trị mặc định khi **Giá vai trò**, **thể loại**, và **Bảng giá** các bản ghi mục được tạo. Nó sẽ không được sử dụng để xác định bảng giá.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
