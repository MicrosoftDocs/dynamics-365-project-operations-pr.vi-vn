---
title: Đồng bộ hóa Trạng thái dự án để ngăn nhập dữ liệu vào các dự án đã đóng
description: Bài viết này giải thích cách đồng bộ hóa Trạng thái dự án để ngăn chặn việc nhập vào các dự án không hoạt động hoặc đã đóng.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Đồng bộ hóa Trạng thái dự án để ngăn nhập dữ liệu vào các dự án đã đóng

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

## <a name="scenario"></a>Kịch bản

Contoso sẽ thực hiện chính thức với Microsoft Dynamics 365 Project Operations cho các trường hợp nguồn lực/không tồn kho. Là một phần của các hoạt động kinh doanh thông thường, các dự án có thể được hoàn thành hoặc tạm dừng. Bạn có thể hủy kích hoạt dự án để đảm bảo không có chi phí hoặc hóa đơn nào được tạo.

## <a name="solution"></a>Giải pháp

### <a name="prerequisites"></a>Điều kiện tiên quyết

-   Microsoft Dynamics 365 Finance 10.0.29 trở lên phải được cài đặt.
-   Ánh xạ Ghi kép 1.0.0.3 cho Dự án V2 (msdyn\_ projects) phải được cài đặt hoặc định cấu hình thủ công như mô tả bên dưới.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Tạo phiên bản cập nhật của ánh xạ ghi kéo Dự án V2 tích hợp Project Operations

Để cập nhật ánh xạ ghi kéo Dự án V2 Project Operations:

1. Chuyển đến không gian làm việc **Quản lý dữ liệu** và chọn **Ghi kép**.
2. Chọn ngăn xếp **Ghi kép**.
3. từ cột **Ánh xạ bảng**, tìm và chọn **Dự án V2 (msdyn\_projects)**, sau đó chọn Dừng.
4. Chọn tên ánh xạ để mở ánh xạ rồi chọn **[Không có]**.
5. Từ hộp thoại Chọn cột, hãy chọn **statecode \[Project Status\]** và sau đó chọn OK. Bạn có thể nhập **state** vào trong giá trị bộ lọc để thu hẹp danh sách.
6.  Chọn **Thêm hoặc chỉnh sửa chuyển đổi** trong cột **loại bản đồ** để chỉnh sửa mục chuyển đổi.
7.  Từ **Loại chuyển đổi**, chọn **ValueMap**.
8.  Chọn **Thêm ánh xạ giá trị**, và sau đó thêm các **Khóa** và **Giá trị** sau đây:

   Khóa       | Giá_trị 
   ----------|-------
   InProcess | 0     
   đã hoàn thành | 1     

![Ảnh chụp màn hình cho thấy ánh xạ Ghi kép](media/projectstage-dw-mapping.png)

9. Chọn **Lưu.**
10. Từ trên cùng của trang **Ghi kép > Dự án V2 (msdyn_projects)**, chọn **Lưu thành**.
11. Từ **Thêm bảng**, trong trường **Nhà phát hành**, chọn **Nhà phát hành mặc định CDS**.
12. Đặt trường **Phiên bản** thành 1.0.0.3.
13. Nhập **Mô tả** rồi chọn **Lưu**.
14. Từ trên cùng của trang **Ghi kép> Dự án V2 (msdyn_projects)**, chọn **Chạy** để bắt đầu ánh xạ, và sau đó chọn **Có** nếu được yêu cầu xác nhận trước khi chạy. 

### <a name="close-a-newly-completed-project"></a>Đóng một dự án mới hoàn thành

Dynamics 365 Finance sử dụng trường **giai đoạn dự án** để phân biệt giữa các dự án **đang tiến hành** hoặc **đã hoàn thành**. Các dự án **đã hoàn thành** không thể phát sinh chi phí hoặc được lập hóa đơn cho khách hàng.

1. Mở một dự án để hủy kích hoạt.
2. Từ ruy băng, chọn **Hủy kích hoạt**.

> [!NOTE]
> Bạn có thể hủy kích hoạt hoặc đóng một dự án vì cả hai đều sẽ hoạt động giống nhau trong bối cảnh Tài chính.

3. Trong phần Tài chính, hãy mở trang **Tất cả các dự án danh sách**.
4. Xác nhận dự án đã hủy kích hoạt không xuất hiện trong danh sách.
5. Trong bộ lọc **hiển thị dự án** bên trên danh sách, thay đổi thứ tự từ **Hiện hoạt** thành **Tất cả**.
6. Bây giờ bạn sẽ thấy dự án đã hủy kích hoạt.

Nếu bạn cố gắng ghi lại thời gian hoặc chi phí cho dự án này trong Tài chính, bạn sẽ không thấy dự án để lựa chọn. Nếu bạn nhập thủ công số dự án trên một khoản chi phí, bạn sẽ thấy thông báo như "Giai đoạn dự án đã kết thúc không cho phép ghi trong dự án". Lập hóa đơn và các chức năng thanh toán khác nên bị vô hiệu hóa vì chúng sẽ ở trong bối cảnh của một dự án đã đóng.

