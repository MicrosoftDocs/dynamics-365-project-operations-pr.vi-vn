---
title: Ước tính dự án và tích hợp thực tế
description: Chủ đề này cung cấp thông tin về tích hợp ghi kép Project Operations cho các giá trị ước tính và thực tế dự án.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006317"
---
# <a name="project-estimates-and-actuals-integration"></a>Ước tính dự án và tích hợp thực tế

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này cung cấp thông tin về tích hợp ghi kép Project Operations cho các giá trị ước tính và thực tế dự án.

## <a name="project-estimates"></a>Ước tính dự án

Các giá trị ước tính về lao động, chi phí và vật tư của dự án được tạo và duy trì trong Microsoft Dataverse, đồng thời được đồng bộ hóa với ứng dụng Finance and Operations cho mục đích kế toán. Các thao tác tạo, cập nhật và xóa không được hỗ trợ thông qua ứng dụng Finance and Operations.

Tạo giá trị ước tính yêu cầu cấu hình kế toán hợp lệ cho dự án. Các dự án được liên kết với các mô tả hợp đồng phải có hồ sơ doanh thu và chi phí dự án hợp lệ được xác định trong các quy tắc về chi phí và hồ sơ doanh thu của Dự án. Để biết thêm thông tin, hãy xem [Đặt cấu hình hoạt động kế toán cho các dự án có thể tính phí](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Ước tính lao động

Ước tính lao động được tạo bởi Người quản lý dự án hoặc Người quản lý nguồn lực, cũng là người chỉ định một nguồn lực chung hoặc được đặt tên cho nhiệm vụ dự án. Có thể đánh giá hồ sơ chỉ định nguồn lực trên tab **Chỉ định nguồn lực** trên trang **Chi tiết dự án** trong Dataverse. Hồ sơ chỉ định nguồn lực trong Dataverse tạo bản ghi dự báo giờ trong ứng dụng Finance and Operations bằng **Thực thể tích hợp Project Operations cho ước tính giờ (msdyn\_resourceassignments)**.

   ![Tích hợp ước tính lao động.](./Media/DW4LaborEstimates.png)

Tính năng ghi kép đồng bộ hóa các hồ sơ chỉ định nguồn lực vào bảng tách chuyển (**ProjCDSEstimHoursImport**) rồi sử dụng logic nghiệp vụ để tạo và cập nhật các bản ghi dự báo giờ (**ProjForecastEmpl**).

Kế toán viên của dự án đánh giá các bản ghi giờ dự báo được tạo trong ứng dụng Finance and Operations bằng cách chuyển đến **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Kế hoạch** > **Dự báo giờ**.

## <a name="expense-estimates"></a>Ước tính chi phí

Ước tính chi phí được tạo ra bởi Người quản lý dự án trên tab **Ước tính chi phí** trên trang **Chi tiết dự án** trong Dataverse. Hồ sơ ước tính chi phí được lưu trữ trong thực thể **Mô tả ước tính** trong Dataverse. Các bản ghi ước tính này có lớp giao dịch, **Chi phí** và được đồng bộ hóa với hồ sơ dự báo chi phí trong ứng dụng Finance and Operations bằng **Thực thể tích hợp Project Operations để ước tính chi phí (msdyn\_estimatelines)**.

   ![Tích hợp ước tính chi phí.](./Media/DW4ExpenseEstimates.png)

Tính năng ghi kép đồng bộ hóa các bản ghi ước tính chi phí vào bảng tách chuyển, **(ProjCDSEstimateExpenseImport)** rồi sử dụng logic nghiệp vụ để tạo và cập nhật các bản ghi dự báo giờ (**ProjForecastCost**). Mô tả ước tính lưu trữ hồ sơ ước tính bán hàng và ước tính chi phí riêng biệt. Logic kinh doanh trong ứng dụng Finance and Operations điền một bản ghi dự báo Chi phí duy nhất bằng cách sử dụng chi tiết này trong bảng tách chuyển.

Kế toán viên của dự án có thể đánh giá các bản ghi dự báo chi phí trong ứng dụng Finance and Operations bằng cách chuyển đến **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Kế hoạch** > **Dự báo chi phí**.

## <a name="material-estimates"></a>Ước tính vật tư

Ước tính vật tư được tạo ra bởi Người quản lý dự án trên tab **Ước tính vật tư** trên trang **Chi tiết dự án** trong Dataverse. Hồ sơ ước tính vật tư được lưu trữ trong thực thể **Mô tả ước tính** trong Dataverse. Các bản ghi ước tính này có lớp giao dịch, **Vật tư** và được đồng bộ hóa với hồ sơ dự báo sản phẩm trong ứng dụng Finance and Operations bằng **Bảng tích hợp Project Operations để ước tính vật tư (msdyn\_estimatelines)**.

   ![Tích hợp ước tính vật tư.](./Media/DW4MaterialEstimates.png)

Tính năng ghi kép đồng bộ hóa các bản ghi ước tính vật tư vào bảng tách chuyển **ProjForecastSalesImpor** rồi sử dụng logic nghiệp vụ để tạo và cập nhật các bản ghi dự báo sản phẩm (**ForecastSales**). Mô tả ước tính lưu trữ hồ sơ ước tính bán hàng và ước tính chi phí riêng biệt. Logic kinh doanh trong ứng dụng Finance and Operations điền một bản ghi dự báo Sản phẩm duy nhất bằng cách sử dụng chi tiết này trong bảng tách chuyển.

Kế toán viên của dự án có thể đánh giá các bản ghi dự báo sản phẩm trong ứng dụng Finance and Operations bằng cách chuyển đến **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Kế hoạch** > **Dự báo sản phẩm**.

## <a name="project-actuals"></a>Giá trị thực tế của dự án

Giá trị thực tế của dự án được tạo trong Dataverse, dựa trên thời gian, chi phí, vật tư và hoạt động thanh toán. Tất cả các thuộc tính hoạt động của những giao dịch này bao gồm số lượng, giá vốn, giá bán và dự án được ghi lại trong thực thể Dataverse. Để biết thêm thông tin, hãy xem [Giá trị thực tế](../actuals/actuals-overview.md). Hồ sơ giá trị thực tế được đồng bộ hóa với ứng dụng Finance and Operations bằng bản đồ bảng ghi kép **Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals)** để hạch toán xuôi tuyến.

   ![Tích hợp giá trị thực tế.](./Media/DW4Actuals.png)

