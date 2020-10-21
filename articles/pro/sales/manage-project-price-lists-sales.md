---
title: Quản lý bảng giá dự án trên báo giá dự án
description: Chủ đề này cung cấp thông tin về cách làm việc với bảng giá dự án trên báo giá. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966888"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Quản lý bảng giá dự án trên báo giá dự án (Bán hàng)

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Báo giá dự án được thiết kế để hỗ trợ nhiều bảng giá bán hàng hiệu quả theo ngày. Với Dynamics 365 Project Operations, một thực thể liên kết mới có tên **Bảng giá dự án** được thêm vào. Thực thể này có mối quan hệ 1 - nhiều với báo giá dự án.

Bảng giá dự án được sử dụng để định giá các giao dịch thời gian và chi phí trên một dự án. Khi một báo giá có một hoặc nhiều bảng giá dự án, những bảng giá này được sử dụng để định giá ước tính thời gian và chi phí, cũng như giá trị thực tế cho các dự án được liên kết với báo giá thông qua mô tả báo giá.

Khi không có bảng giá dự án trên báo giá dự án, bạn sẽ nhận được thông báo cảnh báo. Thông báo nói rằng vì không có bảng giá dự án, công việc và chi phí dự án ước tính và thực tế của bạn sẽ không được định giá. Thay vào đó, chúng sẽ có giá bằng không (0) cho các giá trị bán hàng.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Liên kết hoặc tách bảng giá dự án trên báo giá dự án

Để tạo hoặc chọn một bảng giá cụ thể cho việc ước tính công việc và chi phí theo dự án, hãy hoàn thành các bước sau.

1. Trên báo giá, hãy chọn tab **Giá dự án** và trong lưới con, chọn **+ Thêm bảng giá dự án mới**.
2. Trên trang Tạo nhanh, hãy chọn một bảng giá. Danh sách thả xuống hiển thị tất cả các bảng giá có ngữ cảnh được đặt thành **Bán hàng** và đơn vị tiền tệ khớp với đơn vị tiền tệ trên báo giá.
4. Nhập mô tả cho liên kết bảng giá dự án và chọn **Lưu và đóng**.

Liên kết bảng giá dự án được tạo.

Bạn có thể lặp lại quy trình này nếu bạn cần liên kết nhiều hơn một bảng giá dự án với báo giá dự án. Chỉ tạo nhiều bảng giá dự án nếu bạn có các ngày có hiệu lực khác nhau trên mỗi bảng giá dự án được liên kết.

> [!NOTE]
> Project Operations không hỗ trợ ngày hiệu lực của bảng giá dự án chồng chéo nhau. Nếu có nhiều bảng giá dự án cho một giao dịch với ngày nhất định, giá của giao dịch đó sẽ được đặt mặc định là không (0).
Để loại bỏ liên kết bảng giá dự án, hãy chọn bảng giá dự án rồi chọn **Xóa bảng giá dự án trên báo giá**. Bảng giá được xóa khỏi bảng giá dự án của báo giá, nhưng bản thân bảng giá không bị xóa. Chỉ có liên kết đến báo giá bị xóa.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Thiết lập bảng giá dự án mặc định trên báo giá

Bảng giá dự án có thể được thiết lập mặc định trên báo giá dự án. Thiết lập này đảm bảo rằng tất cả các báo giá trong tổ chức của bạn luôn bắt đầu bằng một bảng giá chuẩn cho khoảng thời gian giá đó.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Thiết lập giá trị mặc định tổ chức cho bảng giá dự án

1. Đi đến **Thiết đặt** > **Tổng quát** > **Tham số**.
2. Trên trang danh sách **Tham số hiện hoạt**, tìm bản ghi rồi nhấp đúp để mở. 
3. Trên trang **Tham số**, chọn tab **Bảng giá**. Bạn có thể thấy danh sách các bảng giá mặc định được hiển thị. Đây là danh sách chi phí tiêu chuẩn và bảng giá bán hàng. Việc có một bảng giá bán hàng được liên kết tại đây cho mọi đơn vị tiền tệ mà bạn bán hàng sẽ đảm bảo rằng bảng giá bán hàng này được đặt mặc định trên bất kỳ báo giá nào bạn tạo cho khách hàng giao dịch bằng đơn vị tiền tệ này.

### <a name="set-up-customer-specific-project-price-lists"></a>Thiết lập bảng giá dự án dành riêng cho khách hàng

Bảng giá dự án dành riêng cho khách hàng cũng có thể được thiết lập khi bạn đã thương lượng thỏa thuận giá chính với khách hàng của mình.

Để thiết lập bảng giá dự án dành riêng cho khách hàng, hãy hoàn thành các bước sau.

1. Trong phần **Bán hàng**, chọn **Khách hàng**.
2. Trong danh sách các tài khoản hiện hoạt của bạn, hãy chọn và mở bản ghi khách hàng mà bạn có bảng giá đặc biệt.
3. Trên tab **Bảng giá dự án**, bạn có thể tạo liên kết bảng giá mới để có bảng giá dự án dành riêng cho khách hàng này.

## <a name="create-custom-pricing-on-a-project-quote"></a>Tạo giá tùy chỉnh trên báo giá dự án

Sau khi bạn có bảng giá dự án mặc định cho tổ chức và dành riêng cho khách hàng, báo giá dự án của bạn sẽ tự động được tạo với các liên kết bảng giá dự án này. Tuy nhiên, trong một số trường hợp nhất định, bạn có thể cần tạo giá tùy chỉnh cho báo giá dự án cụ thể. 

1. Trên **Báo giá dự án**, trên tab **Bảng giá dự án**, hãy xác minh trên lưới con là không có bản ghi bảng giá cụ thể nào được chọn.
2. Chọn **Tạo nội dung định giá tùy chỉnh**. Thao tác này sẽ tạo bản sao của tất cả các bảng giá tiêu chuẩn hiện được liên kết với báo giá và liên kết các bản sao này với báo giá. Các liên kết hiện có với bảng giá tiêu chuẩn sẽ bị loại bỏ. Sau đó, nhân viên bán hàng có thể bắt đầu chỉnh sửa giá trên các bản sao này. Các mức giá thay đổi này sẽ chỉ áp dụng cho báo giá dự án này.
