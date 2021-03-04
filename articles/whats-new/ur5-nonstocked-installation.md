---
title: Cập nhật Project Operations trong môi trường Tài chính
description: Chủ đề này cung cấp thông tin về cách cập nhật Project Operations trong môi trường Dynamics 365 Finance.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816651"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Cập nhật Project Operations trong môi trường Tài chính

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_


Chủ đề này cung cấp thông tin về cách cập nhật Dynamics 365 Project Operations trong môi trường Dynamics 365 Finance. Bạn phải làm theo 3 quy trình để cập nhật Project Operations lên Bản cập nhật 5 (UR5):

- [Nhập gói vào dự án thử nghiệm](#import)
- [Áp dụng bản cập nhật](#apply)
- [Cập nhật môi trường Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Nhập gói vào dự án LCS

1. Đăng nhập vào [Lifecycle Services (LCS)](https://lcs.dynamics.com/) với vai trò Chủ dự án hoặc Người quản lý môi trường.
2. Chọn dự án LCS của bạn từ danh sách dự án.
3. Trên trang **Dự án**, trong nhóm **Môi trường**, hãy mở môi trường bạn muốn cập nhật.
4. Xác nhận rằng môi trường đó đang chạy. Nếu môi trường đó chưa khởi động, hãy khởi động.
5. Trong phần **Bản phát hành mới** ở trang **Các bản cập nhật hiện có**, hãy chọn **Xem bản cập nhật** để tìm bản 10.0.15.

![Nút Xem bản cập nhật](media/view-update.png)

6. Trên trang **Bảng cập nhật nhị phân**, hãy chọn **Lưu gói**.
7. Trên trang **Xem lại và lưu bản cập nhật**, hãy chọn **Lưu gói**.
8. Trên ngăn **Lưu gói vào thư viện tài sản** mở ra, hãy nhập tên gói rồi chọn **Lưu gói**.
9. Khi LCS lưu xong gói, nút **Xong** sẽ sẵn sàng. Chọn **Xong**. LCS sẽ xác minh gói. Quá trình xác minh có thể mất ít phút hoặc tối đa là 1 giờ.


## <a name="apply-the-package-update"></a><a name="apply"></a>Áp dụng bản cập nhật gói

1. Trong LCS, trên trang **Chi tiết môi trường**, hãy chọn **Bảo trì** > **Áp dụng bản cập nhật**.
2. Từ danh sách, hãy chọn gói bạn đã lưu trước đó rồi chọn **Áp dụng**.
3. Chọn **Có** để xác nhận rằng bạn muốn triển khai gói.

![Xác nhận hộp thoại triển khai gói](media/confirm-package-deployment.png)

4. Chọn **Có** để xác nhận rằng bạn muốn cập nhật ứng dụng.

![Xác nhận hộp thoại cập nhật ứng dụng](media/confirm-application-update.png)

Quá trình triển khai và cập nhật ứng dụng sẽ bắt đầu. 

Trên trang **Chi tiết môi trường**, ở góc trên cùng bên phải, trạng thái môi trường sẽ chuyển thành **Đang phục vụ**. Trong khoảng hai giờ, quá trình cập nhật sẽ hoàn tất. Thông tin bản phát hành ứng dụng sẽ chuyển thành **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** và trạng thái môi trường sẽ chuyển thành **Đã triển khai**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Cập nhật môi trường Dataverse

1. Đăng nhập vào [Trung tâm quản trị Power Platform](https://admin.powerplatform.com/).
2. Trong danh sách, hãy tìm và mở môi trường mà bạn đã dùng để cài đặt Project Operations.
3. Trên trang **Môi trường**, hãy chọn **Nguồn lực** > **Ứng dụng Dynamics 365**.
4. Trong danh sách, hãy tìm **Microsoft Dynamics 365 Project Operations** và trong cột **Trạng thái**, hãy chọn **Có sẵn bản cập nhật**.
5. Đánh dấu vào ô **Tôi đồng ý với điều khoản dịch vụ** rồi chọn **Cập nhật**. Phiên bản mới nhất của giải pháp sẽ được cài đặt.

Sau khi cài đặt xong, bạn sẽ có phiên bản 4.5.0.134.

## <a name="configure-new-features"></a>Đặt cấu hình các tính năng mới

### <a name="enable-dual-write-mapping"></a>Bật ánh xạ ghi kép

Sau khi cập nhật xong trên môi trường Tài chính và Dataverse, bạn có thể bật các ánh xạ ghi kép cần thiết. Hãy hoàn tất các quy trình sau để bật ánh xạ ghi kép.

- [Cập nhật các tùy chọn cài đặt bảo mật trên môi trường Customer Engagement](#security)
- [Làm mới các thực thể dữ liệu](#refresh)
- [Cập nhật và chạy các ánh xạ ghi kép](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Cập nhật các tùy chọn cài đặt bảo mật trên môi trường Dataverse

Các chi tiết cập nhật sau đây đối với quyền bảo mật của thực thể là bắt buộc như một phần của bản cập nhật lên UR5.

1. Trong môi trường Dataverse, hãy đi đến **Cài đặt** và trong nhóm **Hệ thống**, hãy chọn **Bảo mật**.

![Cài đặt môi trường Dataverse](media/Picture21.png)

2. Chọn **Vai trò Bảo mật**.
3. Từ danh sách vai trò, hãy chọn **Người dùng ứng dụng ghi kép** rồi chọn tab **Thực thể tùy chỉnh**. 
4. Xác minh rằng vai trò có quyền **Đọc** và **Gắn thêm vào** đối với:

      - **Loại tỷ giá hối đoái**
      - **Biểu đồ tài khoản** 
      - **Lịch tài khóa** 
      - **Sổ cái**

5. Sau khi cập nhật xong vai trò bảo mật, hãy đi đến **Cài đặt** > **Bảo mật** > **Nhóm**. Xác minh rằng vai trò **người dùng ứng dụng ghi kép** đã được áp dụng cho nhóm. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Làm mới các thực thể dữ liệu từ bản cập nhật

1. Trong môi trường Tài chính, hãy mở không gian làm việc **Quản lý dữ liệu** rồi mở trang **Tham số khuôn khổ**.
2. Trên tab **Cài đặt thực thể**, hãy chọn **Làm mới danh sách thực thể**.
3. Chọn **Đóng** để xác nhận việc làm mới thực thể.

 > [!NOTE]
 > Quá trình này sẽ mất khoảng 20 phút để hoàn tất. Bạn sẽ được thông báo khi quá trình làm mới hoàn tất.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Cập nhật ánh xạ ghi kép

1. Trong không gian làm việc **Quản lý dữ liệu**, hãy chọn **Ghi kép**.
2. Chọn **Áp dụng giải pháp**, chọn cả 2 giải pháp trong danh sách rồi chọn **Áp dụng**.
3. Trên trang **Ghi kép**, chọn các sơ đồ bảng sau rồi chọn **Dừng**.

    - **Giá trị tích hợp thực tế của Project Operations (msdyn_actuals)**
    - **Hạng mục chi tiêu dự án tích hợp trong Project Operations (msdyn_expensecategories)**
    - **Thực thể xuất chi tiêu dự án thực tích hợp trong Project Operations (msdyn_expenses)**

4. Trên trang **Phiên bản sơ đồ bảng**, hãy áp dụng phiên bản mới của bảng cho từng thực thể trong số 3 thực thể.
5. Trên trang **Ghi kép**, hãy chọn chạy để khởi động lại sơ đồ.
6. Từ danh sách sơ đồ, hãy chọn **Sổ cái (msdyn_ledgers)** ánh xạ với mọi yêu cầu tiên quyết rồi đánh dấu vào ô **Đồng bộ ban đầu**. 
7. Trong trường **Đối tượng chính cho đồng bộ hóa ban đầu**, hãy chọn **ứng dụng Finance and Operations** rồi chọn **Chạy**.
 
 ![Đồng bộ hóa sơ đồ sổ cái](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]