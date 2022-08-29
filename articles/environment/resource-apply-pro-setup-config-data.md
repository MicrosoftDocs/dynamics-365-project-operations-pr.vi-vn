---
title: Thiết lập và áp dụng dữ liệu cấu hình trong Microsoft Dataverse
description: Bài viết này cung cấp thông tin về cách thiết lập và áp dụng dữ liệu cấu hình trong Hoạt động dự án.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b09d3ea7348082a0467fd7b47918c9e00d1f1e8c
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230278"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Thiết lập và áp dụng dữ liệu cấu hình trong Common Data Service 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_



## <a name="prerequisites"></a>Điều kiện tiên quyết

Trước khi bạn bắt đầu định cấu hình dữ liệu trong Microsoft Dataverse, các điều kiện tiên quyết sau phải được đáp ứng:

1.  Điều khoản a Dataverse và môi trường Dynamics 365 Finance cho Hoạt động dự án.
2.  Thông tin pháp nhân từ Dynamics 365 Finance được chia sẻ với Dataverse Môi trường. Điều này có nghĩa là **Công ty** thực thể trong Dataverse có hồ sơ công ty sau:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Cài đặt dữ liệu cấu hình và thiết lập

1. Tải xuống, bỏ chặn và giải nén [Gói dữ liệu cấu hình và thiết lập](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Chuyển đến thư mục đã giải nén rồi chạy tệp thực thi là *DataMigrationUtility*.
3. Trên trang 1 của Trình hướng dẫn di chuyển cấu hình (CMT) Common Data Service, hãy chọn **Nhập dữ liệu** và sau đó chọn **Tiếp tục**.

![Di chuyển cấu hình.](./media/1ConfigurationMigration.png)

4. Trên Trang 2 của Trình hướng dẫn CMT, hãy chọn **Microsoft 365** làm **Loại triển khai**.
5. Chọn **Hiển thị danh sách tổ chức khả dụng** và hộp kiểm **Hiển thị nâng cao**.
6. Chọn khu vực của đối tượng thuê của bạn, nhập thông tin xác thực của bạn rồi chọn **Đăng nhập**.

![Đăng nhập cấu hình.](./media/2ConfigurationSignin.png)

7. Trên trang 3, từ danh sách tổ chức trên đối tượng thuê, hãy chọn tổ chức bạn muốn nhập dữ liệu demo vào rồi chọn **Đăng nhập**.
8. Trên trang 4, hãy chọn tệp zip là *SampleSetupAndConfigData* từ thư mục đã giải nén.

![Chọn tệp zip.](./media/3ZipFile.png)

![Chọn một tệp.](./media/4SelectAFile.png)

9. Sau khi chọn tệp zip, hãy chọn **Nhập dữ liệu**.

![Nhập dữ liệu.](./media/5ImportData.png)

10. Quá trình nhập sẽ chạy trong khoảng hai mười phút tùy thuộc vào tốc độ mạng của bạn. Sau khi hoàn tất quá trình nhập, hãy thoát khỏi Trình hướng dẫn CMT. 
11. Kiểm tra tổ chức của bạn để tìm dữ liệu trong 26 thực thể sau:

  - Tiền tệ
  - Biểu đồ tài khoản
  - Lịch tài khóa
  - Các loại tỷ giá hối đoái
  - Ngày thanh toán
  - Lịch trình thanh toán
  - Điều khoản Thanh toán
  - Đơn vị tổ chức
  - Liên hệ
  - Nhóm thuế
  - Nhóm khách hàng
  - Nhóm nhà cung cấp
  - Đơn vị
  - Nhóm đơn vị đo
  - Bảng giá
  - Bảng giá Tham số Dự án
  - Tuần suất hóa đơn
  - Thể loại Nguồn lực có thể đăng ký trước
  - Thể loại giao dịch
  - Thể loại Chi phí
  - Giá Vai trò
  - Giá cả Thể loại Giao dịch
  - Đặc tính
  - Nguồn lực có thể đăng ký
  - LK thể loại nguồn lực có thể đăng ký trước
  - Đặc điểm Nguồn lực có thể đặt trước

![Hoàn thành quá trình nhập.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Cập nhật cấu hình Project Operations

1. Điều hướng tới môi trường CE. Bạn có thể tìm môi trường này bằng cách mở [Trung tâm quản trị Power Platform](https://admin.powerplatform.microsoft.com/environments), chọn môi trường, sau đó chọn **Mở môi trường**. 

![Mở môi trường.](./media/7OpenEnvironment.png)

2. Chuyển đến **Dự án** > **Nguồn lực** rồi chọn **Mới** để tạo nguồn lực có thể đăng ký trước cho người dùng của bạn.

![Nguồn lực có thể đặt trước.](./media/8BookableResources.png)

3. Trên tab **Tổng quát**, hãy chọn người dùng là quản trị viên của bạn. Xác minh rằng múi giờ khớp với múi giờ bạn đang ở. 

![Nguồn lực mới có thể đăng ký trước.](./media/9NewBookableResource.png)

4. Trên tab **Lên lịch**, trong trường **Công ty**, hãy chọn công ty **USPM** rồi chọn **Lưu**. 

![Tab Lên lịch.](./media/10SchedulingTab.png)

5. Chọn tab **Giờ làm việc**.  

![Giờ làm việc.](./media/11WorkHours.png)

6. Nhấp đúp chuột vào bất kỳ giá trị nào trong lịch và chọn **Chỉnh sửa** > **Tất cả các sự kiện trong chuỗi**. 

![Lịch làm việc.](./media/12WorkCalendar.png)

7. Thay đổi giờ làm việc thành một ngày làm việc tám (8) giờ, đánh dấu các ngày cuối tuần là ngày không làm việc và đảm bảo múi giờ khớp với múi giờ của bạn. 
8. Chọn **Lưu và đóng**.

![Cập nhật lịch.](./media/13UpdateCalendar.png)

9. Chuyển đến **Thiết đặt** > **Các mẫu lịch** và chọn **Mới**.
 
 ![Mẫu lịch.](./media/14CalendarTemplates.png)
 
 10. Nhập tên, chọn nguồn lực mẫu bạn đã tạo, sau đó chọn **Lưu**. 
 
 ![Lưu mẫu lịch.](./media/15SaveCalendarTemplate.png)
 
 11. Chuyển đến **Tham số** và nhấp đúp vào bản ghi. 
 
 ![Tham số Dự án.](./media/16ProjectParameters.png)
 
12. Cập nhật các trường sau:

 - **Công ty mặc định**: USPM
 - **Đơn vị tổ chức mặc định**: Contoso Robotics Global
 - **Tần suất hóa đơn** : Ngày thứ bảy và ngày cuối cùng
 - **Mẫu giờ làm việc** : Thay đổi mẫu bạn đã tạo.

13. Chọn **Lưu**. 

![Đã cập nhật tham số dự án.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
