---
title: Đồng bộ hóa Trạng thái dự án để ngăn chặn việc xâm nhập vào các dự án đã đóng
description: Bài viết này giải thích cách đồng bộ hóa Trạng thái dự án để ngăn chặn việc xâm nhập vào các dự án không hoạt động hoặc đã đóng.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348123"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Đồng bộ hóa Trạng thái dự án để ngăn chặn việc xâm nhập vào các dự án đã đóng

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

## <a name="scenario"></a>Kịch bản

Contoso đang phát trực tiếp với Microsoft Dynamics 365 Project Operations cho các tình huống tài nguyên / không có hàng. Là một phần của các hoạt động kinh doanh thông thường, các dự án có thể được hoàn thành hoặc tạm dừng. Bạn có thể hủy kích hoạt dự án để đảm bảo không có chi phí hoặc hóa đơn nào được tạo ra.

## <a name="solution"></a>Giải pháp

### <a name="prerequisites"></a>Điều kiện tiên quyết

-   Microsoft Dynamics 365 Finance 10.0.29 trở lên phải được cài đặt.
-   Bản đồ Ghi kép 1.0.0.3 cho Dự án V2 (msdyn\_ dự án) phải được cài đặt hoặc cấu hình thủ công như mô tả bên dưới.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Tạo phiên bản cập nhật của bản đồ tích hợp Hoạt động Dự án Bản đồ ghi kép Projects V2

Để cập nhật bản đồ ghi kép Project Operations Projects V2:

1. Đi đến **Quản lý dữ liệu** không gian làm việc và chọn **Viết kép**.
2. Chọn **Viết kép** ngói.
3. Từ T **Sơ đồ bảng** cột, định vị và chọn **Dự án V2 (msdyn\_ dự án)**, rồi chọn Dừng.
4. Chọn tên bản đồ để mở bản đồ và sau đó chọn **[Không có]**.
5. Từ hộp thoại Chọn cột, hãy chọn **mã trạng thái\[ Tình trạng của dự án\]** và sau đó chọn OK. Bạn có thể gõ **tiểu bang** trong giá trị bộ lọc để thu hẹp danh sách.
6.  Lựa chọn **Thêm hoặc chỉnh sửa chuyển đổi** bên trong **loại bản đồ** để chỉnh sửa biến đổi.
7.  Từ **Biến đổi kiểu** lựa chọn **Bản đồ giá trị**.
8.  Lựa chọn **Thêm ánh xạ giá trị**, và sau đó thêm phần sau **Chìa khóa** và **Giá trị**:

   Khóa       | Giá_trị 
   ----------|-------
   Đang tiến hành | 0     
   đã hoàn thành | 1     

![Ảnh chụp màn hình hiển thị ánh xạ ghi kép](media/projectstage-dw-mapping.png)

9. Chọn **Lưu.**
10. Từ trên cùng của **Ghi kép> Dự án V2 (msdyn_projects)** trang, chọn **Lưu thành**.
11. Từ **Thêm bảng** bên trong **Nhà xuất bản** trường, chọn **Nhà xuất bản Mặc định CDS**.
12. Đặt **Phiên bản** trường tới 1.0.0.3.
13. Gõ a **Sự mô tả**, và sau đó chọn **Tiết kiệm**.
14. Từ trên cùng của **Ghi kép> Dự án V2 (msdyn_projects)** trang, chọn **Chạy** để bắt đầu bản đồ, và sau đó cắt **Đúng** nếu được yêu cầu xác nhận trước khi chạy. 

### <a name="close-a-newly-completed-project"></a>Đóng một dự án mới hoàn thành

Dynamics 365 Finance sử dụng **giai đoạn dự án** lĩnh vực để phân biệt giữa các dự án **đang tiến hành** hoặc **hoàn thành**. **Hoàn thành** các dự án không thể phát sinh chi phí hoặc được lập hóa đơn cho khách hàng.

1. Mở một dự án để hủy kích hoạt.
2. Từ ruy-băng, hãy chọn **Hủy kích hoạt**.

> [!NOTE]
> Bạn có thể hủy kích hoạt hoặc đóng một dự án vì cả hai đều sẽ hoạt động giống nhau trong bối cảnh Tài chính.

3. Trong Tài chính, hãy mở **Tất cả các dự án danh sách** trang.
4. Xác nhận rằng dự án đã hủy kích hoạt không xuất hiện trong danh sách.
5. Bên trong **hiển thị các dự án** lọc phía trên danh sách, thay đổi giá trị từ **Tích cực** đến **Tất cả các**.
6. Bây giờ bạn sẽ thấy dự án đã hủy kích hoạt.

Nếu bạn cố gắng ghi lại thời gian hoặc chi phí cho dự án này trong Tài chính, bạn sẽ không thấy dự án để lựa chọn. Nếu bạn nhập thủ công số dự án trên một khoản chi phí, bạn sẽ thấy thông báo như "Giai đoạn dự án đã kết thúc không cho phép ghi trong dự án". Lập hóa đơn và các chức năng thanh toán khác nên bị vô hiệu hóa vì chúng sẽ ở trong bối cảnh của một dự án đã đóng.

