---
title: Cung cấp môi trường mới
description: Chủ đề này cung cấp thông tin về cách cung cấp môi trường Project Operations mới.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a00426678d23000dc19386792d346318eab74ed9
ms.sourcegitcommit: d3f66dfb5978c5c6b7fd51363c7f9278737c49c1
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/17/2021
ms.locfileid: "7928687"
---
# <a name="provision-a-new-environment"></a>Cung cấp môi trường mới

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Chủ đề này cung cấp thông tin về cách cung cấp môi trường Dynamics 365 Project Operations cho các tình huống dựa trên nguồn lực/hàng không trữ kho.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Bật quy trình tự động cung cấp Project Operations trong dự án LCS

Sử dụng các bước sau để bật quy trình tự động cung cấp Project Operations cho dự án LCS của bạn.

1. Chuyển đến [LCS](https://lcs.dynamics.com/v2) và chọn ngăn xếp **Quản lý tính năng xem trước**.
2. Trong danh sách **Tính năng xem trước**, hãy chọn **Tính năng Project Operations**, sau đó chọn **Đã bật tính năng xem trước** để kích hoạt Project Operations.

   > [!NOTE]
   > Bước này chỉ được thực hiện một lần cho mỗi dự án LCS.

## <a name="provision-a-project-operations-environment"></a>Cung cấp môi trường Project Operations

1. Mở Dynamics 365 Finance mới [môi trường demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) hoặc triển khai [môi trường sản xuất/hộp cát](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Tìm hiểu trình hướng dẫn **Cung cấp môi trường**. 

   > [!IMPORTANT]
   > Đảm bảo phiên bản ứng dụng đã chọn là 10.0.13 trở lên.

3. Để cung cấp Project Operations, trong phần **Cài đặt nâng cao**, hãy chọn **Common Data Service**. 
4. Bật **Thiết đặt Common Data Service** bằng việc chọn **Có** và sau đó nhập thông tin vào các trường bắt buộc:

  - Tên
  - Khu vực
  - Ngôn ngữ
  - Tiền tệ
 
5. Trong trường **Mẫu Common Data Service**, hãy chọn **Project Operations** 
6. Chọn loại môi trường để triển khai. Bản dùng thử dựa trên đăng ký sẽ cho phép bạn triển khai môi trường CDS trong 30 ngày. 

     ![Cài đặt triển khai.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Chọn **Đồng ý** để xác nhận các điều khoản dịch vụ và sau đó chọn **Xong** để quay lại cài đặt triển khai.
    >
    >![Đồng ý triển khai.](./media/2DeploymentConsent.png)

7. Không bắt buộc - Áp dụng dữ liệu demo cho môi trường. Đi đến **Cài đặt nâng cao**, chọn **Tuy chỉnh cấu hình Cơ sở dữ liệu SQL** rồi đặt tùy chọn **Xác định tập dữ liệu cho cơ sở dữ liệu ứng dụng** thành **Demo**.
8. Hoàn thành các trường bắt buộc còn lại trong trình hướng dẫn và xác nhận việc triển khai. Thời gian cung cấp môi trường sẽ khác nhau tùy theo loại môi trường. Việc cung cấp có thể mất đến sáu giờ.

   Sau khi quá trình triển khai hoàn tất thành công, môi trường sẽ hiển thị là **Đã triển khai**.

9. Để chắc chắn rằng môi trường đã được triển khai thành công, hãy chọn **Đăng nhập** rồi đăng nhập vào môi trường cần xác nhận.

    ![Chi tiết môi trường.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Áp dụng nội dung cập nhật cho môi trường Finance

Project Operations yêu cầu môi trường Finance có phiên bản ứng dụng **10.0.13 (10.0.569.20009)** trở lên.

Bạn có thể cần áp dụng các bản cập nhật chất lượng cho môi trường Finance của mình để nhận được phiên bản này.

1. Trong LCS, trên trang **Chi tiết môi trường**, trong phần **Bản cập nhật có sẵn**, hãy chọn **Xem bản cập nhật**.

    ![Xem bản cập nhập.](./media/5ViewUpdates.png)

2. Trên trang **Bản cập nhật nhị phân**, hãy chọn **Lưu gói.**

    ![Lưu gói.](./media/6SavePackage.png)

3. Nhấp vào **Chọn tất cả** rồi chọn **Lưu gói**.

    ![Xem lại và lưu bản cập nhật.](./media/7ReviewAndSaveUpdates.png)

4. Nhập tên và mô tả của gói, sau đó chọn **Lưu**. Tùy thuộc vào kết nối Internet, quá trình này có thể mất một chút thời gian.

    ![Tải gói lên Thư viện tài sản.](./media/8UploadPackageToAssetsLibrary.png)

5. Sau khi gói được lưu, hãy chọn **Xong** và lưu gói này vào Thư viện tài sản trong dự án LCS của bạn.

   Việc lưu và xác nhận gói có thể mất khoảng 15 phút.

6. Để áp dụng bản cập nhật, hãy điều hướng đến trang **Môi trường chi tiết** trong LCS và chọn **Duy trì** > **Áp dụng bản cập nhật**.

    ![Duy trì môi trường.](./media/9MaintainEnvironment.png)

7. Trong danh sách bản cập nhật, hãy chọn gói bạn đã tạo và chọn **Áp dụng**.

    ![Áp dụng bản cập nhật.](./media/10ApplyUpdates.png)

   Việc cung cấp dịch vụ môi trường sẽ mất một thời gian. Sau khi hoàn tất, môi trường sẽ trở lại trạng thái đã triển khai.

    ![Đã triển khai môi trường.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Thiết lập kết nối Ghi kép 

1. Trong dự án LCS của bạn, hãy chuyển đến trang **Chi tiết môi trường**.
2. Trong phần **Thông tin môi trường Common Data Service**, hãy chọn **Liên kết tới CDS for Apps**.
3. Sau khi liên kết hoàn tất, hãy chọn **Liên kết tới CDS for Apps** lần nữa. Bạn sẽ được chuyển hướng đến Ghi kép trong Finance.

    ![Liên kết tới CDS.](./media/12LinktoCDS.png)

4. Chọn **Áp dụng giải pháp** để truy cập vào các thực thể sẽ được ánh xạ trong tích hợp.

    ![Áp dụng giải pháp.](./media/13ApplySolutions.png)

5. Chọn cả 2 giải pháp là Bản đồ thực thể ghi kép **Dynamics 365 Finance and Operations** và **Bản đồ thực thể ghi kép Dynamics 365 Project Operations** rồi chọn **Áp dụng**.

    ![Xác nhận giải pháp.](./media/14ConfirmSolutions.png)

    Sau khi các giải pháp được áp dụng, các thực thể Ghi kép được áp dụng cho môi trường.

    ![Đang áp dụng giải pháp.](./media/15ApplyingSolutions.png)

    Sau khi các thực thể được áp dụng, tất cả các ánh xạ có sẵn sẽ được liệt kê trong môi trường.

    ![Bản đồ ghi kép.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Làm mới các thực thể dữ liệu sau khi cập nhật

1. Trong Finance, hãy chuyển đến không gian làm việc **Quản lý dữ liệu**.

    ![Không gian làm việc quản lý dữ liệu.](./media/16DataManagement.png)

2. Chọn ngăn xếp **Tham số khung**.

    ![Tham số khung.](./media/17FrameworkParameters.png)

3. Trên trang **Cài đặt thực thể**, hãy chọn **Làm mới danh sách thực thể**.

    ![Làm mới danh sách thực thể.](./media/18RefreshEntityList.png)

Quá trình làm mới sẽ mất khoảng 20 phút. Bạn sẽ nhận được một cảnh báo khi quá trình hoàn tất.

  ![Xác nhận làm mới.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Cập nhật các tùy chọn cài đặt bảo mật trong Project Operations trên Dataverse

1. Đi đến Project Operations trên môi trường Dataverse của bạn. 
2. Đi đến **Cài đặt** > **Bảo mật** > **Vai trò bảo mật**. 
3. Trên trang **Vai trò bảo mật**, trong danh sách vai trò, hãy chọn **người dùng ứng dụng ghi kép** rồi chọn tab **Thực thể tùy chỉnh**.  
4. Xác minh rằng vai trò có quyền **Đọc** và **Gắn thêm vào** cho các thực thể sau:
      
      - **Loại tỷ giá hối đoái**
      - **Biểu đồ tài khoản**
      - **Lịch tài khóa**
      - **Sổ cái**
      - **Công ty**
      - **Chi phí**

5. Sau khi cập nhật xong vai trò bảo mật, hãy đi đến **Cài đặt** > **Bảo mật** > **Nhóm**, rồi chọn nhóm mặc định trong chế độ xem nhóm **Chủ sở hữu doanh nghiệp địa phương**.
6. Chọn **Quản lý vai trò** và xác minh rằng quyền bảo mật **người dùng ứng dụng ghi kép** đã được áp dụng cho nhóm này.

## <a name="run-project-operations-dual-write-maps"></a>Chạy bản đồ ghi kép Project Operations

1. Trong dự án LCS của bạn, hãy chuyển đến trang **Chi tiết môi trường**.
2. Trong phần **Thông tin môi trường Common Data Service**, hãy chọn **Liên kết tới CDS for Apps.** Sau khi bạn chọn liên kết, bạn sẽ được chuyển hướng đến danh sách các thực thể trong ánh xạ.
3. Bắt đầu các bản đồ. Để biết thêm thông tin, hãy xem [Các phiên bản ánh xạ ghi kép Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Xác thực tất cả các bản đồ liên quan đến dự án đang ở trạng thái đang chạy.

    ![Tất cả các bản đồ đang chạy.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Áp dụng dữ liệu cấu hình trong CDS cho Project Operations (tùy chọn)

Nếu bạn đã áp dụng dữ liệu demo cho môi trường Tài chính, hãy xem [Thiết lập và áp dụng dữ liệu cấu hình trong Common Data Service cho Project Operations](resource-apply-pro-setup-config-data.md) để áp dụng dữ liệu demo cho môi trường CDS.


Môi trường Project Operations của bạn hiện đã được cung cấp và đặt cấu hình. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
