---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 32, V3
description: Bài viết này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5124137c24da9b579ee1365524d66d9135b2d420
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912910"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Bài viết này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 32. Phiên bản này có số bản dựng là V3.10.53.108 và được phát hành rộng rãi thông qua bản tự cập nhật vào tháng 6 năm 2021.

## <a name="update-release-32"></a>Phát hành bản cập nhật 32

### <a name="bug-fixes"></a>Sửa lỗi

#### <a name="general"></a>Chung

- Khi hoạt động nâng cấp lớn không thành công, thì bạn chỉ nên chặn các điểm vào ứng dụng chính để bảo đảm rằng các thực thể được chia sẻ vẫn có thể truy nhập được.

#### <a name="time-and-expense"></a>Thời gian và Chi phí

Các vấn đề sau đã được khắc phục:

- **TimeEntriesImportFromResourceAssignment** không duy trì thời gian bắt đầu và kết thúc của lát đường bao chỉ định nguồn lực.
- Khi bạn chọn **Mục nhập mở** trên lưới **Mục nhập thời gian**, bạn có thể không chọn được các biểu mẫu khác.
- Trong khi bạn nhập các mục chỉ định vào mục nhập thời gian, truy vấn mã máy khách có thể tạo ra một URL dài khiến truy vấn không thành công.
- Trong lưới **Mục nhập thời gian**, sau khi một giá trị bị xóa khỏi một ô, tiêu điểm sẽ không còn ở lưới nữa.
- Nút **Từ chối** bị loại bỏ khỏi dạng xem **Xử lý phê duyệt** đối với các mục phê duyệt hiện đại.
- Tính ổn định và hiệu suất của chức năng phê duyệt hàng loạt mục nhập thời gian chịu sự ảnh hưởng của các điểm bế tắc và tình trạng không xử lý được thích hợp các mục tùy chỉnh liên quan đến thực thể **Mục nhập thời gian**.

#### <a name="project-planning"></a>Lập kế hoạch dự án

- Một ngoại lệ tham chiếu null sẽ được tạo ra khi bạn cập nhật một dự án có giá trị null ở trường **Đơn vị hợp đồng**.
- Chức năng **Làm mới số liệu tổng của dự án** tính toán sai chi phí còn lại và doanh thu còn lại trên một dự án.
- Các phép tính định giá thừa gây ảnh hưởng tới hiệu suất có liên quan đến các phần cập nhật đối với đường bao chỉ định nguồn lực.

#### <a name="resource-management"></a>Quản lý nguồn lực

Sự cố sau đây đã được khắc phục:

- Khi năng lực theo lịch của một nguồn lực có thể đặt trước lớn hơn 1, Project Service Automation nhận biết không chính xác giá trị năng lực này là 0 (không). Do đó, xuất hiện một vòng lặp vô hạn ở dạng xem lịch trình.

#### <a name="sales"></a>Bán hàng

Các vấn đề sau đã được khắc phục:

- Khi một dòng nhật ký kế toán được tạo có loại giao dịch là tùy chỉnh, ngoại lệ tham chiếu null sau đây sẽ xuất hiện: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Các vai trò và danh mục bị vô hiệu hóa trước khi một báo giá được sao chép sẽ không được thêm vào các vai trò và danh mục có thể tính phí của báo giá mới được sao chép.
- Ngày lập chứng từ và ngày kế toán không được căn chỉnh với ngày bắt đầu có trên chi tiết dòng hóa đơn được tạo trực tiếp trên hóa đơn nháp.
- Các ngoại lệ tham chiếu null sẽ được tạo trong các tình huống có liên quan đến việc vô hiệu hóa các vai trò và danh mục trước khi một báo giá được sao chép.
- Hành động **Cập nhật giá** trên trang **Dự án** không cập nhật các giá trị ước tính chi phí và ước tính vật liệu.
