---
title: Áp dụng dữ liệu cấu hình và thiết lập bản demo – bản đơn giản
description: Bài viết này cung cấp thông tin về cách áp dụng dữ liệu cấu hình và thiết lập demo cho Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811052"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Áp dụng dữ liệu cấu hình và thiết lập bản demo cho Project Operations – bản đơn giản 

_**Triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá_



## <a name="prerequisites"></a>Điều kiện tiên quyết

Trước khi bắt đầu cấu hình, bạn phải cung cấp môi trường Dataverse cho Dynamics 365 Project Operations.


## <a name="instructions"></a>Hướng dẫn

1. Tải xuống [Gói dữ liệu thiết lập](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Điều hướng đến thư mục *ProjOpsSampleSetupData - CE only CMT* và chạy tệp thực thi *DataMigrationUtility*.
1. Trên trang 1 của Trình hướng dẫn di chuyển cấu hình (CMT) Common Data Service, hãy chọn **Nhập dữ liệu** và sau đó chọn **Tiếp tục**.

    ![Di chuyển cấu hình.](./media/1ConfigurationMigration.png)

1. Trên Trang 2 của Trình hướng dẫn CMT, hãy chọn **Microsoft 365** làm **Loại triển khai**.
1. Chọn **Hiển thị danh sách tổ chức khả dụng** và hộp kiểm **Hiển thị nâng cao**.
1. Chọn khu vực của đối tượng thuê của bạn, nhập thông tin xác thực của bạn, sau đó chọn **Đăng nhập**.

   ![Đăng nhập cấu hình.](./media/2ConfigurationSignin.png)

1. Trên trang 3, từ danh sách Tổ chức trên Đối tượng thuê, hãy chọn tổ chức bạn muốn nhập dữ liệu demo vào rồi chọn **Đăng nhập**.
1. Trên trang 4, hãy chọn tệp zip *SampleSetupAndConfigData* ở thư mục được giải nén *ProjOpsSampleSetupData - CE only CMT*.

   ![Tệp Zip.](./media/3ZipFile.png)

   ![Chọn một tệp.](./media/4SelectAFile.png)

1. Sau khi chọn tệp zip, hãy chọn **Nhập dữ liệu**.

   ![Nhập dữ liệu.](./media/5ImportData.png)

1. Quá trình nhập sẽ chạy trong khoảng hai mười phút tùy thuộc vào tốc độ mạng của bạn. Sau khi hoàn tất, hãy thoát khỏi CMT Wizard. 
1. Kiểm tra tổ chức của bạn để tìm dữ liệu trong 18 thực thể sau:

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
