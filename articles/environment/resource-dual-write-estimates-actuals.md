---
title: Ước tính dự án và tích hợp thực tế
description: Bài viết này cung cấp thông tin về tích hợp ghi kép Hoạt động dự án cho các ước tính và thực tế của dự án.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914612"
---
# <a name="project-estimates-and-actuals-integration"></a>Ước tính dự án và tích hợp thực tế

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này cung cấp thông tin về tích hợp ghi kép Hoạt động dự án cho các ước tính và thực tế của dự án.

## <a name="project-estimates"></a>Ước tính dự án

Các ước tính về lao động, chi phí và vật liệu của dự án được tạo và duy trì trong Microsoft Dataverse và được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động cho các mục đích kế toán. Các hoạt động tạo, cập nhật và xóa không được hỗ trợ thông qua ứng dụng Tài chính và Hoạt động.

Tạo giá trị ước tính yêu cầu cấu hình kế toán hợp lệ cho dự án. Các dự án được liên kết với các mô tả hợp đồng phải có hồ sơ doanh thu và chi phí dự án hợp lệ được xác định trong các quy tắc về chi phí và hồ sơ doanh thu của Dự án. Để biết thêm thông tin, hãy xem [Đặt cấu hình hoạt động kế toán cho các dự án có thể tính phí](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Ước tính lao động

Ước tính lao động được tạo bởi Người quản lý dự án hoặc Người quản lý nguồn lực, cũng là người chỉ định một nguồn lực chung hoặc được đặt tên cho nhiệm vụ dự án. Có thể đánh giá hồ sơ chỉ định nguồn lực trên tab **Chỉ định nguồn lực** trên trang **Chi tiết dự án** trong Dataverse. Hồ sơ phân công tài nguyên trong Dataverse tạo bản ghi dự báo giờ trong ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Thực thể tích hợp Hoạt động dự án cho ước tính giờ (msdyn\_ phân công tài nguyên)**.

   ![Tích hợp ước tính lao động.](./Media/DW4LaborEstimates.png)

Tính năng ghi kép đồng bộ hóa các hồ sơ chỉ định nguồn lực vào bảng tách chuyển (**ProjCDSEstimHoursImport**) rồi sử dụng logic nghiệp vụ để tạo và cập nhật các bản ghi dự báo giờ (**ProjForecastEmpl**).

Kế toán dự án xem xét các bản ghi giờ dự báo được tạo trong ứng dụng Tài chính và Hoạt động bằng cách truy cập **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Kế hoạch** > **Dự báo giờ**.

## <a name="expense-estimates"></a>Ước tính chi phí

Ước tính chi phí được tạo ra bởi Người quản lý dự án trên tab **Ước tính chi phí** trên trang **Chi tiết dự án** trong Dataverse. Hồ sơ ước tính chi phí được lưu trữ trong thực thể **Mô tả ước tính** trong Dataverse. Các bản ghi ước tính này có lớp giao dịch, **Chi phí** và được đồng bộ hóa với hồ sơ dự báo chi phí trong ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Thực thể tích hợp Hoạt động Dự án để ước tính chi phí (msdyn\_ đường ước tính)**.

   ![Tích hợp ước tính chi phí.](./Media/DW4ExpenseEstimates.png)

Tính năng ghi kép đồng bộ hóa các bản ghi ước tính chi phí vào bảng tách chuyển, **(ProjCDSEstimateExpenseImport)** rồi sử dụng logic nghiệp vụ để tạo và cập nhật các bản ghi dự báo giờ (**ProjForecastCost**). Mô tả ước tính lưu trữ hồ sơ ước tính bán hàng và ước tính chi phí riêng biệt. Logic kinh doanh trong ứng dụng Tài chính và Hoạt động điền vào một bản ghi dự báo Chi phí bằng cách sử dụng chi tiết này trong bảng phân tích.

Kế toán dự án có thể xem xét hồ sơ dự báo chi phí trong ứng dụng Tài chính và Hoạt động bằng cách truy cập **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Kế hoạch** > **Dự báo chi phí**.

## <a name="material-estimates"></a>Ước tính vật tư

Ước tính vật tư được tạo ra bởi Người quản lý dự án trên tab **Ước tính vật tư** trên trang **Chi tiết dự án** trong Dataverse. Hồ sơ ước tính vật tư được lưu trữ trong thực thể **Mô tả ước tính** trong Dataverse. Các bản ghi ước tính này có lớp giao dịch, **Vật chất** và được đồng bộ hóa với các bản ghi dự báo mặt hàng trong ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Bảng tích hợp dự án để ước tính vật liệu (msdyn\_ đường ước tính)**.

   ![Tích hợp ước tính vật tư.](./Media/DW4MaterialEstimates.png)

Tính năng ghi kép đồng bộ hóa các bản ghi ước tính vật tư vào bảng tách chuyển **ProjForecastSalesImpor** rồi sử dụng logic nghiệp vụ để tạo và cập nhật các bản ghi dự báo sản phẩm (**ForecastSales**). Mô tả ước tính lưu trữ hồ sơ ước tính bán hàng và ước tính chi phí riêng biệt. Logic kinh doanh trong ứng dụng Tài chính và Hoạt động điền vào một bản ghi dự báo Mặt hàng duy nhất bằng cách sử dụng chi tiết này trong bảng phân tích.

Kế toán dự án có thể xem xét các bản ghi dự báo hạng mục trong ứng dụng Tài chính và Hoạt động bằng cách truy cập **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Kế hoạch** > **Dự báo mặt hàng**.

## <a name="project-actuals"></a>Giá trị thực tế của dự án

Giá trị thực tế của dự án được tạo trong Dataverse, dựa trên thời gian, chi phí, vật tư và hoạt động thanh toán. Tất cả các thuộc tính hoạt động của những giao dịch này bao gồm số lượng, giá vốn, giá bán và dự án được ghi lại trong thực thể Dataverse. Để biết thêm thông tin, hãy xem [Giá trị thực tế](../actuals/actuals-overview.md). Các bản ghi thực tế được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động bằng cách sử dụng sơ đồ bảng ghi kép **Hướng dẫn tích hợp Hoạt động Dự án (msdyn\_ thực tế)** để hạch toán hạ nguồn.

   ![Tích hợp giá trị thực tế.](./Media/DW4Actuals.png)

Sơ đồ bảng **Giá trị tích hợp thực tế của Project Operations** đồng bộ hóa tất cả các bản ghi từ thực thể **Giá trị thực tế** trong Dataverse, với thuộc tính **Bỏ qua đồng bộ hóa (chỉ sử dụng nội bộ)** đặt thành **Sai**. Giá trị thuộc tính này được đặt tự động trong Dataverse khi bản ghi được tạo. Ví dụ trong đó thuộc tính này được đặt thành **Đúng**:

  - Thực tế chi phí của dự án cho các giao dịch liên công ty. Để biết thêm thông tin, hãy xem [Tạo giao dịch liên công ty](../project-accounting/create-intercompany-transactions.md). Các bản ghi này bị bỏ qua vì hệ thống tạo lại chi phí thực tế của dự án trong ứng dụng Tài chính và Hoạt động khi hóa đơn của nhà cung cấp liên công ty được đăng.
  - Bản ghi bán hàng chưa lập hóa đơn âm được tạo khi hóa đơn ước giá được xác nhận. Các bản ghi này bị bỏ qua vì công cụ phụ của dự án trong ứng dụng Tài chính và Hoạt động không đảo ngược hồ sơ bán hàng chưa lập hóa đơn khi lập hóa đơn mà thay đổi trạng thái thành đã lập hóa đơn đầy đủ.

Bản đồ bảng ghi kép đồng bộ hóa các bản ghi thực tế với bảng tách chuyển, **ProjCDSActualsImport**. Các bản ghi này được xử lý theo quy trình định kỳ **Nhập từ bảng tách chuyển** khi tạo dòng nhật ký kế toán tích hợp Project Operations và mô tả đề xuất hóa đơn dự án. Để biết thêm thông tin, hãy xem [Nhật ký tích hợp trong Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse cũng nắm bắt các liên kết giữa các giao dịch thực tế của dự án trong thực thể **Kết nối giao dịch**. Để biết thêm thông tin, hãy xem [Liên kết giá trị thực tế với bản ghi gốc](../actuals/linkingactuals.md). Các liên kết giữa các giao dịch thực tế cũng được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động bằng cách sử dụng sơ đồ bảng ghi kép, **Thực thể tích hợp cho các mối quan hệ giao dịch dự án (msdyn\_ giao dịch kết nối)**. Các bản ghi này được sử dụng cho quy trình định kỳ, **Nhập từ bảng tách chuyển** khi tạo dòng nhật ký kế toán tích hợp Project Operations và mô tả đề xuất hóa đơn Dự án.

Đăng nhật ký tích hợp Project Operations và đề xuất hóa đơn dự án sẽ kích hoạt cập nhật trong các bản ghi tương ứng của bảng tách chuyển, **ProjCDSActualsImport**. Hệ thống nắm bắt và ghi lại các thuộc tính kế toán sau cho các giao dịch thực tế:

- Khoản tiền tệ kế toán
- Tỷ giá
- Số phiếu
- Số tiền thuế bán hàng

Bản đồ bảng **Giá trị tích hợp thực tế của Project Operations** cập nhật hồ sơ thực tế tương ứng trong Dataverse với thông tin này.
