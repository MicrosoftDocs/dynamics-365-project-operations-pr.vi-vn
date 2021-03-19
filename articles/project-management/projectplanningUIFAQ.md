---
title: Khắc phục sự cố khi làm việc trong lưới Tác vụ
description: Chủ đề này cung cấp thông tin khắc phục sự cố cần thiết khi làm việc trong lưới Tác vụ.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286589"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Khắc phục sự cố khi làm việc trong lưới Tác vụ 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này mô tả cách khắc phục các vấn đề bạn có thể gặp phải khi làm việc với quản lý chi phí.

## <a name="enable-cookies"></a>Bật cookie

Project Operations yêu cầu bật cookie của bên thứ ba để kết xuất cấu trúc phân tích công việc. Khi cookie của bên thứ ba không được bật, thay vì thấy các nhiệm vụ, bạn sẽ thấy trang trống khi chọn tab **Nhiệm vụ** trên trang **Dự án**.

![Tab trống khi cookie của bên thứ ba không được bật](media/blankschedule.png)


### <a name="workaround"></a>Giải pháp thay thế
Đối với Microsoft Edge hoặc trình duyệt Google Chrome, các quy trình sau đây trình bày cách cập nhật cài đặt trình duyệt của bạn để bật cookie của bên thứ ba.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Mở trình duyệt Edge.
2. Ở góc trên bên phải, chọn biểu tượng **dấu chấm lửng** (...), sau đó chọn **Cài đặt**.
3. Trong **Cookie và quyền đối với trang web**, chọn **Cookie và dữ liệu trang web**.
4. Tắt tùy chọn **Chặn cookie bên thứ ba**.

#### <a name="google-chrome"></a>Google Chrome

1. Mở trình duyệt Chrome.
2. Ở góc trên bên phải, chọn dấu 3 chấm dọc, sau đó chọn **Cài đặt**.
3. Trong **Quyền riêng tư và bảo mật**, chọn **Cookie và dữ liệu khác của trang web**.
4. Chọn **Cho phép tất cả cookie**.

> [!IMPORTANT]
> Nếu bạn chặn cookie của bên thứ ba, tất cả cookie và dữ liệu trang web từ các trang web khác sẽ bị chặn, ngay cả khi trang web đó được cho phép trong danh sách ngoại lệ của bạn.

## <a name="pex-endpoint"></a>Điểm cuối PEX

Project Operations yêu cầu tham số dự án tham chiếu đến Điểm cuối PEX. Điểm cuối này phải giao tiếp được với dịch vụ được sử dụng để kết xuất cấu trúc phân tích công việc. Nếu tham số không được bật, bạn sẽ nhận được lỗi "Tham số dự án không hợp lệ". 

### <a name="workaround"></a>Giải pháp thay thế
 ![Trường Điểm cuối PEX trên tham số dự án](media/projectparameter.png)

1. Thêm trường **Điểm cuối PEX** vào trang **Tham số dự án**.
2. Cập nhật trường này với giá trị sau: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Xóa trường khỏi trang **Tham số dự án**.

## <a name="privileges-for-project-for-the-web"></a>Đặc quyền cho Dự án cho Web

Project Operations dựa vào một dịch vụ lập lịch bên ngoài. Dịch vụ này yêu cầu người dùng được chỉ định nhiều vai trò để đọc và ghi cho các thực thể liên quan đến cấu trúc phân tích công việc. Các thực thể này bao gồm nhiệm vụ dự án, phân công nguồn lực và mức phụ thuộc nhiệm vụ. Nếu người dùng không thể kết xuất cấu trúc phân tích công việc khi họ truy cập tab **Nhiệm vụ**, có thể là do chưa bật Dự án cho Project Operations. Người dùng có thể nhận được lỗi vai trò bảo mật hoặc lỗi liên quan đến từ chối quyền truy cập.


## <a name="workaround"></a>Giải pháp thay thế

1. Đi đến **Cài đặt > Bảo mật > Người dùng > Người dùng ứng dụng**.  

   ![Trình đọc ứng dụng](media/applicationuser.jpg)
   
2. Nhấp đúp vào hồ sơ người dùng ứng dụng để xác minh những nội dung sau:

 - Người dùng có quyền truy cập vào dự án. Việc xác minh này thường được thực hiện qua việc đảm bảo rằng người dùng có vai trò bảo mật là **Quản lý dự án**.
 - Người dùng ứng dụng Microsoft Project tồn tại và được định cấu hình chính xác.
 
3. Nếu người dùng này chưa tồn tại, bạn có thể tạo bản ghi người dùng mới. Chọn **Người dùng mới**. Thay đổi biểu mẫu nhập thành **Người dùng Ứng dụng**, sau đó thêm **ID ứng dụng**.

   ![Chi tiết người dùng ứng dụng](media/applicationuserdetails.jpg)

4. Xác minh rằng người dùng đã được gán đúng giấy phép và dịch vụ được bật trong chi tiết gói dịch vụ của giấy phép.
5. Xác minh rằng người dùng có thể mở project.microsoft.com.
6. Xác minh thông qua các thông số dự án rằng hệ thống đang trỏ đến đúng điểm cuối dự án.
7. Xác minh rằng người dùng ứng dụng dự án được tạo.
8. Áp dụng các vai trò bảo mật sau cho người dùng:

  - Người dùng Dataverse
  - Hệ thống Project Operations
  - Hệ thống Dự án

## <a name="error-when-updating-the-work-breakdown-structure"></a>Lỗi khi cập nhật cấu trúc phân tích công việc

Khi có một hoặc nhiều bản cập nhật cho cấu trúc phân tích công việc, các thay đổi cuối cùng không thành công và không được lưu. Lỗi xảy ra trong lưới lịch trình ghi chú rằng "Không thể lưu thay đổi bạn thực hiện gần đây".

### <a name="workaround"></a>Giải pháp thay thế

1. Xác minh rằng người dùng đã được gán đúng giấy phép và dịch vụ được bật trong chi tiết gói dịch vụ của giấy phép.
2. Xác minh rằng người dùng có thể mở project.microsoft.com.
3. Xác minh rằng hệ thống đang trỏ đến đúng điểm cuối dự án.
4. Xác minh rằng người dùng Ứng dụng Dự án đã được tạo.
5. Áp dụng các vai trò bảo mật sau cho người dùng:
  
  - Người dùng Dataverse hoặc người dùng Cơ sở
  - Hệ thống Project Operations
  - Hệ thống Dự án
  - Hệ thống ghi kép của Project Operations (Vai trò này là bắt buộc nếu bạn đang triển khai kịch bản dựa trên nguồn lực/hàng không nhập kho của Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]