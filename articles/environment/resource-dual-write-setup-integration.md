---
title: Tích hợp dữ liệu cấu hình và thiết lập Project Operations
description: Chủ đề này cung cấp thông tin về thiết lập và đặt cấu hình bản đồ ghi kép của Project Operations.
author: sigitac
manager: Annbe
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d5fe81dca30039f99d5d7b9bb459214e540db945
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939066"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Tích hợp dữ liệu cấu hình và thiết lập Project Operations

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này cung cấp thông tin về tích hợp ghi kép Project Operations để cho thực thể thiết lập và cấu hình.

## <a name="project-contracts-contract-lines-and-projects"></a>Hợp đồng dự án, mô tả hợp đồng và dự án

Các hợp đồng dự án, mô tả hợp đồng và các dự án được tạo trong Dataverse và đồng bộ hóa với ứng dụng Finance and Operations cho kế toán bổ sung. Bản ghi trong các thực thể này chỉ có thể được tạo và xóa trong Dataverse. Tuy nhiên, các thuộc tính kế toán như giá trị mặc định của nhóm thuế bán hàng và kích thước tài chính có thể được thêm vào các bản ghi này trong ứng dụng Finance and Operations.

  ![Khái niệm về tích hợp hợp đồng dự án](./media/1ProjectContract.jpg)

Khách hàng tiềm năng, cơ hội và báo giá của hoạt động bán hàng được theo dõi trong Dataverse và không đồng bộ hóa với ứng dụng Finance and Operations vì không có kế toán xuôi tuyến được liên kết với hoạt động này.

Chức năng hợp đồng dự án trong Dataverse tạo một bản ghi hợp đồng dự án trong ứng dụng Finance and Operations bằng bản đồ bảng **Tiêu đề hợp đồng dự án (salesorders)**. Lưu hợp đồng dự án trong Dataverse cũng bắt đầu tạo bản ghi thực thể khách hàng hợp đồng dự án. Bản ghi này được đồng bộ hóa với ứng dụng Finance and Operations bằng bản đồ bảng **Nguồn tài trợ dự án (msdyn\_projectcontractssplitbillingrules)**. Bản đồ này cũng đồng bộ hóa các hoạt động bổ sung, cập nhật và xóa của khách hàng trong hợp đồng dự án. Tỷ lệ thanh toán phân chia giữa các khách hàng hợp đồng dự án chỉ được quản lý trong Dataverse và không được đồng bộ hóa với ứng dụng Finance and Operations.

Sau khi hợp đồng dự án được tạo trong Dataverse, kế toán viên của dự án có thể cập nhật các thuộc tính kế toán cho hợp đồng dự án này trong ứng dụng Finance and Operations bằng cách chuyển đến **Quản lý dự án và kế toán** > **Hợp đồng dự án** > **Thiết lập** > **Hiển thị kế toán mặc định**. Kế toán viên có thể đánh giá các thuộc tính hợp đồng của dự án hoạt động, chẳng hạn như ngày giao hàng được yêu cầu và số tiền hợp đồng bằng cách chọn ID hợp đồng dự án trong ứng dụng Finance and Operations giúp mở hồ sơ hợp đồng dự án liên quan trong Dataverse.

Thực thể dự án được đồng bộ hóa với ứng dụng Finance and Operations bằng bản đồ bảng **Dự án V2 (msdyn\_projects)**. Kế toán viên của dự án có thể:

  - Đánh giá các dự án trong ứng dụng Finance and Operations bằng cách chuyển đến **Quản lý dự án và kế toán** > **Tất cả các dự án**. 
  - Cập nhật các thuộc tính kế toán cho dự án trong ứng dụng Finance and Operations bằng cách chuyển đến **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Thiết lập** > **Hiển thị kế toán mặc định**.  
  - Đánh giá các thuộc tính của dự án hoạt động, chẳng hạn như ngày bắt đầu và ngày kết thúc ước tính, bằng cách chọn ID dự án trong ứng dụng Finance and Operations giúp mở bản ghi dự án liên quan trong Dataverse.

Một dự án được liên kết với hợp đồng dự án thông qua thực thể **Mô tả hợp đồng dự án**.

Mô tả hợp đồng dự án trong Dataverse tạo quy tắc thanh toán hợp đồng dự án trong ứng dụng Finance and Operations bằng bản đồ bảng **Mô tả hợp đồng dự án (salesorderdetails)**. Phương thức thanh toán xác định loại quy tắc thanh toán hợp đồng dự án trong ứng dụng Finance and Operations:

  - Mô tả hợp đồng dự án có phương thức thanh toán theo thời gian và vật tư tạo ra quy tắc thanh toán về thời gian và loại vật tư.
  - Mô tả hợp đồng có phương thức thanh toán giá cố định tạo ra một quy tắc thanh toán quan trọng.

