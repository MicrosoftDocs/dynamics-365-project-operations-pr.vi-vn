---
title: Tạo và áp dụng các điều khoản lưu giữ khoản thanh toán cho nhà cung cấp
description: Chủ đề này cung cấp thông tin về cách thiết lập và duy trì các điều khoản lưu giữ đối với khoản thanh toán của nhà cung cấp.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3961d18fcd53381ad43a1d3e598ac61652ba9843
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685128"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Tạo và áp dụng các điều khoản lưu giữ khoản thanh toán cho nhà cung cấp

[!include [banner](../includes/banner.md)] 

Việc thiết lập các điều khoản lưu giữ khoản thanh toán cho nhà cung cấp cho một dự án sẽ hữu ích khi tổ chức của bạn muốn giữ lại một phần khoản thanh toán cho nhà cung cấp. Chẳng hạn, bạn muốn giữ khoản thanh toán cho nhà cung cấp cho đến khi sản phẩm được giao đáp ứng được kỳ vọng của bạn. Điều khoản lưu giữ khoản thanh toán cho nhà cung cấp có thể được chỉ định khi bạn thương lượng hợp đồng với nhà cung cấp.

## <a name="create-vendor-payment-retention-terms"></a>Tạo điều khoản lưu giữ khoản thanh toán cho nhà cung cấp

Bạn có thể nhập tỷ lệ phần trăm khoản thanh toán cho nhà cung cấp sẽ giữ lại và tỷ lệ phần trăm số tiền đã giữ lại trước đây sẽ được giải phóng. Số tiền sẽ tự động được giữ lại trên hóa đơn của nhà cung cấp cho đến khi hợp đồng đạt đến trạng thái hoàn thành được chỉ định. Sau khi bạn thiết lập các điều khoản lưu giữ, bạn có thể áp dụng chúng cho bất kỳ dự án nào của nhà cung cấp đó.

Hãy sử dụng các bước sau để thiết lập và duy trì các điều khoản lưu giữ khoản thanh toán cho nhà cung cấp. 

1. Chuyển tới **Quản lý dự án và kế toán** > **Lưu giữ** > **Điều khoản lưu giữ khoản thanh toán cho nhà cung cấp**.
2. Chọn **Mới** để thêm điều khoản lưu giữ mới. Giá trị **ID quy tắc** cho điều khoản mới sẽ được nhập tự động. 
3. Nhập phần mô tả ngắn gọn vào trường **Mô tả** và trên FastTab **Điều khoản**, hãy chọn **Thêm dòng** để nhập các giá trị điều khoản cho những mục sau:

   - **Phần trăm đơn vị được giao**: Nhập tỷ lệ phần trăm hoàn thành cho điều khoản. Số tiền sẽ tự động được giữ lại trên hóa đơn của nhà cung cấp cho đến khi giai đoạn hoàn thành của dự án đạt đến tỷ lệ phần trăm đã chỉ định. Chẳng hạn, nếu bạn nhập 50, thì số tiền sẽ được giữ lại cho đến khi dự án hoàn thành 50 phần trăm.
   - **Tỷ lệ phần trăm giữ lại**: Nhập tỷ lệ phần trăm số tiền sẽ được giữ lại trên hóa đơn của nhà cung cấp. Lấy ví dụ, nếu bạn nhập 10, thì 10 phần trăm số tiền trên hóa đơn của nhà cung cấp sẽ được giữ lại cho đến khi dự án đạt được tỷ lệ phần trăm hoàn thành như đã đặt trong trường **Phần trăm đơn vị được giao**.
   - **Tỷ lệ phần trăm sẽ giải phóng**: Chọn **Thêm dòng** để nhập tỷ lệ phần trăm của bất kỳ số tiền nào đã giữ lại trước đây sẽ được giải phóng khi dự án đạt đến mức độ hoàn thành đã chọn.

> [!NOTE]
> Nếu bạn có nhiều mốc cho các mức độ hoàn thành dự án khác nhau, hãy nhập một dòng điều khoản lưu giữ riêng biệt cho mỗi quy tắc lưu giữ. Mỗi dòng có thể chỉ định một tỷ lệ phần trăm lưu giữ khác nhau và một tỷ lệ phần trăm giải phóng khác nhau đối với mỗi mức độ hoàn thành dự án được chỉ định.

Sau khi bạn thiết lập các điều khoản lưu giữ cho nhà cung cấp, bạn có thể áp dụng chúng cho dự án.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Áp dụng điều khoản lưu giữ cho dự án của nhà cung cấp

1. Chuyển tới **Quản lý dự án và kế toán** > **Dự án** > **Tất cả dự án** và mở một dự án trong trang danh sách dự án.
2. Trên FastTab **Thỏa thuận của nhà cung cấp**, hãy chọn **Thêm dòng**.
3. Ở trường **Mã tài khoản**, hãy chọn một trong các tùy chọn sau: 

   - **Bảng**: Các điều khoản lưu giữ được áp dụng cho một nhà cung cấp.
   - **Nhóm**: Các điều khoản lưu giữ được áp dụng cho tất cả các nhà cung cấp trong một nhóm nhà cung cấp.
   - **Tất cả**: Các điều khoản lưu giữ được áp dụng cho tất cả các nhà cung cấp.

4. Ở trường **Nhà cung cấp/nhóm nhà cung cấp**, hãy chọn nhà cung cấp hoặc nhóm nhà cung cấp sẽ được áp dụng các điều khoản lưu giữ. Nếu bạn đã chọn **Tất cả** ở bước trước, thì trường này sẽ không khả dụng.
5. Ở trường **Điều khoản lưu giữ cho nhà cung cấp**, hãy chọn các điều khoản lưu giữ mà bạn đã tạo trong quy trình trước.
6. Nếu dự án cũng được thiết lập các điều khoản trả tiền khi được trả tiền (PWP) cho nhà cung cấp, hãy nhập tỷ lệ phần trăm ngưỡng cho dự án trong trường **Tỷ lệ phần trăm ngưỡng PWP**.

Các điều khoản lưu giữ cho nhà cung cấp cũng được hiển thị trên các đơn đặt hàng mà bạn tạo cho nhà cung cấp.


[!INCLUDE[footer-include](../includes/footer-banner.md)]