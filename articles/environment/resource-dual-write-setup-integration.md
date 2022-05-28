---
title: Tích hợp dữ liệu cấu hình và thiết lập Project Operations
description: Chủ đề này cung cấp thông tin về thiết lập và đặt cấu hình bản đồ ghi kép của Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586922"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Tích hợp dữ liệu cấu hình và thiết lập Project Operations

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này cung cấp thông tin về tích hợp ghi kép Project Operations để cho thực thể thiết lập và cấu hình.

## <a name="project-contracts-contract-lines-and-projects"></a>Hợp đồng dự án, mô tả hợp đồng và dự án

Các hợp đồng dự án, các dòng hợp đồng và các dự án được tạo trong Dataverse và được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động để kế toán bổ sung. Bản ghi trong các thực thể này chỉ có thể được tạo và xóa trong Dataverse. Tuy nhiên, các thuộc tính kế toán như giá trị mặc định của nhóm thuế bán hàng và thứ nguyên tài chính có thể được thêm vào các bản ghi này trong ứng dụng Tài chính và Hoạt động.

  ![Khái niệm về tích hợp hợp đồng dự án.](./media/1ProjectContract.jpg)

Khách hàng tiềm năng, cơ hội và báo giá hoạt động bán hàng được theo dõi trong Dataverse và không đồng bộ hóa với các ứng dụng Tài chính và Hoạt động vì không có kế toán hạ nguồn nào được liên kết với hoạt động này.

Chức năng hợp đồng dự án trong Dataverse tạo hồ sơ hợp đồng dự án trong ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Tiêu đề hợp đồng dự án (đơn hàng bán)** bảng sơ đồ. Lưu hợp đồng dự án trong Dataverse cũng bắt đầu tạo bản ghi thực thể khách hàng hợp đồng dự án. Hồ sơ này được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Nguồn vốn dự án (msdyn\_ projectcontractssplitbillingrules)** bảng sơ đồ. Bản đồ này cũng đồng bộ hóa các hoạt động bổ sung, cập nhật và xóa của khách hàng trong hợp đồng dự án. Tỷ lệ thanh toán phân chia giữa các khách hàng hợp đồng dự án chỉ được nắm vững trong Dataverse và không được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động.

Sau khi hợp đồng dự án được tạo trong Dataverse, kế toán dự án có thể cập nhật các thuộc tính kế toán cho hợp đồng dự án này trong ứng dụng Tài chính và Hoạt động bằng cách truy cập **Quản lý dự án và kế toán** > **Hợp đồng dự án** > **Thiết lập** > **Hiển thị kế toán mặc định**. Kế toán có thể xem xét các thuộc tính hợp đồng dự án hoạt động, chẳng hạn như ngày giao hàng được yêu cầu và số tiền hợp đồng bằng cách chọn ID hợp đồng dự án trong ứng dụng Tài chính và Hoạt động để mở hồ sơ hợp đồng dự án liên quan trong Dataverse.

Thực thể dự án được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Dự án V2 (msdyn\_ dự án)** bảng sơ đồ. Kế toán viên của dự án có thể:

  - Xem lại các dự án trong ứng dụng Tài chính và Hoạt động bằng cách đi tới **Quản lý dự án và kế toán** > **Tất cả các dự án**. 
  - Cập nhật các thuộc tính kế toán cho dự án trong ứng dụng Tài chính và Hoạt động bằng cách truy cập **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Thiết lập** > **Hiển thị kế toán mặc định**.  
  - Xem lại các thuộc tính của dự án hoạt động, chẳng hạn như ngày bắt đầu và ngày kết thúc ước tính, bằng cách chọn ID dự án trong ứng dụng Tài chính và Hoạt động để mở hồ sơ dự án liên quan trong Dataverse.

Một dự án được liên kết với hợp đồng dự án thông qua thực thể **Mô tả hợp đồng dự án**.

Các dòng hợp đồng dự án trong Dataverse tạo quy tắc thanh toán hợp đồng dự án trong ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Các dòng hợp đồng dự án (chi tiết đơn hàng)** bảng sơ đồ. Phương thức thanh toán xác định loại quy tắc thanh toán hợp đồng dự án trong ứng dụng Tài chính và Hoạt động:

  - Mô tả hợp đồng dự án có phương thức thanh toán theo thời gian và vật tư tạo ra quy tắc thanh toán về thời gian và loại vật tư.
  - Mô tả hợp đồng có phương thức thanh toán giá cố định tạo ra một quy tắc thanh toán quan trọng.

