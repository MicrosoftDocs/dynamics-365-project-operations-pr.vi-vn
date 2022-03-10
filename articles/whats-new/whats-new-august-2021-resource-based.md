---
title: Tính năng mới kể từ tháng 8 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 8 năm 2021 của Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501397"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 8 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

*Áp dụng cho: Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho*

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

   - Project Operations trong môi trường Microsoft Dataverse phiên bản 4.13.0.152.
   - Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.20.

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- **Bộ phê duyệt**: Các bộ phê duyệt nhóm các yêu cầu phê duyệt thời gian, chi phí hoặc mức sử dụng vật liệu lại với nhau thành các tập hợp con thao tác nhỏ hơn. Việc nhóm này cho phép xử lý các phê duyệt theo yêu cầu cụ thể của dự án, đồng thời cho phép thử lại và sắp xếp theo trình tự. Việc nhóm các yêu cầu giúp cải thiện độ tin cậy và khả năng truy xuất nguồn gốc của việc xử lý phê duyệt đối với khối lượng phê duyệt lớn. Để biết thêm thông tin, hãy xem phần [Bộ phê duyệt](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này.

Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản đang hoạt động của bản đồ trên trang **Ghi kép** trong cột **Phiên bản**. Kích hoạt phiên bản mới của bản đồ bằng cách chọn **Các phiên bản bản đồ bảng**, chọn phiên bản mới nhất, sau đó lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) trong hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 2295625 | Tên cột mốc phải được sao chép từ lịch hóa đơn sang chi tiết dòng hóa đơn. |
| Định giá và thanh toán | 2316323 | Không thể chỉnh sửa chiết khấu trên hóa đơn chiếu lệ trong Project Operations cho các tình huống dựa trên nguồn lực. |
|   Quản lý cơ hội | 2338619 | Chỉ được gọi các quy tắc kinh doanh **Cơ hội** và **Báo giá** trên các trang. |
| Quản lý nguồn lực | 2316523 | Việc sử dụng **Gửi yêu cầu** từ một yêu cầu nguồn lực có một vai trò được đính kèm sẽ không hiển thị lỗi. |
| Quản lý nguồn lực | 2326885 | Việc tạo yêu cầu nguồn lực thông qua một dự án sẽ không hiển thị lỗi. |
| Thời gian và chi phí | 2335584 | Dòng tác vụ không dùng nữa trong mục nhập thời gian. |
| Thời gian và chi phí | 2336884 | Nút nhập thời gian **Sao chép tuần** phải hoạt động không chỉ cho người dùng hiện tại. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Đi lại và chi phí | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Số tiền giao dịch thuế bán hàng và giao dịch nhà cung cấp không chính xác được đăng khi một khoản chi phí được tạo ra từ giao dịch thẻ tín dụng. |
| Đi lại và chi phí | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Quyết toán sai là các dòng được tạo khi tạo nhật ký thanh toán. |
| Đi lại và chi phí | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Số tiền giao dịch thuế bán hàng không chính xác được đăng khi một khoản chi phí được tạo ra từ giao dịch thẻ tín dụng. |
| Đi lại và chi phí | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Việc xóa dòng chi phí có thể mất nhiều thời gian. |
| Kế toán dự án | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Hệ thống không hỗ trợ thiết lập trình tự số liên tục khi bạn đăng ước tính sau khi áp dụng KB 4619395. |
| Kế toán dự án | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Việc đăng hóa đơn của nhà cung cấp có thể không thành công với thông báo lỗi "Các giao dịch trên chứng từ không cân bằng tính đến ngày 17/5/2021. (đơn vị tiền tệ kế toán: 0,00 - đơn vị tiền tệ báo cáo: 0,01) " |
