---
title: Tạo nhóm dự án
description: Chủ đề này cung cấp thông tin về cách tạo và quản lý nhóm dự án.
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
ms.openlocfilehash: f134d7566954e640eea8ff8af98e184273ad570c
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683058"
---
# <a name="create-a-project-team"></a>Tạo nhóm dự án

[!include [banner](../includes/banner.md)]

Để sử dụng các vai trò đã được thiết lập trước đó trong một dự án, người quản lý dự án phải liên kết các vai trò đó với dự án. Có thể gán nhiều vai trò cho một dự án. Để tránh nhầm lẫn, các vai trò này được tự động gắn nhãn trong quá trình dự trữ. Ví dụ: nếu người quản lý dự án yêu cầu ba kỹ sư phần mềm, thì ba vai trò Kỹ sư phần mềm có nhãn là **kỹ sư phần mềm 1**, **kỹ sư phần mềm 2** và **kỹ sư phần mềm 3** sẽ được tạo tự động. Nếu các đặc điểm của vai trò đã được thiết lập cho vai trò, thì chúng được áp dụng như một bộ lọc trong quá trình tìm kiếm nguồn lực. Các đặc điểm bổ sung có thể được thêm vào theo yêu cầu để tinh chỉnh thêm nội dung tìm kiếm.

Cài đặt dạng xem cũng có thể được tùy chỉnh để mang lại dạng xem tốt hơn về tình trạng rảnh/bận của nguồn lực. Có các tùy chọn để hiển thị tình trạng rảnh/bận theo giờ, ngày, tuần, tháng, quý và năm. Ngoài ra, còn có một tùy chọn để hiển thị năng lực sẵn sàng và còn lại của nguồn lực. Tùy chọn này hữu ích cho việc quản lý thời gian, khi bạn ước tính thời gian sẵn có cho các hoạt động hoặc tình trạng rảnh/bận của nguồn lực.

Người quản lý dự án có thể chọn một vai trò trên trang và sau đó, nếu có sẵn một nguồn lực phù hợp với yêu cầu, hãy chọn dự trữ nguồn lực để thực hiện vai trò đó. Lưu ý rằng không cần dự trữ nguồn lực tại thời điểm này trong giai đoạn lập kế hoạch. Khi tạo một WBS, bạn có thể thay các vai trò bằng nguồn lực có biên chế cho dự án. Nếu vai trò được thay bằng nguồn lực có biên chế trong WBS, thiết lập nguồn lực sẽ tự động cập nhật danh sách và lịch trình của nhóm dự án.

[![Danh sách nhóm dự án bao gồm cả vai trò và nguồn lực thực tế.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Người quản lý dự án có nhiều tùy chọn khác nhau để đặt trước nguồn lực cho một dự án, chẳng hạn như **Năng lực còn lại**, **Năng lực đầy đủ**, **Phần trăm năng lực** và **Chỉ định giờ**. Các tùy chọn đặt trước này có thể bị hủy bỏ bất cứ lúc nào nếu việc phân công nguồn lực thay đổi. Hai loại đặt trước được hỗ trợ:

- **Đặt trước chắc chắn** – Việc dự trữ nguồn lực đã được phê duyệt và xác nhận để tiến hành thuê trong thời gian quy định.
- **Đặt trước dự kiến** – Việc dự trữ nguồn lực được dự kiến thiết lập để tiến hành thuê trong thời gian quy định.

Quy trình sau đây giải thích cách tạo nhóm dự án.

## <a name="create-a-project-team"></a>Tạo nhóm dự án

1. Trên trang danh sách **Tất cả dự án**, chọn dự án rồi chọn **Chỉnh sửa**.
2. Trên tab **Nhóm dự án và lập lịch trình**, trong trường **Lên lịch ngày kết thúc**, nhập ngày bắt đầu lịch trình cộng thêm một tháng. Ví dụ: nếu ngày bắt đầu lịch trình là ngày 24 tháng 6 năm 2017 (24/06/2017), hãy nhập **24/07/2017**.
3. Chọn **Thêm**.
4. Trong ngăn **Thêm vai trò vào dự án**, trong trường **Vai trò**, chọn **Người quản lý dự án cấp cao**.
5. Lựa chọn **Năng lực cần thiết**.
6. Trên trang **Chọn đặc điểm**, các đặc điểm mà bạn đã thiết lập cho vai trò Người quản lý dự án cấp cao được chọn theo mặc định. Chọn **OK**.
7. Trên trang **Thêm vai trò vào dự án**, trong trường **Số lượng tài nguyên**, nhập **1**.
8. Trong trường **Nguồn lực**, phần tra cứu hiển thị tất cả nguồn lực có năng lực cần thiết. Chọn **Daniel Goldschmidt** rồi chọn **Tạo**.
9. Trên trang **Dự án**, chọn **Thêm**.
10. Trong ngăn **Thêm vai trò vào dự án**, trong trường **Vai trò**, chọn **Thành viên nhóm**. Trong trường **Số nguồn lực**, nhập **5**.
11. Chọn **Tạo**.
12. Trên trang **Dự án**, chọn **Đáp ứng nguồn lực**.

## <a name="monitor-project-teams"></a>Giám sát các nhóm dự án
1. Trên trang **Tất cả dự án**, chọn liên kết **ID dự án** cho dự án **Nâng cấp XYZ Giai đoạn 2**.
2. Trên **Nhóm dự án và lập lịch trình** FastTab, xác minh rằng các nguồn lực dự án được liệt kê là chính xác.


[!INCLUDE[footer-include](../includes/footer-banner.md)]