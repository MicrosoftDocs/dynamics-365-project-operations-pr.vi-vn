---
title: Thiết lập nguồn lực dự án
description: Bài viết này cung cấp thông tin về việc thiết lập hoặc yêu cầu tài nguyên dự án.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a4e6fe829d6b39aed9eb6aaea42f245fc997593
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933794"
---
# <a name="set-up-project-resources"></a>Thiết lập nguồn lực dự án

[!include [banner](../includes/banner.md)]

Bạn phải thiết lập lịch và liên kết nó với nhân viên. Lịch được sử dụng để lập lịch trình cho dự án và thời gian làm việc của các nguồn lực được dành cho dự án. Trong quá trình thiết lập lịch, người quản lý dự án có thể cân bằng tài nguyên trong quá trình tối ưu hóa nguồn lực. Dựa trên lịch trình theo lịch, có thể đưa ra các hạn chế đối với nguồn lực. Bạn có thể thiết lập lịch trên trang **Lịch**.

Khi bạn thiết lập nhân viên làm nguồn lực dự án, bạn có thể chọn từ nhân viên làm việc trong công ty mà bạn đang thiết lập nguồn lực. Ngoài ra, bạn có thể chọn nhân viên từ các công ty khác trong tổ chức của mình. Những nhân viên này được gọi là nguồn lực liên công ty.

Các quy trình sau đây giải thích cách thiết lập một nhân viên làm nguồn lực dự án trong công ty của bạn và cách thiết lập nguồn lực dự án liên công ty.

## <a name="set-up-a-worker-as-a-project-resource"></a>Thiết lập nhân viên làm nguồn lực dự án

1. Trên trang **Nhân viên** trong danh sách **Nhân viên**, chọn nhân viên mà bạn đang thêm làm nguồn lực dự án và mở hồ sơ nhân viên.
2. Trên Ngăn hành động, chọn **Dự án** &gt; **Thiết lập** &gt; **Thiết lập dự án**.
3. Chọn lịch rồi đóng trang.

Bạn cũng có thể chỉ định các dự án mặc định cho một nguồn lực như một loại phân công trước. Phân công trước có thể được sử dụng khi người quản lý tài nguyên hoặc người quản lý dự án biết trước dự án mà nguồn lực sẽ thực hiện. Phân công trước cũng có thể dựa trên yêu cầu về người tài trợ dự án hoặc khách hàng. Để phân công trước dự án, trên trang **Chỉ định dự án**, trên tab **Dự án**, trong danh sách **Dự án còn lại**, chọn dự án thích hợp.

## <a name="set-up-an-intercompany-resource"></a>Thiết lập nguồn lực liên công ty

Khi bạn thiết lập một nhân viên làm nguồn lực liên công ty, bạn phải hoàn thành việc thiết lập ở cả công ty cho mượn và công ty mượn.

### <a name="in-the-lending-company"></a>Ở công ty cho mượn

1. Trong Finance, hãy xác minh rằng công ty cho mượn đã được chọn, rồi hoàn thành quy trình trong phần trước đó: "Thiết lập nhân viên làm nguồn lực dự án".
2. Trên trang **Kế toán liên công ty**, chọn **Mới**.
3. Trong trường **ID pháp nhân**, chọn công ty cho mượn. Điền vào các trường còn lại là thích hợp, sau đó chọn **Lưu**.
4. Trên trang **Giá chuyển nhượng**, chọn **Mới**.
5. Trong trường **Pháp nhân mượn**, chọn công ty thích hợp.
6. Để chỉ cho mượn nguồn lực mà bạn tạo ở đầu phần này, trong trường **Nguồn lực**, chọn tên của nguồn lực mà bạn đã tạo. Để hiển thị toàn bộ nguồn lực của công ty cho mượn cho công ty mượn, hãy để trống trường **Nguồn lực**.
7. Trên trang **Tham số quản lý dự án và kế toán**, trên tab **Liên công ty**, đặt tùy chọn **Bật lập lịch và bảng chấm công nguồn lực** thành **Có**.

### <a name="in-the-borrowing-company"></a>Ở công ty mượn

- Trên trang **Danh sách nguồn lực**, trong bộ lọc tìm kiếm, hãy nhập tên nguồn lực mà bạn đã tạo cho công ty cho mượn, để xác minh rằng tên đó có trong danh sách nguồn lực dành cho công ty mượn hay không.

## <a name="request-project-resources"></a>Yêu cầu nguồn lực dự án
Chức năng lập lịch trình nguồn lực dự án chỉ cho phép người quản lý nguồn lực phân phối nguồn lực biên chế trong hoạt động thuê hoặc dự án. Để bật chức năng này, hãy hoàn thành các nhiệm vụ sau hoặc xác minh rằng chúng đã được hoàn thành:

- Thiết lập chuỗi số.
- Thiết lập quy trình công việc kế toán và quản lý dự án.
- Bật quy trình công việc yêu cầu nguồn lực.

Sau khi hoàn thành các nhiệm vụ liên trước, bạn có thể hoàn thành các nhiệm vụ sau theo yêu cầu:

- Tạo một yêu cầu nguồn lực từ nguồn lực biên chế đã đặt trước dự kiến.
- Giám sát yêu cầu nguồn lực.
- Thực hiện các đề nghị nguồn lực.
- Yêu cầu nguồn lực biên chế từ WBS.
- Đặt trước nguồn lực cho dự án mà không có yêu cầu về nguồn lực biên chế.


[!INCLUDE[footer-include](../includes/footer-banner.md)]