---
title: Áp dụng dữ liệu demo của Project Operations cho môi trường Finance được lưu trữ trên đám mây
description: Chủ đề này sẽ giải thích cách áp dụng dữ liệu demo từ Project Operations cho môi trường Dynamics 365 Finance được lưu trữ trên đám mây.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949145"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>Áp dụng dữ liệu demo của Project Operations cho môi trường Finance được lưu trữ trên đám mây

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

>[Quan trọng] Chủ đề này chỉ có thể áp dụng cho Microsoft Dynamics 365 Finance phiên bản 10.0.13 và chỉ có thể được thực hiện trên môi trường được lưu trữ trên đám mây. Hoàn thành các bước trong chủ đề này **TRƯỚC** khi bạn áp dụng các bản cập nhật chất lượng cho môi trường.

1. Trong dự án LCS của bạn, hãy mở trang **Chi tiết môi trường**. Lưu ý rằng trang này bao gồm các chi tiết cần thiết để kết nối với môi trường bằng cách sử dụng Giao thức Máy tính Từ xa (RDP).

![Chi tiết môi trường ](./media/1EnvironmentDetails.png)

Bộ thông tin xác thực được đánh dấu đầu tiên là thông tin xác thực tài khoản cục bộ và chứa siêu liên kết đến kết nối máy tính từ xa. Thông tin xác thực bao gồm tên người dùng và mật khẩu quản trị môi trường. Bộ thông tin xác thực thứ hai được sử dụng để đăng nhập vào SQL Server trong môi trường này.

2. Kết nối với môi trường bằng siêu liên kết trong **Tài khoản cục bộ** và sử dụng **Thông tin xác thực tài khoản cục bộ** để xác thực.
3. Chuyển đến **Dịch vụ thông tin Internet** > **Bộ ứng dụng** > **AOSService** và ngừng dịch vụ. Bạn hiện đang ngừng dịch vụ để có thể tiếp tục thay thế cơ sở dữ liệu SQL.

![Ngừng AOS](./media/2StopAOS.png)

4. Chuyển đến **Dịch vụ** và ngừng hai mục sau:

- Microsoft Dynamics 365 Unified Operations: Dịch vụ quản lý lô
- Microsoft Dynamics 365 Unified Operations: Khung xuất nhập dữ liệu

![Ngừng dịch vụ](./media/3StopServices.png)

5. Mở Microsoft SQL Server Management Studio. Đăng nhập bằng thông tin xác thực SQL server và sử dụng mật khẩu và người dùng axdbadmin từ trang **Chi tiết môi trường** LCS.

![SQL Server Management Studio](./media/4SSMS.png)

6. Trong Trình khám phá đối tượng, **Cơ sở dữ liệu** và xác định vị trí **AXDB**. Bạn sẽ thay thế cơ sở dữ liệu bằng một cơ sở dữ liệu mới nằm trong [Trung tâm tải xuống](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Sao chép tệp zip vào máy ảo mà bạn được điều khiển từ xa rồi giải nén nội dung tệp zip.
8. Trong SQL Server Management Studio, hãy nhấp chuột phải vào **AxDB** rồi chọn **Nhiệm vụ** > **Khôi phục** > **Cơ sở dữ liệu**.

![Khôi phục cơ sở dữ liệu](./media/5RestoreDatabase.png)

9. Chọn **Thiết bị nguồn** và điều hướng đến tệp được giải nén từ tệp zip bạn đã sao chép.

![Thiết bị nguồn](./media/6SourceDevice.png)

10. Chọn **Tùy chọn** rồi chọn **Ghi đè cơ sở dữ liệu hiện có** và **Đóng các kết nối hiện có đến cơ sở dữ liệu đích**. 
11. Chọn **OK**.

![Khôi phục thiết đặt](./media/7RestoreSetting.png)

Bạn sẽ nhận được xác nhận rằng khôi phục AXDB đã thành công. Sau khi nhận được xác nhận này, bạn có thể đóng SQL Services Management Studio.

12. Quay lại **Dịch vụ thông tin Internet** > **Bộ ứng dụng** > **AOSService** và bắt đầu AOSService.
13. Chuyển đến **Dịch vụ** và bắt đầu hai dịch vụ bạn đã ngừng trước đó.

14. Xác định vị trí công cụ AdminUserProvisioning trên máy ảo này. Xem trong phần K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Chạy tệp .ext bằng địa chỉ người dùng của bạn trong trường **Địa chỉ email**. 
16. Chọn **Gửi**.

![Cung cấp Người dùng là quản trị viên](./media/8AdminUserProvisioning.png)

Quá trình này mất vài phút để hoàn thành. Bạn sẽ nhận được thông báo xác nhận rằng Người dùng là quản trị viên đã được cập nhật thành công.

17. Cuối cùng, chạy Dấu nhắc lệnh với tư cách là Quản trị viên và thực hiện iisreset

![Đặt lại IIS](./media/9IISReset.png)

18. Đóng phiên máy tính từ xa và sử dụng trang **Môi trường chi tiết** LCS để đăng nhập vào môi trường để xác nhận rằng môi trường đang hoạt động như mong đợi.

![Finance and Operations](./media/10FinanceAndOperations.png)
