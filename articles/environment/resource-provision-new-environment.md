---
title: Cung cấp môi trường mới
description: Chủ đề này cung cấp thông tin về cách cung cấp môi trường Project Operations mới.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086995"
---
# <a name="provision-a-new-environment"></a>Cung cấp môi trường mới

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này cung cấp thông tin về cách cung cấp môi trường Dynamics 365 Project Operations mới cho kịch bản dựa trên nguồn lực/hàng không nhập kho.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Bật quy trình tự động cung cấp Project Operations trong dự án LCS

Sử dụng các bước sau để bật quy trình tự động cung cấp Project Operations cho dự án LCS của bạn.

1. Chuyển đến [LCS](https://lcs.dynamics.com/v2) và chọn ngăn xếp **Quản lý tính năng xem trước**.
2. Trong danh sách **Tính năng xem trước** , hãy chọn **Tính năng Project Operations** , sau đó chọn **Đã bật tính năng xem trước** để kích hoạt Project Operations.

> [!NOTE]
> Bước này chỉ được thực hiện một lần cho mỗi dự án LCS.

## <a name="provision-a-project-operations-environment"></a>Cung cấp môi trường Project Operations

1. Mở Dynamics 365 Finance mới [môi trường demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) hoặc triển khai [môi trường sản xuất/hộp cát](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Tìm hiểu trình hướng dẫn **Cung cấp môi trường**. 

> [!IMPORTANT]
> Đảm bảo phiên bản ứng dụng đã chọn là 10.0.13 trở lên.

3. Để cung cấp Project Operations, trong phần **Cài đặt nâng cao** , hãy chọn **Common Data Service**. 
4. Bật **Thiết đặt Common Data Service** bằng việc chọn **Có** và sau đó nhập thông tin vào các trường bắt buộc:

  - Tên
  - Khu vực
  - Ngôn ngữ
  - Tiền tệ
 
5. Trong trường **Mẫu Common Data Service** , hãy chọn **Project Operations** 

6. Chọn loại môi trường để triển khai. Bản dùng thử dựa trên đăng ký sẽ cho phép bạn triển khai môi trường CDS trong 30 ngày. 

![Cài đặt triển khai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Chọn **Đồng ý** để xác nhận các điều khoản dịch vụ và sau đó chọn **Xong** để quay lại cài đặt triển khai.

![Đồng ý triển khai](./media/2DeploymentConsent.png)

7. Hoàn thành các trường bắt buộc còn lại trong trình hướng dẫn và xác nhận việc triển khai. Thời gian cung cấp môi trường thay đổi tùy theo loại môi trường. Việc cung cấp có thể mất đến sáu giờ.

  Sau khi quá trình triển khai hoàn tất thành công, môi trường sẽ hiển thị là **Đã triển khai**.

8. Để xác nhận môi trường đã được triển khai thành công, hãy chọn **Đăng nhập** và đăng nhập vào môi trường để xác nhận.

![Chi tiết môi trường](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Áp dụng dữ liệu demo Project Operations Finance (bước tùy chọn)

Áp dụng dữ liệu demo Project Operations Finance cho bản phát hành dịch vụ 10.0.13 Môi trường lưu trữ trên đám mây như được mô tả trong [bài viết này](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Áp dụng nội dung cập nhật cho môi trường Finance

Project Operations yêu cầu môi trường Finance có phiên bản ứng dụng **10.0.13 (10.0.569.20009)** trở lên.

Bạn có thể cần áp dụng các bản cập nhật chất lượng cho môi trường Finance của mình để nhận được phiên bản này.

1. Trong LCS, trên trang **Chi tiết môi trường** , trong phần **Bản cập nhật có sẵn** , hãy chọn **Xem bản cập nhật**.

![Xem bản cập nhập](./media/5ViewUpdates.png)

2. Trên trang **Bản cập nhật nhị phân** , hãy chọn **Lưu gói.**

![Lưu gói](./media/6SavePackage.png)

3. Nhấp vào **Chọn tất cả** rồi chọn **Lưu gói**.

![Xem lại và lưu bản cập nhật](./media/7ReviewAndSaveUpdates.png)

4. Nhập tên và mô tả của gói, sau đó chọn **Lưu**. Tùy thuộc vào kết nối Internet, quá trình này có thể mất một chút thời gian.

![Tải gói lên Thư viện tài sản](./media/8UploadPackageToAssetsLibrary.png)

5. Sau khi gói được lưu, hãy chọn **Xong** và lưu gói này vào Thư viện tài sản trong dự án LCS của bạn.

Việc lưu và xác nhận gói có thể mất khoảng 15 phút.

6. Để áp dụng bản cập nhật, hãy điều hướng đến trang **Môi trường chi tiết** trong LCS và chọn **Duy trì** > **Áp dụng bản cập nhật**.

![Duy trì môi trường](./media/9MaintainEnvironment.png)

7. Trong danh sách bản cập nhật, hãy chọn gói bạn đã tạo và chọn **Áp dụng**.

![Áp dụng bản cập nhật](./media/10ApplyUpdates.png)

Việc cung cấp dịch vụ môi trường sẽ mất một thời gian. Sau khi hoàn tất, môi trường sẽ trở lại trạng thái đã triển khai.

![Đã triển khai môi trường](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Thiết lập kết nối Ghi kép 

1. Trong dự án LCS của bạn, hãy chuyển đến trang **Chi tiết môi trường**.
2. Trong phần **Thông tin môi trường Common Data Service** , hãy chọn **Liên kết tới CDS for Apps**.
3. Sau khi liên kết hoàn tất, hãy chọn **Liên kết tới CDS for Apps** lần nữa. Bạn sẽ được chuyển hướng đến Ghi kép trong Finance.

![Liên kết tới CDS](./media/12LinktoCDS.png)

4. Chọn **Áp dụng giải pháp** để truy cập vào các thực thể sẽ được ánh xạ trong tích hợp.

![Áp dụng giải pháp](./media/13ApplySolutions.png)

5. Chọn cả hai giải pháp, **Bản đồ thực thể ghi kép của Dynamics 365 Finance and Operations** và **Bản đồ thực thể ghi kép của Dynamics 365 Project Operations** , và sau đó chọn **Áp dụng**.

![Xác nhận giải pháp](./media/14ConfirmSolutions.png)

Sau khi các giải pháp được áp dụng, các thực thể Ghi kép được áp dụng cho môi trường.

![Đang áp dụng giải pháp](./media/15ApplyingSolutions.png)

Sau khi các thực thể được áp dụng, tất cả các ánh xạ có sẵn sẽ được liệt kê trong môi trường.

![Bản đồ ghi kép](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Làm mới các thực thể dữ liệu sau khi cập nhật

1. Trong Finance, hãy chuyển đến không gian làm việc **Quản lý dữ liệu**.

![Không gian làm việc quản lý dữ liệu](./media/16DataManagement.png)

2. Chọn ngăn xếp **Tham số khung**.

![Tham số khung](./media/17FrameworkParameters.png)

3. Trên trang **Cài đặt thực thể** , hãy chọn **Làm mới danh sách thực thể**.

![Làm mới danh sách thực thể](./media/18RefreshEntityList.png)

Quá trình làm mới sẽ mất khoảng 20 phút. Bạn sẽ nhận được một cảnh báo khi quá trình hoàn tất.

![Xác nhận làm mới](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Chạy bản đồ ghi kép Project Operations

1. Trong dự án LCS của bạn, hãy chuyển đến trang **Chi tiết môi trường**.
2. Trong phần **Thông tin môi trường Common Data Service** , hãy chọn **Liên kết tới CDS for Apps.** Sau khi bạn chọn liên kết, bạn sẽ được chuyển hướng đến danh sách các thực thể trong ánh xạ.
3. Bắt đầu bản đồ như mô tả trong bảng sau. Đảm bảo làm theo trình tự như đã liệt kê.

| **Sơ đồ thực thể** | **Làm mới thực thể** | **Đồng bộ ban đầu** | **Bản cái cho đồng bộ hóa ban đầu** | **Chạy điều kiện tiên quyết** | **Đồng bộ hóa ban đầu điều kiện tiên quyết** |
| --- | --- | --- | --- | --- | --- |
| **Vai trò nguồn lực dự án cho tất cả các công ty (các thể loại nguồn lực có thể đăng ký trước)** | No | Có | Common Data Service | No | Không áp dụng |
| **Thực thể pháp lý (cdm\_companies)** | No | Có | Ứng dụng Finance and Operations | No | Không áp dụng |
| **Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals)** | No | No | Không áp dụng | Có | No |
| **Mô tả hợp đồng dự án (salesorderdetails)** | No | No | Không áp dụng | No | No |
| **Thực thể tích hợp cho các mối quan hệ giao dịch dự án (msdyn\_transactionconnections)** | No | No | Không áp dụng | No | Không áp dụng |
| **Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | Không áp dụng | No | Không áp dụng |
| **Thực thể tích hợp Project Operations để ước tính chi phí (msdyn\_estimateslines)** | No | No | Không áp dụng | No | Không áp dụng |
| **Thực thể xuất danh mục chi phí dự án tích hợp Project Operations (msdyn\_expensecategories)** | No | No | Không áp dụng | No | Không áp dụng |
| **Thực thể xuất chi phí dự án tích hợp Project Operations (msdyn\_expenses)** | Có | No | Không áp dụng | No | Không áp dụng |
| **Thực thể tích hợp Project Operations để ước tính giờ (msdyn\_resourceassignments)** | Có | No | Không áp dụng | No | Không áp dụng |


4. Để làm mới thực thể, hãy chọn tên bản đồ, sau đó chọn **Làm mới thực thể**. 


![Làm mới bản đồ](./media/20RefreshMapping.png)

5. Sau khi quá trình làm mới hoàn tất, hãy chạy bản đồ. Trước khi bạn bật bản đồ tiếp theo, hãy xác minh rằng bản đồ trong bảng ở trạng thái **Đang chạy**. Việc chạy bản đồ với số lượng điều kiện tiên quyết lớn hơn có thể mất một chút thời gian.

Để chạy bản đồ với các điều kiện tiên quyết, hãy bật tùy chọn chuyển đổi **Hiển thị bản đồ thực thể liên quan**. Nếu bảng cho biết **Đồng bộ hóa ban đầu điều kiện tiên quyết** là **Không** , hãy xác minh rằng cờ **Đồng bộ ban đầu** đang **Tắt** trong tất cả các bản đồ tiên quyết trước khi bạn chạy.

![Chạy bản đồ](./media/21RunMap.png)

6. Xác thực tất cả các bản đồ liên quan đến dự án đang ở trạng thái đang chạy.

![Tất cả các bản đồ đang chạy](./media/22AllMapsRunning.png)

Môi trường Project Operations của bạn hiện đã được cung cấp và đặt cấu hình.
