---
title: Quản lý bảng giá dự án trên hợp đồng dự án
description: Chủ đề này cung cấp thông tin về cách quản lý bảng giá dự án trên hợp đồng dự án.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffc48782394995781535ae56142dc76afeb9a040
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858589"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Quản lý bảng giá dự án trên hợp đồng dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hợp đồng dự án trong Dynamics 365 Project Operations được thiết kế để hỗ trợ nhiều bảng giá bán hàng có hiệu lực theo ngày trên hợp đồng. Trong Project Operations, có một thực thể liên kết mới có tên là **Bảng giá dự án**. Thực thể này có mối quan hệ một-nhiều đối với hợp đồng dự án.

Bảng giá dự án được dùng để định giá các giao dịch về thời gian, vật tư và chi phí cho một dự án. Khi hợp đồng có một hoặc nhiều bảng giá dự án, các bảng giá này sẽ được dùng để định giá cho các số liệu ước tính và thực tế về thời gian, vật tư, chi phí của các dự án liên quan đến hợp đồng thông qua mục mô tả hợp đồng.

Khi không có bảng giá dự án trong hợp đồng dự án, bạn sẽ thấy thông báo cảnh báo rằng không có bảng giá dự án nào và các số liệu ước tính, công việc thực tế của dự án, vật tư và chi phí đã ghi lại sẽ không được định giá. Sẽ không có mức giá cho các giá trị doanh thu.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Liên kết hoặc hủy liên kết bảng giá dự án trên một hợp đồng dự án

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Tạo hoặc liên kết một bảng giá cụ thể để ước tính công việc, vật tư và chi phí dựa trên dự án

1. Trên hợp đồng dự án, hãy chọn tab **Bảng giá dự án**.
2. Trong lưới con, hãy chọn **+ Thêm bảng giá dự án mới**.
3. Trên thanh trượt **Tạo nhanh**, chọn một bảng giá. 

  Danh sách thả xuống hiển thị tất cả các bảng giá có ngữ cảnh được đặt thành **Bán hàng**, trong đó đơn vị tiền tệ trên bảng giá khớp với đơn vị tiền tệ trên hợp đồng.
  
4. Nhập mô tả cho liên kết bảng giá dự án, chọn **Tiết kiệm**, sau đó đóng thanh trượt **Tạo nhanh**.

   Liên kết bảng giá dự án được tạo.
   
5. Lặp lại các bước từ 1 đến 4 để liên kết nhiều bảng giá dự án với hợp đồng dự án. Chỉ tạo nhiều bảng giá dự án nếu ngày có hiệu lực của từng bảng giá được liên kết là khác nhau.

> [!NOTE]
> Project Operations không hỗ trợ trường hợp các ngày có hiệu lực của bảng giá dự án bị chồng chéo. Nếu nhiều bảng giá dự án của một giao dịch có chung một ngày cụ thể, thì mức giá của giao dịch đó sẽ được đặt mặc định là 0.

### <a name="remove-a-project-price-list-association"></a>Hủy liên kết bảng giá dự án

- Chọn bảng giá dự án, sau đó chọn **Xóa bảng giá dự án hợp đồng** trên lưới con. 

  Bảng giá sẽ được xóa khỏi các bảng giá của dự án trên hợp đồng. Bản thân bảng giá sẽ không bị xóa. Chỉ sự liên kết giữa bảng giá với hợp đồng bị xóa.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Thiết lập để tự động đặt các bảng giá dự án làm bảng giá mặc định trên hợp đồng

Có thể thiết lập bảng giá dự án làm bảng giá dự án mặc định. Sự thiết lập này đảm bảo rằng tất cả các hợp đồng trong tổ chức của bạn luôn bắt đầu với một bảng giá dự án tiêu chuẩn cho khoảng thời gian có giá đó.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Thiết lập bảng giá mặc định của tổ chức cho bảng giá dự án

1. Chuyển đến **Cài đặt** > **Chung**, sau đó chọn **Tham số**.
2. Trên trang danh sách **Tham số hoạt động**, chọn và bấm đúp vào hồ sơ để mở hồ sơ. Trong khi bấm đúp, hãy đảm bảo bạn không bấm vào giá trị trường là siêu liên kết. 
3. Trên trang **Tham số hoạt động**, chọn tab **Bảng giá**. Một lưới con hiển thị danh sách các bảng giá mặc định sẽ xuất hiện. Đây là bảng kê giá vốn và giá bán tiêu chuẩn. Việc có một bảng kê giá **Bán** tại đây cho mỗi đơn vị tiền tệ mà bạn bán hàng theo đó sẽ đảm bảo rằng bảng giá bán hàng là bảng giá mặc định trên bất kỳ hợp đồng nào bạn tạo cho khách hàng giao dịch bằng đơn vị tiền tệ này.

### <a name="set-up-a-customer-specific-project-price-list"></a>Thiết lập bảng giá dự án dành riêng cho khách hàng

Bạn cũng có thể thiết lập bảng giá dự án dành riêng cho khách hàng khi đã thương lượng được một mức giá cơ bản với khách hàng.

1. Chuyển đến **Bán hàng** > **Khách hàng**.
2. Trong danh sách các khách hàng hiện hoạt, hãy chọn khách hàng có bảng giá riêng.
3. Chọn hồ sơ khách hàng đó để mở hồ sơ rồi chọn tab **Bảng giá dự án**. Một lưới con hiển thị danh sách bảng giá dự án cụ thể cho khách hàng này sẽ xuất hiện. 
4. Tạo một liên kết bảng giá mới tại đây để có bảng giá dự án dành riêng cho khách hàng này.

## <a name="custom-pricing-on-a-project-contract"></a>Mức giá tùy chỉnh trên hợp đồng dự án

Sau khi bạn có bảng giá dự án mặc định cho tổ chức và khách hàng cụ thể, các hợp đồng dự án của bạn sẽ tự động được tạo với các liên kết bảng giá dự án này. Tuy nhiên, các bảng giá dự án trong hợp đồng dự án sẽ luôn được sao chép cùng với ngày tháng và tên hợp đồng được gắn kèm. Khi đó, người quản lý dự án và khách hàng có thể bắt đầu chỉnh sửa mức giá trên các bản sao nói trên. Các mức giá đã thay đổi sẽ chỉ áp dụng cho hợp đồng dự án này.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