Kế toán viên của dự án có thể đánh giá mô tả hợp đồng dự án trong ứng dụng Finance and Operations bằng cách chuyển đến **Quản lý dự án và kế toán** > **Hợp đồng dự án** > **Thiết lập** > **Hiển thị kế toán mặc định** và xem xét các chi tiết trên tab **Mô tả hợp đồng**. Kế toán viên cũng có thể đặt các kích thước tài chính mặc định cho các mô tả hợp đồng theo phương pháp thanh toán giá cố định trên tab này.

## <a name="billing-milestones"></a>Mốc thanh toán

Mô tả hợp đồng dự án sử dụng phương pháp thanh toán giá cố định được lập hóa đơn thông qua các mốc thanh toán. Các mốc thanh toán được đồng bộ hóa để dự báo các giao dịch trên tài khoản trong ứng dụng Finance and Operations bằng cách sử dụng bản đồ bảng **Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Tích hợp mốc thanh toán](./media/2Milestones.jpg)

Kế toán viên có thể đánh giá các giao dịch trên tài khoản và điều chỉnh các thuộc tính kế toán cho các giao dịch đó bằng cách chuyển đến **Quản lý dự án và kế toán** > **Hợp đồng dự án** > **Duy trì** > **Giao dịch trên tài khoản** hoặc **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Duy trì** > **Giao dịch trên tài khoản**.

Trong lần đầu tiên tạo mốc thanh toán cho mô tả hợp đồng dự án nhất định, hệ thống sẽ tự động tạo một dự án ước tính doanh thu theo giá cố định cho dự án được liên kết với mô tả hợp đồng này. Các dự án ước tính doanh thu theo giá cố định có thể được xem xét bằng cách chuyển đến **Quản lý dự án và kế toán** > **Dự án ước tính doanh thu theo giá cố định**.

### <a name="project-tasks"></a>Nhiệm vụ dự án

Các nhiệm vụ dự án được đồng bộ hóa với ứng dụng Finance and Operations thông qua bản đồ bảng **Nhiệm vụ dự án (msdyn\_projecttasks)** chỉ dùng cho mục đích tham khảo. Các thao tác tạo, cập nhật và xóa không được hỗ trợ thông qua ứng dụng Finance and Operations.

  ![Tích hợp nhiệm vụ dự án](./media/3Tasks.jpg)

## <a name="project-resources"></a>Nguồn lực dự án

Các thực thể **Vai trò nguồn lực dự án** được đồng bộ hóa với ứng dụng Finance and Operations bằng bản đồ bảng **Vai trò nguồn lực dự án cho tất cả các công ty (bookableresourcecategories)** chỉ dùng cho mục đích tham khảo. Do vai trò tài nguyên trong Dataverse không dành riêng cho công ty, hệ thống sẽ tự động tạo các bản ghi vai trò nguồn lực cụ thể của công ty tương ứng trong ứng dụng Finance and Operations cho tất cả các pháp nhân được bao gồm trong phạm vi tích hợp ghi kép.

![Tích hợp vai trò nguồn lực](./media/5Resources.jpg)

Nguồn lực dự án trong Project Operations được duy trì trong Dataverse và không được đồng bộ hóa với ứng dụng Finance and Operations.

### <a name="transaction-categories"></a>Danh mục giao dịch

Các danh mục giao dịch được duy trì trong Dataverse và được đồng bộ hóa với ứng dụng Finance and Operations bằng bản đồ bảng **Danh mục giao dịch dự án (msdyn\_transactioncategories)**. Sau khi bản ghi danh mục giao dịch được đồng bộ hóa, hệ thống sẽ tự động tạo bốn bản ghi danh mục được chia sẻ. Mỗi bản ghi tương ứng với một loại giao dịch trong ứng dụng Finance and Operations và liên kết chúng với bản ghi danh mục giao dịch.

![Tích hợp danh mục giao dịch](./media/4TransactionCategories.jpg)

Việc sử dụng các danh mục giao dịch cho các giá trị ước tính và thực tế yêu cầu kế toán viên của dự án hoặc quản trị viên hệ thống phải tạo các danh mục dự án tương ứng trong mọi pháp nhân. Để biết thêm thông tin, hãy xem [Đặt cấu hình danh mục dự án](../project-accounting/configure-project-categories.md).
