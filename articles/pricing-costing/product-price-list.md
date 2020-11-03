---
title: Bảng giá sản phẩm
description: Chủ đề này cung cấp thông tin về bảng giá khi định giá theo danh mục, được sử dụng cho báo giá và hợp đồng dự án.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 504aa90bfb478207059b5e2894a3990f9a4a5e9e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087176"
---
# <a name="product-price-lists"></a>Bảng giá sản phẩm

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các thuộc tính bảng giá và hạng mục trong bảng giá hỗ trợ giá danh mục sản phẩm. Đối với hầu hết các phần, chức năng này dùng cho mô tả dựa trên danh mục trên báo giá dự án và hợp đồng dự án.

Đối với các mô tả dựa trên dự án, hợp đồng đại diện cho thỏa thuận sau khi thắng. Bởi vì quá trình đàm phán thường diễn ra trước khi thắng, nên giá đính kèm với báo giá luôn được sao chép ở dạng nguyên trạng vào bảng giá mới và đính kèm với hợp đồng. Bảng giá mới này không thể thay đổi được ngoài phạm vi của hợp đồng. Hạn chế này giúp bảo vệ bảng giá được thương lượng khỏi mọi thay đổi về giá xảy ra trong bảng giá chính.

Sản phẩm nên được thiết lập để có chi phí và bảng giá mặc định trong danh mục sản phẩm. Sử dụng giá niêm yết, chi phí tiêu chuẩn và chi phí hiện tại để đặt cấu hình chi phí và bảng giá mặc định. Bảng giá mặc định chỉ dùng trên mô tả báo giá hoặc mô tả hợp đồng dự án khi hệ thống không thể tìm thấy mô tả bảng giá cho sản phẩm đó trong bảng giá sản phẩm cho báo giá hoặc hợp đồng dự án.

Giá vốn của mô tả danh mục sản phẩm có thể thay đổi giữa các báo giá. Khả năng này rất quan trọng, bởi vì nếu không theo dõi chính xác chi phí, bạn không thể xác định lợi nhuận hoạt động trên các tương tác dự án. Theo mặc định, chi phí tiêu chuẩn của sản phẩm dùng làm giá vốn. Tuy nhiên, giá vốn mặc định có thể được cập nhật trên mô tả báo giá nếu có giá vốn khác cho báo giá đó.

## <a name="price-list-items"></a>Hạng mục trong bảng giá

Bạn có thể thêm sản phẩm từ danh mục sản phẩm vào bảng giá khác. Mô tả bảng giá cho sản phẩm luôn tham chiếu một đơn vị cụ thể. Giá cho một sản phẩm trên hạng mục trong bảng giá có thể được đặt cấu hình ở dạng khoản tiền tệ. Ngoài ra, giá này có thể được đặt cấu hình ở dạng chức năng của bảng giá, chi phí hiện tại hoặc chi phí tiêu chuẩn.

PSA hỗ trợ nhiều tùy chọn làm tròn khi giá được đặt cấu hình ở dạng chức năng của bảng giá, chi phí tiêu chuẩn hoặc chi phí hiện tại. Ngoài việc tận dụng nhiều phương pháp định giá và các tùy chọn làm tròn, bạn có thể liên kết danh sách giảm giá với các hạng mục trong bảng giá. 

Khi bạn tạo một bảng giá tùy chỉnh mới cho báo giá bằng cách chọn **Tạo định giá tùy chỉnh** trên trang **Báo giá dự án** , một bản sao của bảng giá sẽ được tạo và trường **Thực thể** trên tiêu đề của bảng giá mới sẽ được đặt thành **Thực thể bán hàng**. Tên của bảng giá mới được gắn với tên của báo giá và dấu thời gian. Bạn cũng có thể dùng tên của bảng giá mới và tên của báo giá trong quy trình làm việc tùy chỉnh để kích hoạt đánh giá hoặc phê duyệt bổ sung cho báo giá sử dụng giá tùy chỉnh.

 
## <a name="default-product-price-list"></a>Bảng giá sản phẩm mặc định
Mỗi bản ghi khách hàng có trường **Bảng giá mặc định** , nơi bạn có thể chỉ định bảng giá khớp với đơn vị tiền tệ của khách hàng. Giá trị mặc định sẽ không được nhập tự động vào trong trường này. Khi một thỏa thuận giá tùy chỉnh có khách hàng cụ thể tồn tại, bạn có thể dùng trường này để liên kết bảng giá với khách hàng đó.

Các thực thể Cơ hội, Báo giá và Hợp đồng dự án dùng các đơn hàng sau để nhập bảng giá sản phẩm mặc định. Cùng một thứ tự được dùng cho bảng giá sản phẩm.

1.  Báo giá
2.  Cơ hội
3.  Khách hàng
4.  Thiết đặt tổng thể 

Theo sản phẩm, trường **Sản phẩm** trên mô tả báo giá liệt kê tất cả sản phẩm hiện hoạt trong bảng giá sản phẩm của báo giá. Nếu sản phẩm đã bị hủy kích hoạt hoặc nếu đó là sản phẩm nháp, thì sản phẩm đó không được liệt kê ngay cả khi có trong bảng giá. 

Mô tả danh mục sản phẩm được thêm vào mô tả hóa đơn trên hóa đơn đầu tiên được tạo cho hợp đồng dự án. Trên hóa đơn nháp, những mô tả hóa đơn đó có thể bị xóa. Trong trường hợp đó, các mô tả sẽ xuất hiện trên hóa đơn tiếp theo cho đến khi chúng được lập hóa đơn hoặc cho đến khi hóa đơn được gửi đến khách hàng. Bạn không thể lập hóa đơn cho một phần số lượng theo dòng mô tả hóa đơn sản phẩm. Khi mô tả sản phẩm từ hóa đơn hợp đồng được lập hóa đơn, các số liệu thực tế sẽ được tạo. Tuy nhiên, các số liệu thực tế đó không liên kết với thực thể dự án liên quan. Nói cách khác, các mô tả hợp đồng dự án dựa trên sản phẩm độc lập với mọi việc sử dụng dựa trên dự án. Mức tiêu thụ vật liệu trên dự án sẽ không được theo dõi.
