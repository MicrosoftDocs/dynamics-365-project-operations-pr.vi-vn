---
title: Trợ cấp cho dự án
description: Bài viết này giải thích cách tạo hoặc sửa đổi một khoản trợ cấp.
author: RadhikaRS
ms.date: 04/22/2020
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
ms.openlocfilehash: 40357bdfb74b6afdb26663e6439f90e762b79029
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913646"
---
# <a name="project-grants"></a>Trợ cấp cho dự án

[!include [banner](../includes/banner.md)]

Trợ cấp là một món quà bằng tiền cho một mục đích hoặc dự án cụ thể. Thông thường, có hạn chế về cách chi tiêu một khoản trợ cấp. Trong Quản lý dự án và kế toán, bạn có thể nhập và theo dõi các khoản trợ cấp, đồng thời xác định mối quan hệ của chúng với các dự án và hợp đồng dự án. Ví dụ: bạn có thể thực hiện các tác vụ sau:

- Liên kết các khoản trợ cấp với các dự án và các nguồn tài trợ thông qua các liên kết đến trang **Dự án** và **Chi tiết hợp đồng dự án**.
- Nhập và theo dõi các thay đổi đối với khoản trợ cấp khi khoản trợ cấp chuyển từ trạng thái này sang trạng thái khác.
- Nhập và theo dõi chi phí, số tiền được yêu cầu và số tiền được thưởng.
- Tạo các khoản trợ cấp chính và liên kết các khoản trợ cấp phụ với chúng.

Bạn có thể tạo một khoản trợ cấp bằng cách nhập tất cả các chi tiết vào một bản ghi mới hoặc bạn có thể sao chép các chi tiết từ một khoản trợ cấp hiện có và sau đó cập nhật chúng.

## <a name="create-a-new-grant"></a>Tạo một khoản trợ cấp mới

1. Đi đến **Quản lý dự án và kế toán** \> **Khoản trợ cấp** \> **Khoản trợ cấp**.
2. Chọn **Mới** \> **Trợ cấp**.
3. Trên trang chi tiết khoản trợ cấp, trên FastTab **Tổng quát**, trong trường **ID khoản trợ cấp**, hãy nhập mã nhận dạng chữ và số cho khoản trợ cấp.
4. Trong trường **Tên khoản trợ cấp**, hãy nhập tên cho khoản trợ cấp.
5. Trong trường **Mô tả**, hãy thêm thông tin chi tiết về khoản trợ cấp mới.

    Hầu hết các trường khác trên trang là tùy chọn và bạn có thể nhập bao nhiêu thông tin tùy ý.

    Danh sách sau đây mô tả thông tin được chỉ định trên mỗi FastTab của trang chi tiết khoản trợ cấp:

    - **Tổng quát** – Nhập tên khoản trợ cấp, trạng thái, mô tả, mục đích và số tiền.
    - **Thông tin liên lạc** – Nhập thông tin chi tiết về các nhân viên, bộ phận quản lý khoản trợ cấp và khách hàng trợ cấp hoặc nguồn tổ chức trợ cấp. Bạn cũng có thể cho biết liệu tổ chức của bạn có phải là một tổ chức chuyển tiếp nhận trợ cấp, sau đó chuyển cho người nhận khác hay không. Chọn **Thêm** để thêm thông tin liên lạc chẳng hạn như số điện thoại và địa chỉ email cho tổ chức cung cấp khoản trợ cấp.
    - **Ngày và thời hạn** – Nhập ngày tháng liên quan đến khoản trợ cấp và đơn xin trợ cấp. Ví dụ bao gồm ngày đến hạn nộp đơn, ngày nộp đơn và ngày khoản trợ cấp được chấp thuận hoặc bị từ chối.
    - **Dự án liên kết và hợp đồng dự án** – Bạn chỉ có thể nhập thông tin trên FastTab này nếu trường **Trạng thái trợ cấp** trên FastTab **Tổng quát** được đặt thành **Hiện hoạt** hoặc **Đã trao thưởng**. Chọn trong số các tùy chọn sau để hoàn thành tác vụ liên quan:

        - **Thêm nguồn tiền** – Thêm một nguồn tiền mới cho khoản trợ cấp. Bạn có thể nhập tất cả các chi tiết ngay bây giờ hoặc bạn có thể sử dụng thông tin mặc định và cập nhật vào lúc khác.
        - **Thêm hợp đồng dự án** – Thêm hoặc cập nhật thông tin hợp đồng dự án.
        - **Thêm dự án** – Thêm hoặc cập nhật chi tiết dự án.

    - **Thiết lập** – Nhập thông tin chi tiết về các nguồn tiền phù hợp, nếu thông tin này là bắt buộc. Nhiều tổ chức trợ cấp yêu cầu người nhận phải chi một số tiền hoặc nguồn lực cụ thể của riêng họ để phù hợp với số tiền được trao trong khoản trợ cấp. Trong trường **Dự án địa phương hoặc ID theo dõi**, bạn có thể nhập số nhận dạng khác với số nhận dạng của dự án.

        > [!NOTE]
        > Nếu một phần của khoản trợ cấp sẽ được trao cho một tổ chức khác, hãy đặt tùy chọn **Người trợ cấp phụ** thành **Có**. Đối với các khoản trợ cấp được trao ở Hoa Kỳ, bạn có thể chỉ định xem khoản trợ cấp sẽ được trao theo ủy quyền của tiểu bang hay liên bang.

    - **Chi tiết giải ngân** – Thêm hoặc cập nhật thông tin về tần suất khoản tiền trợ cấp có thể được giải ngân, lập hóa đơn hoặc chi tiêu.

## <a name="create-a-new-grant-from-a-copy"></a>Tạo một khoản trợ cấp mới từ một bản sao

1. Đi đến **Quản lý dự án và kế toán** \> **Khoản trợ cấp** \> **Khoản trợ cấp**.
2. Chọn **Mới** \> **Sao chép từ khoản trợ cấp**.
3. Nhập số nhận dạng chữ và số và tên cho khoản trợ cấp mới, sau đó chọn **OK**.
4. Trên trang chi tiết khoản trợ cấp, hãy xem lại các chi tiết của khoản trợ cấp đã sao chép và thực hiện bất kỳ thay đổi nào được yêu cầu. Hầu hết các trường trên trang là tùy chọn.

## <a name="view-or-modify-grant-details"></a>Xem hoặc sửa đổi chi tiết khoản trợ cấp

1. Đi đến **Quản lý dự án và kế toán** \> **Khoản trợ cấp** \> **Khoản trợ cấp**.
2. Chọn khoản trợ cấp cần sửa đổi.
3. Trên ngăn Hành động, trên tab **Trợ cấp**, trong nhóm **Duy trì**, hãy chọn **Chỉnh sửa**.
4. Xem lại chi tiết khoản trợ cấp và thực hiện bất kỳ thay đổi nào được yêu cầu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]