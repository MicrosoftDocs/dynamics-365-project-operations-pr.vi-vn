---
title: Thiết lập tỷ lệ giữ chân nhà cung cấp
description: Chủ đề này giải thích cách thiết lập tỷ lệ giữ chân nhà cung cấp.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594642"
---
# <a name="set-up-vendor-retention"></a>Thiết lập tỷ lệ giữ chân nhà cung cấp

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này cung cấp thông tin về cách thiết lập tỷ lệ giữ chân nhà cung cấp.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Thiết lập tài khoản giữ chân nhà cung cấp trong Sổ cái chung

1. Trong Dynamics 365 Finance, chuyển đến **Sổ cái chung** > **Thiết lập vào sổ cái** > **Tài khoản cho các giao dịch tự động**.
2. Thêm một mô tả mới.
3. Trong trường **Loại vào sổ cái**, chọn **Giữ chân nhà cung cấp**.
4. Chọn tài khoản chính để vào sổ cái tỷ lệ giữ chân nhà cung cấp.

## <a name="create-vendor-retention-terms"></a>Tạo điều khoản giữ chân nhà cung cấp

Sử dụng trang **Điều khoản giữ chân nhà cung cấp** để thiết lập và duy trì các điều khoản giữ chân cho các khoản thanh toán của nhà cung cấp. Nhập phần trăm khoản thanh toán của nhà cung cấp để giữ lại và phần trăm số tiền đã giữ lại trước đó để giải ngân. Số tiền sẽ tự động được giữ lại trên hóa đơn của nhà cung cấp cho đến khi hợp đồng đạt đến trạng thái hoàn thành được chỉ định. Sau khi các điều khoản giữ lại được thiết lập cho một nhà cung cấp, bạn có thể áp dụng chúng cho bất kỳ dự án nào mà nhà cung cấp đó hoạt động.

1. Trong phần Tài chính, hãy chuyển đến **Quản lý dự án và kế toán** > **Cài đặt** > **Giữ chân** > **Điều khoản giữ lại khoản thanh toán của nhà cung cấp**.
2. Chọn **Mới** để thêm điều khoản lưu giữ mới. Giá trị trong trường **ID quy tắc** cho điều khoản mới được nhập tự động. 
3. Trong trường **Mô tả**, hãy nhập tên mô tả cho điều khoản mới.
4. Trên tab **Điều khoản**, chọn **Thêm mô tả** để nhập điều khoản giữ chân nhà cung cấp.
5. Trong trường **Phần trăm đơn vị được giao**, hãy nhập phần trăm hoàn thành cho quy tắc. Số tiền tự động được giữ lại trên hóa đơn của nhà cung cấp cho đến khi giai đoạn hoàn thành của dự án bằng với tỷ lệ phần trăm mà bạn nhập. Chẳng hạn, nếu bạn nhập 50, thì số tiền sẽ được giữ lại cho đến khi dự án hoàn thành 50 phần trăm.
6. Trong trường **Phần trăm giữ lại**, hãy nhập phần trăm số tiền trên hóa đơn của nhà cung cấp cần giữ lại. Ví dụ: nếu bạn nhập 10,00 vào trường này, thì 10% số tiền trên hóa đơn của nhà cung cấp sẽ được giữ lại cho đến khi dự án đạt đến phần trăm hoàn thành mà bạn chọn trong trường **Phần trăm đơn vị được giao**.
7. Trong trường **Phần trăm giải ngân**, hãy nhập tỷ lệ phần trăm của bất kỳ số tiền đã giữ lại nào trước đó để giải ngân ở mức độ hoàn thành dự án đã chọn.

> [!NOTE]
> Nếu bạn có nhiều mốc cho các mức độ hoàn thành dự án khác nhau, hãy nhập mô tả điều khoản giữ chân nhà cung cấp riêng cho mọi quy tắc giữ chân. Mỗi mô tả có thể chỉ định một tỷ lệ phần trăm khác nhau để giữ lại và một tỷ lệ phần trăm khác nhau để giải ngân cho mỗi mức độ hoàn thành dự án được chỉ định.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Thiết lập thỏa thuận nhà cung cấp cho dự án

Thiết lập các điều khoản giữ chân nhà cung cấp áp dụng cho dự án. Các điều khoản lưu giữ cho nhà cung cấp cũng được hiển thị trên các đơn đặt hàng mà bạn tạo cho nhà cung cấp.

1. Trong phần Tài chính, hãy chuyển đến **Quản lý dự án và kế toán** > **Dự án** > **Tất cả các dự án**. 
2. Chọn một dự án và trên Ngăn nhiệm vụ, hãy chọn **Nhóm dự án** > **Thỏa thuận nhà cung cấp**.
3. Trên trang **Thỏa thuận nhà cung cấp**, thêm một mô tả mới.
4. Trong trường **Mã tài khoản**, hãy chọn một trong các tùy chọn sau:
   - **Bảng**: Các điều khoản lưu giữ được áp dụng cho một nhà cung cấp.
   - **Nhóm**: Các điều khoản lưu giữ được áp dụng cho tất cả các nhà cung cấp trong một nhóm nhà cung cấp.
   - **Tất cả**: Các điều khoản lưu giữ được áp dụng cho tất cả các nhà cung cấp.
5. Ở trường **Nhà cung cấp/nhóm nhà cung cấp**, hãy chọn nhà cung cấp hoặc nhóm nhà cung cấp sẽ được áp dụng các điều khoản giữ lại. Nếu bạn đã chọn **Tất cả** ở bước trước, thì trường này sẽ không khả dụng.
6. Trong trường **Điều khoản giữ chân nhà cung cấp**, hãy chọn ID quy tắc cho các điều khoản giữ chân để áp dụng cho nhà cung cấp này.

