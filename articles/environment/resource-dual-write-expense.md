---
title: Tích hợp quản lý chi phí
description: Chủ đề này cung cấp thông tin về tích hợp báo cáo chi phí trong Project Operations bằng tính năng ghi kép.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 06471532d2e41bb80ebf92f0a8b93c324b3f6d3e845cea8033d85d291ea237eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986607"
---
# <a name="expense-management-integration"></a>Tích hợp quản lý chi phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này cung cấp thông tin về báo cáo chi phí trong Project Operations [triển khai chi phí đầy đủ](../expense/expense-overview.md) bằng tính năng ghi kép.

## <a name="expense-categories"></a>Danh mục chi phí

Khi triển khai toàn bộ chi phí, các danh mục chi phí được tạo và duy trì trong ứng dụng Finance and Operations. Để tạo danh mục chi phí mới, hãy hoàn thành các bước sau:

1. Trong Microsoft Dataverse, hãy tạo danh mục **Giao dịch**. Tích hợp ghi kép sẽ đồng bộ hóa danh mục giao dịch này với ứng dụng Finance and Operations. Để biết thêm thông tin, hãy xem [Đặt cấu hình danh mục dự án](/dynamics365/project-operations/project-accounting/configure-project-categories) và [Thiết lập Project Operations và tích hợp dữ liệu cấu hình](resource-dual-write-setup-integration.md). Do sự tích hợp này, hệ thống tạo ra bốn bản ghi danh mục được chia sẻ trong ứng dụng Finance and Operations.
2. Trong Tài chính, hãy chuyển đến **Quản lý chi phí** > **Thiết lập** > **Danh mục được chia sẻ** và chọn một danh mục được chia sẻ với lớp giao dịch **Chi phí**. Đặt thông số **Có thể được sử dụng trong Chi phí** thành **Đúng** và xác định loại chi phí sẽ sử dụng.
3. Sử dụng bản ghi danh mục được chia sẻ này, tạo một danh mục chi phí mới bằng cách chuyển đến phần **Quản lý chi phí** > **Thiết lập** > **Danh mục chi phí** rồi chọn **Mới**. Khi bản ghi được lưu, tính năng ghi kép sử dụng sơ đồ bảng, **Thực thể xuất danh mục dự án tích hợp của Project Operations (msdyn\_expensecategories)** để đồng bộ hóa bản ghi này với Dataverse.

  ![Tích hợp danh mục chi phí.](./media/DW6ExpenseCategories.png)

Các danh mục chi phí trong ứng dụng Finance and Operations dành riêng cho công ty hoặc pháp nhân. Có các bản ghi riêng biệt, tương ứng với pháp nhân cụ thể trong Dataverse. Khi người quản lý dự án ước tính chi phí, họ không thể chọn danh mục chi phí được tạo cho một dự án thuộc sở hữu của công ty khác thay cho công ty sở hữu dự án mà họ đang thực hiện. 

## <a name="expense-reports"></a>Báo cáo chi phí

Báo cáo chi phí được tạo và phê duyệt trong ứng dụng Finance and Operations. Để biết thêm thông tin, hãy xem [Tạo và xử lý các báo cáo chi phí trong Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Sau khi Người quản lý dự án phê duyệt, báo cáo chi phí sẽ được đăng lên sổ cái. Trong Project Operations, các mô tả báo cáo chi phí liên quan đến dự án được đăng bằng các quy tắc đặc biệt:

  - Chi phí liên quan đến dự án (bao gồm cả thuế không thu hồi được) không được ghi ngay vào tài khoản chi phí dự án trong sổ cái, mà thay vào đó được đăng vào tài khoản tích hợp chi phí. Tài khoản này được đặt cấu hình trong **Quản lý dự án và kế toán** > **Thiết lập** > **Quản lý dự án và thông số kế toán**, tab **Project Operations trên Dynamics 365 Customer Engagement**.
  - Tính năng ghi kép đồng bộ hóa Dataverse bằng bản đồ bảng **Thực thể xuất chi phí dự án tích hợp trong Project Operations (msdyn\_expenses)**.
  - Sổ cái thuế, sổ cái nhà cung cấp và các bài đăng tài chính khác được ghi nhận là có thể áp dụng tại thời điểm đăng báo cáo chi phí.

  ![Tích hợp báo cáo chi phí.](./media/DW6ExpenseReports.png)

Khi một bản ghi được ghi vào thực thể **Chi phí** trong Dataverse, hệ thống sẽ kích hoạt quá trình phê duyệt hồ sơ tự động. Nếu cần, bạn có thể xem lại trạng thái quy trình phê duyệt tự động trong Dataverse bằng cách chuyển đến phần **Cài đặt nâng cao** > **Hệ thống** > **Công việc hệ thống**. Sau khi phê duyệt xong, các bản ghi lớp giao dịch chi phí được tạo trong thực thể **Giá trị thực tế**.

Sau đó, các giá trị thực tế liên quan đến chi phí được xử lý bằng cách sử dụng sơ đồ bảng ghi kép **Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals)**. Để biết thêm thông tin, hãy xem [Giá trị ước tính và thực tế của dự án](resource-dual-write-estimates-actuals.md).

Quy trình định kỳ **Nhập từ tách chuyển** tạo các dòng nhật ký kế toán liên quan đến báo cáo Chi phí trong nhật ký Tích hợp Project Operations. Tài khoản bù trừ mặc định là tài khoản tích hợp chi phí. Nhật ký tích hợp Đăng xóa số dư tài khoản cho giao dịch chi phí và chuyển khoản tiền chi phí vào tài khoản chi phí dự án. Hệ thống cũng tạo ra các giao dịch sổ cái của dự án cho các mục đích lập hóa đơn và ghi nhận doanh thu xuôi tuyến.
