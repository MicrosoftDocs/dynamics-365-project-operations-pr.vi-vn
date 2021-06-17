---
title: Tạo hợp đồng nâng cao để thanh toán dựa trên tiến độ
description: Chủ đề này giải thích cách tạo hợp đồng dự án để bạn có thể tạo hóa đơn cho khách hàng, dựa trên phần trăm công việc đã hoàn thành.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999697"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Tạo hợp đồng nâng cao để thanh toán dựa trên tiến độ
[!include [banner](../includes/banner.md)]

Chủ đề này giải thích cách tạo hợp đồng dự án để bạn có thể tạo hóa đơn cho khách hàng, dựa trên phần trăm công việc đã hoàn thành. Số tiền trong hóa đơn được tính toán tự động cho các hạng mục ngân sách của công việc mà bạn thiết lập cho một dự án. Thời gian lập hóa đơn được đặt khi bạn thương lượng hợp đồng dự án với khách hàng.

Sử dụng các quy trình trong chủ đề này để thiết lập một hợp đồng, một dự án liên quan và các quy tắc thanh toán để tính toán số tiền trên hóa đơn cho các hạng mục ngân sách của công việc mà bạn thiết lập cho dự án.

Sau khi tạo hợp đồng và dự án, bạn có thể thiết lập các chi tiết của dự án. Ví dụ: bạn có thể xác định các hoạt động và chỉ định nhân viên cho dự án.

## <a name="example"></a>Ví dụ:

Tổ chức của bạn là một công ty phát triển phần mềm. Bạn đồng ý phát triển gói kế toán tính lương cho một khách hàng với tổng phí là 20.000 đô la Mỹ (USD). Tổ chức của bạn đồng ý xuất hóa đơn cho khách hàng khi bạn hoàn thành tỷ lệ phần trăm cụ thể của dự án. Bạn thiết lập các danh mục dự án sau cho công việc để có thể sử dụng chúng trong quy trình thanh toán:

- Tư vấn
- Thiết kế
- Cài đặt

Bạn cũng thiết lập các quy tắc thanh toán tự động tính toán số tiền trên hóa đơn cho tỷ lệ phần trăm công việc dự án đã hoàn thành trong từng hạng mục.

Người quản lý ngân sách tạo ngân sách cho các hạng mục dự án. Khối lượng công việc đã hoàn thành tự động được tính theo tỷ lệ phần trăm của công việc thực tế so với số tiền được lập ngân sách.

## <a name="prerequisites"></a>Điều kiện tiên quyết

Trước khi tạo một dự án sử dụng quy tắc thanh toán, bạn phải thiết lập chuỗi số cho quy tắc thanh toán và nhật ký phí được sử dụng để đăng các hóa đơn tiến độ.

1. Đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Tham số quản lý dự án và kế toán**.
2. Trên trang **Tham số quản lý dự án và kế toán**, trên tab **Số chuỗi**, hãy thiết lập chuỗi số mà bạn muốn sử dụng khi tạo quy tắc thanh toán.
3. Đi đến **Quản lý dự án và kế toán** \> **Nhật ký** \> **Phí**.
4. Trên trang **Nhật ký phí**, chọn **Mới** và nhập tên nhật ký.

## <a name="create-a-contract-for-progress-billings"></a>Tạo hợp đồng để lập hóa đơn tiến độ

Sử dụng quy trình này để tạo hợp đồng dự án cho một dự án theo giá cố định. Bạn tạo hóa đơn dự án khi công việc được hoàn thành trên dự án đạt tỷ lệ phần trăm được chỉ định.

1. Đi đến **Quản lý dự án và kế toán** \> **Dự án** \> **Hợp đồng dự án**.
2. Trên trang **Hợp đồng dự án**, chọn **Mới**.
3. Trong hộp thoại **Hợp đồng dự án mới**, hãy cài đặt các trường sau:

    - **Tên**
    - **Loại ràng buộc**
    - **Nguồn tiền**
    - **Đơn vị tiền tệ bán hàng** – Theo mặc định, đơn vị tiền tệ này được sử dụng cho các hóa đơn của khách hàng có liên quan đến hợp đồng dự án. Tuy nhiên, bạn có thể thay đổi đơn vị tiền tệ bán hàng trên hóa đơn của một khách hàng cụ thể.