Sơ đồ bảng **Giá trị tích hợp thực tế của Project Operations** đồng bộ hóa tất cả các bản ghi từ thực thể **Giá trị thực tế** trong Dataverse, với thuộc tính **Bỏ qua đồng bộ hóa (chỉ sử dụng nội bộ)** đặt thành **Sai**. Giá trị thuộc tính này được đặt tự động trong Dataverse khi bản ghi được tạo. Ví dụ trong đó thuộc tính này được đặt thành **Đúng**:

  - Thực tế chi phí của dự án cho các giao dịch liên công ty. Để biết thêm thông tin, hãy xem [Tạo giao dịch liên công ty](../project-accounting/create-intercompany-transactions.md). Các bản ghi này bị bỏ qua vì hệ thống tạo lại chi phí thực tế của dự án trong ứng dụng Finance and Operations khi hóa đơn của nhà cung cấp liên công ty được đăng.
  - Bản ghi bán hàng chưa lập hóa đơn âm được tạo khi hóa đơn ước giá được xác nhận. Các bản ghi này bị bỏ qua vì sổ cái của dự án trong ứng dụng Finance and Operations không đảo ngược hồ sơ bán hàng chưa lập hóa đơn khi lập hóa đơn nhưng thay đổi trạng thái thành đã lập hóa đơn đầy đủ.

Bản đồ bảng ghi kép đồng bộ hóa các bản ghi thực tế với bảng tách chuyển, **ProjCDSActualsImport**. Các bản ghi này được xử lý theo quy trình định kỳ **Nhập từ bảng tách chuyển** khi tạo dòng nhật ký kế toán tích hợp Project Operations và mô tả đề xuất hóa đơn dự án. Để biết thêm thông tin, hãy xem [Nhật ký tích hợp trong Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse cũng nắm bắt các liên kết giữa các giao dịch thực tế của dự án trong thực thể **Kết nối giao dịch**. Để biết thêm thông tin, hãy xem [Liên kết giá trị thực tế với bản ghi gốc](../actuals/linkingactuals.md). Liên kết giữa các giao dịch thực tế cũng được đồng bộ hóa với ứng dụng Finance and Operations bằng bản đồ bảng ghi kép, **Thực thể tích hợp cho các mối quan hệ giao dịch dự án (msdyn\_transactionconnections)**. Các bản ghi này được sử dụng cho quy trình định kỳ, **Nhập từ bảng tách chuyển** khi tạo dòng nhật ký kế toán tích hợp Project Operations và mô tả đề xuất hóa đơn Dự án.

Đăng nhật ký tích hợp Project Operations và đề xuất hóa đơn dự án sẽ kích hoạt cập nhật trong các bản ghi tương ứng của bảng tách chuyển, **ProjCDSActualsImport**. Hệ thống nắm bắt và ghi lại các thuộc tính kế toán sau cho các giao dịch thực tế:

- Khoản tiền tệ kế toán
- Tỷ giá
- Số phiếu
- Số tiền thuế bán hàng

Bản đồ bảng **Giá trị tích hợp thực tế của Project Operations** cập nhật hồ sơ thực tế tương ứng trong Dataverse với thông tin này.
