---
title: Áp dụng dữ liệu cấu hình và thiết lập bản demo – bản đơn giản
description: Bài viết này cung cấp thông tin về cách áp dụng dữ liệu cấu hình và thiết lập demo cho Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410068"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Áp dụng dữ liệu cấu hình và thiết lập bản demo cho Project Operations – bản đơn giản 

_**Triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá_



## <a name="prerequisites"></a>Điều kiện tiên quyết

Trước khi bắt đầu cấu hình, bạn phải cung cấp môi trường Dataverse cho Dynamics 365 Project Operations.


## <a name="instructions"></a>Hướng dẫn

1. Tải [Gói dữ liệu chính](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip) xuống. 
2. Điều hướng đến thư mục *ProjOpsSampleSetupData - CE only CMT* và chạy tệp thực thi *DataMigrationUtility*.
3. Trên trang 1 của Trình hướng dẫn di chuyển cấu hình (CMT) Common Data Service, hãy chọn **Nhập dữ liệu** và sau đó chọn **Tiếp tục**.

    ![Di chuyển cấu hình.](./media/1ConfigurationMigration.png)

4. Trên Trang 2 của Trình hướng dẫn CMT, hãy chọn **Microsoft 365** làm **Loại triển khai**.
5. Chọn **Hiển thị danh sách tổ chức khả dụng** và hộp kiểm **Hiển thị nâng cao**.
6. Chọn khu vực của đối tượng thuê của bạn, nhập thông tin xác thực của bạn, sau đó chọn **Đăng nhập**.

   ![Đăng nhập cấu hình.](./media/2ConfigurationSignin.png)

7. Trên trang 3, từ danh sách Tổ chức trên Đối tượng thuê, hãy chọn tổ chức bạn muốn nhập dữ liệu demo vào rồi chọn **Đăng nhập**.
8. Trên trang 4, hãy chọn tệp zip *SampleSetupAndConfigData* ở thư mục được giải nén *ProjOpsSampleSetupData - CE only CMT*.

   ![Tệp Zip.](./media/3ZipFile.png)

   ![Chọn một tệp.](./media/4SelectAFile.png)

9. Sau khi chọn tệp zip, hãy chọn **Nhập dữ liệu**.

   ![Nhập dữ liệu.](./media/5ImportData.png)

10. Quá trình nhập sẽ chạy trong khoảng hai mười phút tùy thuộc vào tốc độ mạng của bạn. Sau khi hoàn tất, hãy thoát khỏi CMT Wizard. 
11. Kiểm tra tổ chức của bạn để tìm dữ liệu trong 18 thực thể sau:

    -   Tiền tệ
    -   Tài khoản
    -   Đơn vị tổ chức
    -   Liên hệ
    -   Đơn vị
    -   Nhóm đơn vị
    -   Bảng giá
    -   Bảng giá Tham số Dự án 
    -   Tuần suất hóa đơn
    -   Thể loại Nguồn lực có thể đăng ký trước
    -   Thể loại giao dịch
    -   Thể loại Chi phí
    -   Giá Vai trò
    -   Giá cả Thể loại Giao dịch
    -   Đặc tính
    -   Nguồn lực có thể đăng ký
    -   LK thể loại nguồn lực có thể đăng ký trước
    -   Đặc điểm Nguồn lực có thể đặt trước

    ![Hoàn thành quá trình nhập.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