4. Chọn **OK**. Thông tin được sao chép vào tiêu đề của trang **Hợp đồng dự án**.
5. Trên trang **Hợp đồng dự án**, điền vào phần còn lại của thông tin cần thiết cho dự án.

## <a name="create-a-project-for-progress-billings"></a>Tạo dự án để lập hóa đơn tiến độ

Làm theo các bước sau để tạo một dự án và bất kỳ dự án con nào được liên kết với hợp đồng dự án.

1. Chuyển đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả dự án**.
2. Trên trang **Tất cả dự án**, chọn **Mới**.
3. Trong hộp thoại **Dự án mới**, trong trường **Loại dự án**, chọn **Thời gian và vật tư**.
4. Chọn nhóm dự án. Nhóm dự án xác định thông tin đăng cho các dự án được chỉ định cho nhóm.
5. Chọn **Tạo dự án**.
6. Sau khi dự án được tạo, hãy đặt giai đoạn dự án thành **Đang diễn ra**.

## <a name="create-a-budget-for-a-project"></a>Tạo ngân sách cho một dự án

Danh mục ngân sách được sử dụng để tự động tính toán số tiền trên hóa đơn cho tỷ lệ phần trăm công việc đã hoàn thành cho từng hạng mục. Thực hiện theo các bước sau để tạo danh mục ngân sách cho chi phí ước tính.

1. Chuyển đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả dự án**.
2. Trên trang **Tất cả dự án**, chọn và mở dự án mà bạn muốn.
3. Trên trang **Dự án**, trên ngăn Hành động, trên tab **Kế hoạch**, trong nhóm **Ngân sách**, chọn **Ngân sách dự án**.
4. Trên trang **Ngân sách dự án**, nhập chi phí ước tính cho từng hạng mục trong dự án.

## <a name="create-billing-rules-for-progress-billings"></a>Tạo quy tắc thanh toán cho các hóa đơn tiến độ

1. Đi đến **Quản lý dự án và kế toán** \> **Dự án** \> **Hợp đồng dự án**.
2. Trên trang **Hợp đồng dự án**, hãy chọn và mở hợp đồng dự án.
3. Trên trang hợp đồng dự án, trên FastTab **Quy tắc thanh toán**, chọn **Thêm**.
4. Trên trang **Quy tắc thanh toán**, trong trường **Loại mô tả**, chọn **Tiến độ**.
5. Trên FastTab **Chi tiết mô tả quy tắc thanh toán**, trong trường **Giá trị hợp đồng**, hãy nhập tổng giá trị của hợp đồng.
6. Trong trường **Danh mục**, chọn danh mục để đăng giao dịch phí.
7. Trong trường **Dự án**, hãy chọn dự án sử dụng quy tắc thanh toán này.
8. Tùy chọn: Chỉ định quy tắc thanh toán cho các dự án bổ sung. Trên FastTab **Dự án**, trong phần **Dự án có sẵn**, chọn một dự án, sau đó chọn nút mũi tên phải để thêm dự án vào phần **Dự án đã chọn**.
9. Tùy chọn: Tính số tiền phần trăm mà khách hàng giữ lại từ các khoản thanh toán trên hóa đơn. Trên FastTab **Điều khoản lưu giữ thanh toán**, chọn nguồn tiền, sau đó, trong trường **Tỷ lệ phần trăm lưu giữ**, nhập tỷ lệ phần trăm lưu giữ.
10. Lặp lại các bước này để tạo các quy tắc thanh toán bổ sung cho hợp đồng dự án.


[!INCLUDE[footer-include](../includes/footer-banner.md)]