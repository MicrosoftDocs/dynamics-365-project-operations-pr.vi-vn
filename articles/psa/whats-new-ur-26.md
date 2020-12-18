---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643289"
---
<a name="project-service-automation-update-release-26-v3"></a>Phát hành bản cập nhật Project Service Automation 26, V3
================================================

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation, Bản phát hành cập nhật 26, V3. Phiên bản này có mã số bản dựng là V3.10.44.59 và được phát hành rộng rãi thông qua bản tự cập nhật vào tháng 12 năm 2020.

<a name="update-release-26"></a>Phát hành bản cập nhật 26
-----------------

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

-   Người dùng có thể thay đổi nhiệm vụ trên mục thời gian đã được phê duyệt/gửi.

-   Lỗi "Chưa đặt tham chiếu đối tượng" khi lưu mục thời gian.

-   Mục thời gian nhập từ các lần phân công nguồn lực sẽ tạo ra các mục thời gian có giá trị DateTime không chính xác.

-   Khi cài đặt cả ứng dụng Project Service Automation và Field Service, nút **Mới** hiển thị 2 lần trên thanh lệnh của các mục thời gian trong ứng dụng Field Service.

-   Điểm cập nhật ô **Cho phép đơn vị** và **Nhóm đơn vị** giờ đã có tác dụng trên lưới **Ước tính chi phí**.

-   Biểu mẫu **Chỉnh sửa cập nhật mục thời gian** có chứa **Dòng thời gian**.

-   Việc phê duyệt thời gian đối với các mục thời gian không có trong dự án sẽ chặn hệ thống khi tìm kiếm vai trò người phê duyệt dự án.

**Quản lý nguồn lực**

Các vấn đề sau đã được khắc phục:

-   Thêm quy trình xác thực trong phần bổ trợ **PostProjectCreate** để kiểm tra yêu cầu chính trước khi tạo.

-   Biểu mẫu tạo nhanh **Thành viên nhóm dự án** trả về ngoại lệ tham chiếu rỗng nếu các trường bị xóa khỏi biểu mẫu.

-   Tạo các yêu cầu trong 12 giờ thay vì 1 năm sẽ không thành công.

-   Cải thiện thông báo lỗi ngoại lệ tham chiếu rỗng trong quá trình tạo yêu cầu nguồn lực.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

-   Cải thiện chức năng xác thực để giải quyết ngoại lệ tham chiếu rỗng trong phần bổ trợ **PreProjectUpdate**.

-   Các dự án do phần bổ trợ của Microsoft Project trên máy tính sẽ xóa những lần phân công chưa giao.

-   Thêm tùy chọn xác thực mới khi tham chiếu dự án của nhiệm vụ không hợp lệ do ngoại lệ tham chiếu rỗng trong phần bổ trợ **PreValidateProjectTaskUpdate**.

-   Lưới Thành viên nhóm không hiển thị các lượt phần công riêng biệt trên bản ghi thành viên nhóm.

-   Thêm tùy chọn xác thực và thông báo lỗi mới do ngoại lệ tham chiếu rỗng trong phần bổ trợ **PreProjectTaskDelete**.

**Sales**

Các vấn đề sau đã được khắc phục:

-   Khi chọn một dòng dựa trên dự án trong báo giá hoặc hợp đồng, nút **Gợi ý** chỉ hiển thị khi chọn một dòng dựa trên sản phẩm có liên kết với sản phẩm hiện tại.

-   Tách quyền **Create_Product** khỏi quyền **Create_ProjectContract**.

-   Thao tác xóa dòng hóa đơn gây ra lỗi tham chiếu rỗng **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
