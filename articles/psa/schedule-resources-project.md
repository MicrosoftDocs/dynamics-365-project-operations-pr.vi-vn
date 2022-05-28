---
title: Lên lịch các nguồn lực cho dự án
description: Làm cách nào để lên lịch nguồn lực cho dự án trong Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583150"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Lên lịch nguồn lực cho dự án (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Bạn có thể kiểm tra nguồn lực sẵn có để có được một cái nhìn tổng thể về cách đặt nguồn lực của bạn hoặc bạn có thể lọc xem theo kỹ năng, nhóm, vị trí và các tùy chọn khác.  
  
Bảng lịch trình hiển thị danh sách các nguồn lực và tính sẵn có của nguồn lực. Chọn một dạng xem để hiển thị tính sẵn có theo **Giờ**, **Ngày**, **Tuần** hoặc **Tháng**.  
  
Trước khi sử dụng bảng lịch trình, bạn cần thiết lập bảng đó. Để biết thêm thông tin, hãy xem phần [Đặt cấu hình bảng lịch trình (Field Service hoặc Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Nếu bạn đang sử dụng phiên bản cũ, để tìm hiểu về tính sẵn có của nguồn lực, hãy xem phần [Xem tính sẵn có của nguồn lực](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Để sử dụng chức năng đặt trước bảng thông tin lịch trình, mã hóa địa lý và dịch vụ vị trí, bạn cần bật bản đồ.  
> 
> 1. Trên menu chính, hãy chọn **Lập lịch trình Nguồn lực** > **Quản trị**.  
> 2. Bấm vào **Tham số lập lịch trình**.  
> 3. Mở bản ghi rồi cuộn xuống phần **Resource Scheduling Optimization**.  
> 4. Trên trường **Kết nối với Bản đồ**, chọn **Có**.  
> 5. Chấp nhận điều khoản và lưu bản ghi.  
> 6. Trên menu chính, hãy chọn **Project Service** > **Bảng lịch trình**. Từ đây, có vài cách để lên lịch thủ công một yêu cầu đăng ký. Chọn phương thức phù hợp với bạn.
  
## <a name="find-available-resources"></a>Tìm nguồn lực sẵn có

1.  Từ danh sách **Yêu cầu Đăng ký**, bấm chuột phải một đăng ký chưa được lên lịch và chọn một trong các cách sau:  
  
- Chọn **Tìm tính sẵn có – Nguồn lực hiện tại** để tìm kiếm nguồn lực có sẵn từ danh sách trên bảng lịch trình.  
- Chọn **Tìm tính sẵn có – Tất cả Nguồn lực** để tìm kiếm nguồn lực có sẵn từ các nguồn lực trong hệ thống  
   > [!NOTE]
   >  Khi bạn thực hiện điều này, các bộ lọc sẽ hiển thị tùy chọn cho yêu cầu đặt trước đã chọn.  
  
2. Khi bạn thấy một vị trí có sẵn, hãy nhấp chuột phải vào vị trí thời gian trên bảng lịch trình và chọn **Đăng ký Tại đây**. Hoặc, kéo và thả yêu cầu đăng ký vào vị trí thời gian có sẵn.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Đăng ký nguồn lực bằng cách sử dụng dạng xem hàng ngày và xem những ai còn trống lịch
  
1.  Trên bảng lịch trình, hãy chọn **Chế độ Xem** rồi chọn **Ngày**.  
  
    Thao tác này sẽ hiển thị dạng xem lưới về số giờ một nguồn lực được đăng ký mỗi ngày và ngày nào nguồn lực đó rảnh.  
  
2.  Nhấp vào tên nguồn lực bạn muốn đăng ký rồi chọn **Đăng ký**.  
  
3.  Trên hộp thoại **Đăng ký nguồn lực (tạo)**, hãy chọn dự án mà bạn muốn đăng ký nguồn lực cùng với phương pháp đăng ký và thời gian bắt đầu cũng như kết thúc.  
  
4.  Sau khi hoàn tất, hãy chọn **Đăng ký**.  
  
## <a name="view-to-the-schedule-board"></a>Dạng xem của bảng lịch trình
  
1.  Chọn một yêu cầu đặt trước chưa lên lịch từ danh sách ở dưới cùng.  
  
2.  Kéo yêu cầu đăng ký đến vị trí thời gian/nguồn lực có sẵn trên bảng lịch trình.  
  
3.  Sau khi hoàn tất, hãy chọn **Đăng ký**.  
  
### <a name="additional-resources"></a>Tài nguyên bổ sung  
 [Hướng dẫn của người quản lý nguồn lực](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
