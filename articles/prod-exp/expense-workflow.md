---
title: Quy trình làm việc quản lý chi phí
description: Chủ đề này giải thích cách thức bạn có thể sử dụng hệ thống quy trình làm việc trong Microsoft Dynamics 365 Finance để thiết lập quy trình đánh giá báo cáo chi phí trong phần Quản lý chi phí.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005232"
---
# <a name="expense-management-workflow"></a>Quy trình làm việc quản lý chi phí

Bạn có thể sử dụng hệ thống quy trình làm việc để thiết lập quy trình đánh giá báo cáo chi phí trong phần Quản lý chi phí. Bạn có thể thiết lập một quy trình làm việc sử dụng các tiêu chí sau để xác định ai phê duyệt báo cáo chi phí:

- Hệ thống phân cấp báo cáo của nhân viên và các giới hạn phê duyệt được xác định trước
- Hệ thống phê duyệt đa cấp hỗ trợ người phê duyệt tạm thời và người phê duyệt cuối cùng
- Các thông số tài chính và trách nhiệm trong dự án
- Phần chỉ định cho người dùng hoặc nhóm người dùng cụ thể

Các mục phê duyệt trong quy trình làm việc có thể được tạo cho báo cáo chi phí, yêu cầu đi lại, tạm ứng tiền mặt và thu hồi thuế giá trị gia tăng (VAT).

**Ví dụ:**

Quy trình sau đây là một ví dụ về quy trình làm việc quản lý chi phí cho một báo cáo chi phí.

1. Một nhân viên tạo và lưu báo cáo chi phí.
2. Nhân viên gửi báo cáo chi phí để phê duyệt. Người phê duyệt được xác định dựa trên các quy tắc đã xác định trong quá trình thiết lập quy trình làm việc.
3. Người phê duyệt nhận được thông báo rằng có một báo cáo chi phí đã sẵn sàng để phê duyệt. Người phê duyệt đánh giá báo cáo chi phí và xác minh rằng các điều kiện sau được đáp ứng:

    - Các chi phí không vi phạm bất kỳ chính sách chi phí nào. Nếu có một khoản chi phí vi phạm chính sách, thì người phê duyệt xác minh rằng trong báo cáo chi phí có chi tiết biện minh kinh doanh hợp lệ.
    - Biên lai điện tử được đính kèm với báo cáo chi phí.

4. Người phê duyệt tiến hành phê duyệt báo cáo chi phí.
5. Báo cáo chi phí được giao cho người điều phối Khoản phải trả để đăng.
6. Một trong các bước sau xảy ra, tùy thuộc vào việc chức năng đăng tự động có được đặt cấu hình hay không:

    - Nếu chức năng đăng tự động được đặt cấu hình, thì báo cáo chi phí sẽ được xử lý để thanh toán và trạng thái của báo cáo chi phí được cập nhật.
    - Nếu chức năng đăng tự động không được đặt cấu hình, thì điều phối viên Khoản phải trả xác minh rằng tất cả các biên lai gốc đã được gửi và các biên lai đó phù hợp với chi phí trên báo cáo chi phí. Tất cả các mã số thuế được nhập trên báo cáo chi phí cũng phải được xác nhận là chính xác.

Sau khi các yêu cầu này được xác minh, báo cáo chi phí sẽ được đăng.

Sau khi báo cáo chi phí được đăng, việc thanh toán được chấp thuận đối với báo cáo chi phí và nhân viên được hoàn trả.


[!INCLUDE[footer-include](../includes/footer-banner.md)]