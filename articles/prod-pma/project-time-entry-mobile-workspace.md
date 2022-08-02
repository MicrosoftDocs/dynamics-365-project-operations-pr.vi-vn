---
title: Không gian làm việc di động mục nhập thời gian dự án
description: Bài viết này cung cấp thông tin về không gian làm việc di động mục nhập thời gian Dự án. Không gian làm việc này cho phép người dùng tham gia và tiết kiệm thời gian cho một dự án bằng cách sử dụng thiết bị di động của họ.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 50388bd024fdf2de0d28e49ef07a01b03c6b88f0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029694"
---
# <a name="project-time-entry-mobile-workspace"></a>Không gian làm việc di động mục nhập thời gian dự án

[!include [banner](../includes/banner.md)]

Bài viết này cung cấp thông tin về **Mục nhập thời gian dự án** không gian làm việc di động. Không gian làm việc này cho phép người dùng tham gia và tiết kiệm thời gian cho một dự án bằng cách sử dụng thiết bị di động của họ.

Không gian làm việc di động này được thiết kế để sử dụng với ứng dụng di động Dynamics 365 Unified Ops. 

## <a name="overview"></a>Tổng quan
Là một phần của công việc hàng ngày của họ, các nguồn lực của dự án thường là tại chỗ hoặc đi du lịch. Không gian làm việc di động **Mục nhập thời gian dự án** cho phép người dùng nhập thời gian có thể lập hóa đơn hoặc không lập hóa đơn đối với một dự án trên thiết bị di động mà họ lựa chọn. Do đó, nguồn lực dự án có thể ghi lại các mục thời gian bất cứ lúc nào và bất cứ nơi đâu. Họ cũng có thể xem các mục thời gian đã được ghi lại. 

Cụ thể, trong không gian làm việc di động **Mục nhập thời gian dự án**, người dùng có thể thực hiện các tác vụ sau:

-   Đối với bất kỳ ngày nào đã chọn, nhập số giờ bạn đã dành cho một tác vụ cụ thể.
-   Tìm kiếm theo tên dự án hoặc khách hàng để tìm dự án cần nhập thời gian.
-   Chỉ định thể loại và hoạt động cho thời gian bạn đã bỏ ra.
-   Ghi lại thời gian có thể lập hóa đơn hoặc không lập hóa đơn cho dự án.
-   Nhập nhận xét bên ngoài và nội bộ (không bắt buộc).

## <a name="prerequisites"></a>Điều kiện tiên quyết
Các điều kiện tiên quyết khác nhau, dựa trên phiên bản của Microsoft Dynamics 365 đã được triển khai cho tổ chức của bạn.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Điều kiện tiên quyết nếu bạn sử dụng Dynamics 365 Finance
Nếu Finance đã được triển khai cho tổ chức của bạn, quản trị viên hệ thống phải phát hành không gian làm việc di động **Mục nhập thời gian dự án**. Để được hướng dẫn, hãy xem [Phát hành không gian làm việc di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Điều kiện tiên quyết nếu bạn sử dụng phiên bản 1611 với bản cập nhật Nền tảng từ 3 trở đi
Nếu phiên bản 1611 với bản cập nhật Nền tảng từ 3 trở đi đã được triển khai cho tổ chức của bạn, quản trị viên hệ thống phải hoàn thành các điều kiện tiên quyết sau. 

<table>
<thead>
<tr class="header">
<th>Điều kiện tiên quyết</th>
<th>Vai trò</th>
<th>Mô tả</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Triển khai KB 4018050.</td>
<td>Quản trị viên hệ thống</td>
<td>KB 4018050 là bản cập nhật X++ hoặc bản vá lỗi siêu dữ liệu có chứa không gian làm việc di động <strong>Mục nhập thời gian dự án</strong>. Để triển khai KB 4018050, quản trị viên hệ thống của bạn phải làm theo các bước sau.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Tải xuống bản sửa lỗi siêu dữ liệu từ Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Cài đặt bản sửa lỗi siêu dữ liệu</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Tạo một gói có thể triển khai</a> chứa mô hình <strong>ApplicationSuite</strong> và <strong>ProjectMobile</strong>, sau đó tải gói có thể triển khai lên LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Áp dụng gói có thể triển khai</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Phát hành không gian làm việc <strong>Mục nhập thời gian dự án</strong>.</td>
<td>Quản trị viên hệ thống</td>
<td>Xem <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Phát hành không gian làm việc di động</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Tải xuống và cài đặt ứng dụng dành cho thiết bị di động

Tải xuống và cài đặt ứng dụng di động tài chính và hoạt động:

-   [Đối với điện thoại Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Đối với iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Đăng nhập vào ứng dụng dành cho thiết bị di động
1.  Khởi động ứng dụng trên thiết bị di động của bạn.
2.  Nhập URL Dynamics 365.
3.  Lần đầu tiên đăng nhập, bạn sẽ được nhắc nhập tên người dùng và mật khẩu của mình. Nhập thông tin xác thực của bạn.
4.  Sau khi bạn đăng nhập, không gian làm việc có sẵn cho công ty của bạn sẽ được hiển thị. Lưu ý rằng nếu quản trị viên hệ thống của bạn phát hành không gian làm việc mới sau đó, bạn sẽ phải làm mới danh sách không gian làm việc di động.

[![Kéo để làm mới.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Nhập thời gian bằng cách sử dụng không gian làm việc di động Mục nhập thời gian dự án
1.  Trên thiết bị di động của bạn, hãy chọn không gian làm việc **Mục nhập thời gian dự án**.
2.  Chọn **Mục nhập thời gian**. Các ngày trong lịch cho tuần hiện tại được hiển thị.
3.  Đối với một ngày đã chọn, hãy chọn **Hành động** &gt; **Mục nhập mới**.
4.  Nhập số giờ để ghi lại.
5.  Chọn dự án cho mục nhập thời gian. Danh sách hiển thị các dự án được tải vào ứng dụng của bạn để sử dụng ngoại tuyến. Theo mặc định, 50 mục được tải, nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, hãy xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Nếu dự án của bạn không có trong danh sách, hãy chọn **Tìm kiếm**. Tìm kiếm theo tên hoặc chuyển sang tìm kiếm theo tên dự án hoặc khách hàng.
7.  Chọn thể loại. Danh sách hiển thị các thể loại được tải vào ứng dụng của bạn để sử dụng ngoại tuyến. Theo mặc định, 50 mục được tải, nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, hãy xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Nếu thể loại của bạn không có trong danh sách, hãy chọn **Tìm kiếm**. Tìm kiếm theo thể loại hoặc chuyển sang tìm kiếm theo tên thể loại.
9.  Chọn hoạt động. Danh sách hiển thị các hoạt động được tải vào ứng dụng của bạn để sử dụng ngoại tuyến. Theo mặc định, 50 mục được tải, nhưng nhà phát triển có thể thay đổi con số này. Để biết thêm thông tin, hãy xem [Nền tảng di động](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Nếu hoạt động của bạn không có trong danh sách, hãy chọn **Tìm kiếm**. Tìm kiếm theo số hoạt động hoặc chuyển sang tìm kiếm theo mục đích.

11. Chọn thuộc tính dòng.
12. Tùy chọn: Nhập nhận xét bên ngoài và nội bộ.
13. Chọn **Xong**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]