Kế toán dự án có thể xem xét các dòng hợp đồng dự án trong ứng dụng Tài chính và Hoạt động bằng cách truy cập **Quản lý dự án và kế toán** > **Hợp đồng dự án** > **Thiết lập** > **Hiển thị kế toán mặc định** và xem xét các chi tiết về **Dòng hợp đồng** chuyển hướng. Kế toán cũng có thể đặt các kích thước tài chính mặc định cho các dòng hợp đồng theo phương pháp thanh toán theo giá cố định trên tab này.

## <a name="billing-milestones"></a>Mốc thanh toán

Mô tả hợp đồng dự án sử dụng phương pháp thanh toán giá cố định được lập hóa đơn thông qua các mốc thanh toán. Các mốc thanh toán được đồng bộ hóa với các giao dịch trên tài khoản dự kiến trong ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Các mốc quan trọng của dòng hợp đồng tích hợp Hoạt động dự án (msdyn\_ hợp đồng** bảng sơ đồ.

  ![Tích hợp mốc thanh toán.](./media/2Milestones.jpg)

Kế toán viên có thể đánh giá các giao dịch trên tài khoản và điều chỉnh các thuộc tính kế toán cho các giao dịch đó bằng cách chuyển đến **Quản lý dự án và kế toán** > **Hợp đồng dự án** > **Duy trì** > **Giao dịch trên tài khoản** hoặc **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Duy trì** > **Giao dịch trên tài khoản**.

Trong lần đầu tiên tạo mốc thanh toán cho mô tả hợp đồng dự án nhất định, hệ thống sẽ tự động tạo một dự án ước tính doanh thu theo giá cố định cho dự án được liên kết với mô tả hợp đồng này. Các dự án ước tính doanh thu theo giá cố định có thể được xem xét bằng cách chuyển đến **Quản lý dự án và kế toán** > **Dự án ước tính doanh thu theo giá cố định**.

### <a name="project-tasks"></a>Nhiệm vụ dự án

Các nhiệm vụ dự án được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động thông qua **Nhiệm vụ dự án (msdyn\_ nhiệm vụ dự án)** bản đồ chỉ cho mục đích tham khảo. Các hoạt động tạo, cập nhật và xóa không được hỗ trợ thông qua các ứng dụng Tài chính và Hoạt động.

  ![Tích hợp nhiệm vụ dự án.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Nguồn lực dự án

Các **Vai trò tài nguyên dự án** thực thể được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Các vai trò tài nguyên dự án cho tất cả các công ty (các thể loại nguồn có thể đặt trước)** bản đồ chỉ cho mục đích tham khảo. Bởi vì tài nguyên đóng vai trò trong Dataverse không dành riêng cho công ty, hệ thống sẽ tự động tạo các bản ghi vai trò tài nguyên tương ứng của từng công ty cụ thể trong ứng dụng Tài chính và Hoạt động cho tất cả các pháp nhân được bao gồm trong phạm vi tích hợp ghi kép.

![Tích hợp vai trò nguồn lực.](./media/5Resources.jpg)

Nguồn lực dự án trong Hoạt động dự án được duy trì trong Dataverse và không được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động.

### <a name="transaction-categories"></a>Danh mục giao dịch

Danh mục giao dịch được duy trì trong Dataverse và được đồng bộ hóa với các ứng dụng Tài chính và Hoạt động bằng cách sử dụng **Các hạng mục giao dịch dự án (msdyn\_ các thể loại giao dịch)** bảng sơ đồ. Sau khi bản ghi danh mục giao dịch được đồng bộ hóa, hệ thống sẽ tự động tạo bốn bản ghi danh mục được chia sẻ. Mỗi bản ghi tương ứng với một loại giao dịch trong ứng dụng Tài chính và Hoạt động và liên kết chúng với bản ghi danh mục giao dịch.

![Tích hợp danh mục giao dịch.](./media/4TransactionCategories.jpg)

Việc sử dụng các danh mục giao dịch cho các giá trị ước tính và thực tế yêu cầu kế toán viên của dự án hoặc quản trị viên hệ thống phải tạo các danh mục dự án tương ứng trong mọi pháp nhân. Để biết thêm thông tin, hãy xem [Đặt cấu hình danh mục dự án](../project-accounting/configure-project-categories.md).
