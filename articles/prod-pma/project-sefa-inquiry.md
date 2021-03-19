---
title: Truy vấn về Lịch trình chi tiêu của Giải thưởng Liên bang
description: Chủ đề này cung cấp thông tin về truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288990"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Truy vấn về Lịch trình chi tiêu của Giải thưởng Liên bang

[!include [banner](../includes/banner.md)]

Theo Thông tư A-133 của Văn phòng Quản lý và Ngân sách, các cơ quan nhận quỹ liên bang phải tuân theo các yêu cầu kiểm toán, còn được gọi là kiểm toán đơn lẻ. Quy trình kiểm toán được sử dụng để báo cáo định kỳ các khoản thu và chi của các khoản trợ cấp liên bang. Một phần của báo cáo kiểm toán đơn lẻ bao gồm Lịch trình chi tiêu của Giải thưởng Liên bang (SEFA).

Truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang bao gồm tiêu đề và số hiệu của Sản phẩm hỗ trợ liên bang trong nước (CFDA), số hiệu trợ cấp, năm trợ cấp, tên cơ quan thuộc liên bang cung cấp tiền và tên của thực thể chuyển tiếp. Cuộc điều tra diễn ra trong một khoảng thời gian cụ thể. Thông thường, khoảng thời gian đó giống với kỳ báo cáo tài chính, là năm tài chính.

Truy vấn bao gồm các khoản trợ cấp có ngày dự kiến trong phạm vi ngày đã chọn. Cột **Cơ quan trợ cấp** của truy vấn hiển thị khách hàng trợ cấp hoặc đối với khoản trợ cấp chuyển tiếp, là cơ quan trợ cấp. Đối với khoản trợ cấp chuyển tiếp, cột **Cơ quan chuyển tiếp** hiển thị khách hàng trợ cấp. Nếu khoản trợ cấp không phải là chuyển tiếp, thì cột **Cơ quan chuyển tiếp** sẽ trống.

## <a name="set-up-the-cfda-clusters"></a>Thiết lập cụm CFDA

Bạn phải thiết lập các cụm CFDA có thể được liên kết với các số CFDA trong truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang.

1. Đi đến **Quản lý dự án và kế toán \> Thiết lập \> Khoản trợ cấp \> cụm Sản phẩm hỗ trợ liên bang trong nước**.
2. Chọn **Mới** để tạo cụm CFDA.
3. Nhập tên cụm.
4. Chọn **Lưu** để lưu thay đổi của bạn.

## <a name="set-up-cfda-numbers"></a>Thiết lập cụm CFDA

Bạn phải thiết lập số CFDA có thể được thêm vào khoản trợ cấp và được bao gồm trong truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang.

1. Đi đến **Quản lý dự án và kế toán \> Thiết lập \> Khoản trợ cấp \> số hiệu Sản phẩm hỗ trợ liên bang trong nước**.
2. Chọn **Mới** để tạo số hiệu CFDA.
3. Trong cột **Số hiệu**, hãy nhập số hiệu CFDA.
4. Nhấn phím **Tab**.
5. Trong cột **Mô tả**, hãy nhập tiêu đề CFDA.
6. Nhấn phím **Tab**.
7. Tùy chọn: Trong trường **Cụm chương trình**, thêm cụm CFDA thích hợp.
8. Chọn **Lưu** để lưu thay đổi của bạn.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Thiết lập các khoản trợ cấp để báo cáo cho truy vấn về Lịch trình chi tiêu của Giải thưởng Liên bang

1. Đi đến **Quản lý dự án và kế toán \> Khoản trợ cấp \> Khoản trợ cấp** và chọn một khoản trợ cấp hiện có.
2. Trên FastTab **Thiết lập**, trong trường **Sản phẩm hỗ trợ liên bang trong nước**, hãy gán số hiệu CFDA. Số hiệu CFDA trên khoản trợ cấp xác định cụm CFDA để báo cáo.
3. Trên FastTab **Thông tin liên lạc**, nhập thông tin người tài trợ bằng cách làm theo các bước sau:

    1. Trong trường **Khách hàng trợ cấp**, nhập khách hàng chịu trách nhiệm cho khoản trợ cấp. Đối với một khoản trợ cấp hiện có, thông tin này có thể đã được nhập.
    2. Cho biết khách hàng trợ cấp có phải là nhà tài trợ hay không. Nếu khách hàng trợ cấp là nhà tài trợ, không chọn hộp kiểm **Chuyển tiếp**. Nếu khách hàng khác là nhà tài trợ và khách hàng trợ cấp chịu trách nhiệm chi tiêu và theo dõi số tiền, hãy chọn hộp kiểm **Chuyển tiếp**.

4. Nếu bạn đã chọn hộp kiểm **Chuyển tiếp** trong bước trước đó, trong trường **Cơ quan trợ cấp**, hãy nhập khách hàng đã cung cấp khoản trợ cấp. Cơ quan trợ cấp và khách hàng trợ cấp không được là cùng một khách hàng.

Dưới đây là một ví dụ về khoản trợ cấp chuyển tiếp:

Chính phủ liên bang đã tài trợ một dự án cơ sở hạ tầng cho một tiểu bang. Chính phủ liên bang đã cung cấp tiền để tiểu bang chi tiêu. Trong trường hợp này, chính phủ liên bang là cơ quan trợ cấp và tiểu bang là khách hàng trợ cấp.

> [!NOTE] 
> Khi bạn bật tính năng này lần đầu tiên, số hiệu CFDA ban đầu sẽ được nhập bằng cách sử dụng các số hiệu hiện có trên khoản trợ cấp.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Loại trừ các khoản trợ cấp khỏi báo cáo SEFA dựa trên loại trợ cấp

1. Chuyển đến **Quản lý dự án và kế toán \> Thiết lập \> Khoản trợ cấp \> Các loại trợ cấp**.
2. Trên FastTab **Thông tin mặc định**, chọn hộp kiểm **Loại trừ khỏi Lịch trình chi tiêu của Giải thưởng Liên bang**.
3. Chọn **Lưu** để lưu thay đổi của bạn.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Chạy truy vấn về Lịch trình chi tiêu của Giải thưởng Liên bang

1. Đi đến **Quản lý dự án và kế toán \> Truy vấn và báo cáo \> Truy vấn về khoản trợ cấp \> Lịch trình chi tiêu của Giải thưởng Liên bang**.
2. Trong phần **Tham số**, hãy làm theo các bước sau:

    1. Trong trường **Khoảng ngày**, chọn mã cho khoảng ngày. Hoặc, trong các trường **Từ ngày** và **Đến ngày**, hãy xác định khoảng ngày.
    2. Tùy chọn: Để chỉ bao gồm các giao dịch đã lập hóa đơn dưới dạng doanh thu trong truy vấn, hãy đặt tùy chọn **Chỉ bao gồm doanh thu đã lập hóa đơn** thành **Có**.

## <a name="columns"></a>Cột

Truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang bao gồm các cột sau:

- Tên cụm Sản phẩm hỗ trợ liên bang trong nước
- Cơ quan trợ cấp
- Cơ quan chuyển tiếp
- Tên khoản trợ cấp
- ID khoản trợ cấp
- ID đơn đăng ký trợ cấp
- Sản phẩm hỗ trợ liên bang trong nước
- Biên nhận
- Các khoản chi tiêu


[!INCLUDE[footer-include](../includes/footer-banner.md)]