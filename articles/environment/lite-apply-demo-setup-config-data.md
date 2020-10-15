---
title: Áp dụng dữ liệu cấu hình và thiết lập demo
description: Chủ đề này cung cấp thông tin về cách áp dụng dữ liệu cấu hình và thiết lập demo cho Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949137"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Áp dụng dữ liệu cấu hình và thiết lập demo để triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá

_**Triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá_

1. Tải [Gói dữ liệu chính](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) xuống. 
2. Chuyển đến thư mục *ProjOpsDemoDataSetupAndMaster - Integrated CMT* rồi chạy tệp thực thi là *DataMigrationUtility*.
3. Trên trang 1 của Trình hướng dẫn di chuyển cấu hình (CMT) Common Data Service, hãy chọn **Nhập dữ liệu** và sau đó chọn **Tiếp tục**.

![Di chuyển cấu hình](./media/1ConfigurationMigration.png)

4. Trên Trang 2 của Trình hướng dẫn CMT, hãy chọn **Office 365** làm **Loại triển khai**.
5. Chọn **Hiển thị danh sách tổ chức khả dụng** và hộp kiểm **Hiển thị nâng cao**.
6. Chọn khu vực của đối tượng thuê của bạn, nhập thông tin xác thực của bạn, sau đó chọn **Đăng nhập**.

![Đăng nhập cấu hình](./media/2ConfigurationSignin.png)

7. Trên trang 3, từ danh sách Tổ chức trên Đối tượng thuê, hãy chọn tổ chức bạn muốn nhập dữ liệu demo vào rồi chọn **Đăng nhập**.
8. Trên trang 4, hãy chọn tệp zip là *MasterAndSetupData* từ thư mục đã giải nén là *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Tệp Zip](./media/3ZipFile.png)

![Chọn tệp](./media/4SelectAFile.png)

9. Sau khi chọn tệp zip, hãy chọn **Nhập dữ liệu**.

![Nhập dữ liệu](./media/5ImportData.png)

10. Quá trình nhập sẽ chạy trong khoảng hai mười phút tùy thuộc vào tốc độ mạng của bạn. Sau khi hoàn tất, hãy thoát khỏi CMT Wizard. 
11. Kiểm tra tổ chức của bạn để tìm dữ liệu trong 20 thực thể sau:

- Tiền tệ
- Đơn vị tổ chức
- Liên hệ
- Nhóm thuế
- Nhóm khách hàng
- Đơn vị
- Nhóm đơn vị
- Bảng giá
- Bảng giá Tham số Dự án
- Tuần suất hóa đơn
- Chi tiết Tuần suất Hóa đơn
- Thể loại Nguồn lực có thể đăng ký trước
- Thể loại giao dịch
- Thể loại Chi phí
- Giá Vai trò
- Giá cả Thể loại Giao dịch
- Đặc tính
- Nguồn lực có thể đăng ký
- LK thể loại nguồn lực có thể đăng ký trước
- Đặc tính Nguồn lực có thể đăng ký trước

![Hoàn thành quá trình nhập](./media/6CompleteImport.png)
