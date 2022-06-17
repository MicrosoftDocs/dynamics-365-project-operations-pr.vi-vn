---
title: Tính năng mới kể từ tháng 9 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 9 năm 2021 của Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có sẵn.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923398"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 9 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

*Áp dụng cho: Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho*

Bài viết này áp dụng cho những điều sau Dynamics 365 Project Operations các thành phần và phiên bản:

   - Project Operations trong môi trường Microsoft Dataverse phiên bản 4.14.0.99.
   - Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản đang hoạt động của bản đồ trên trang **Ghi kép** trong cột **Phiên bản**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Sự cố thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Thời gian và chi phí | 1811407 | Đã điều chỉnh Người phê duyệt dự án vai trò bảo mật để phê duyệt mục nhập chi phí. |
| Thời gian và chi phí | 1811438 | Đã điều chỉnh vai trò bảo mật của Người phê duyệt dự án để hủy bỏ phê duyệt mục nhập thời gian. |
| Thời gian và chi phí | 2370126 | Đã cập nhật biểu tượng **Nhiệm vụ dự án** và **Vai trò** trong thực thể **Mục nhập thời gian**. |
| Thời gian và chi phí | 2379879 | Đã sửa lỗi chức năng **Sao chép tuần** trogn mục nhập thời gian khi sử dụng Dynamics 365 dành cho điện thoại. |
| Định giá và thanh toán | 2371906 | Tổng số tiền trên hóa đơn ước giá không được điều chỉnh trong Project Operations để triển khai dựa trên nguồn lực. |
| Định giá và thanh toán | 2385802 | Đã sửa lỗi xảy ra với số giờ thực tế âm khi tổng số dự án được làm mới. |
| Định giá và thanh toán | 2389675 | Cải thiện hành vi xác nhận hóa đơn ước giá. Thực thể công việc đang hoạt động lâu dài phải tính đến hoạt động cần thiết để ghi kết quả xác nhận cho kế toán. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Đi lại và chi phí | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Số tiền trên các giao dịch thuế bán hàng và nhà cung cấp được tính từ một khoản chi phí được tạo ra từ giao dịch thẻ tín dụng là không chính xác. |
| Đi lại và chi phí | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Các mô tả quyết toán sai được tạo ra khi tạo nhật ký thanh toán. |
| Đi lại và chi phí | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Số tiền trên các giao dịch thuế bán hàng được tính từ một khoản chi phí được tạo ra từ giao dịch thẻ tín dụng là không chính xác. |
| Đi lại và chi phí | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Việc xóa dòng chi phí có thể mất nhiều thời gian. |
| Kế toán dự án | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sau khi bạn áp dụng KB 4619395, việc thay đổi chuỗi số thành **Tiếp diễn** không được hỗ trợ và khi bạn đăng dự toán, sẽ xảy ra lỗi sau: "Hệ thống không hỗ trợ thiết lập 'liên tục' của dãy số Proj_X." |
| Kế toán dự án | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Việc đăng hóa đơn của nhà cung cấp có thể không thành công với thông báo lỗi sau: "Các giao dịch trên chứng từ không cân đối theo ngày 17/5/2021. (đơn vị tiền tệ kế toán: 0,00 - đơn vị tiền tệ báo cáo: 0,01)." |
