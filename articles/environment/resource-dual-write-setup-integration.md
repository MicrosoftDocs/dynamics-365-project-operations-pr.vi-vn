---
title: Tích hợp dữ liệu cấu hình và thiết lập Project Operations
description: Bài viết này cung cấp thông tin về cách thiết lập và cấu hình bản đồ ghi kép Hoạt động Dự án.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029178"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Tích hợp dữ liệu cấu hình và thiết lập Project Operations

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này cung cấp thông tin về tích hợp ghi kép Hoạt động dự án cho các thực thể thiết lập và cấu hình.

## <a name="project-contracts-contract-lines-and-projects"></a>Hợp đồng dự án, mô tả hợp đồng và dự án

Các hợp đồng dự án, các dòng hợp đồng và các dự án được tạo trong Dataverse và được đồng bộ hóa với các ứng dụng tài chính và hoạt động để kế toán bổ sung. Bản ghi trong các thực thể này chỉ có thể được tạo và xóa trong Dataverse. Tuy nhiên, các thuộc tính kế toán như giá trị mặc định của nhóm thuế bán hàng và thứ nguyên tài chính có thể được thêm vào các bản ghi này trong ứng dụng tài chính và hoạt động.

  ![Khái niệm về tích hợp hợp đồng dự án.](./media/1ProjectContract.jpg)

Khách hàng tiềm năng, cơ hội và báo giá hoạt động bán hàng được theo dõi trong Dataverse và không đồng bộ hóa với các ứng dụng tài chính và hoạt động vì không có kế toán hạ nguồn nào được liên kết với hoạt động này.

Chức năng hợp đồng dự án trong Dataverse tạo hồ sơ hợp đồng dự án trong các ứng dụng tài chính và hoạt động bằng cách sử dụng **Tiêu đề hợp đồng dự án (đơn hàng bán)** bản đồ bảng. Lưu hợp đồng dự án trong Dataverse cũng bắt đầu tạo bản ghi thực thể khách hàng hợp đồng dự án. Hồ sơ này được đồng bộ hóa với các ứng dụng tài chính và hoạt động bằng cách sử dụng **Nguồn vốn dự án (msdyn\_ projectcontractssplitbillingrules)** bản đồ bảng. Bản đồ này cũng đồng bộ hóa các hoạt động bổ sung, cập nhật và xóa của khách hàng trong hợp đồng dự án. Tỷ lệ thanh toán phân chia giữa các khách hàng hợp đồng dự án chỉ được nắm vững trong Dataverse và không được đồng bộ hóa với các ứng dụng tài chính và hoạt động.

Sau khi hợp đồng dự án được tạo trong Dataverse, kế toán dự án có thể cập nhật các thuộc tính kế toán cho hợp đồng dự án này trong ứng dụng tài chính và hoạt động bằng cách truy cập **Quản lý dự án và kế toán** > **Hợp đồng dự án** > **Cài đặt** > **Hiển thị kế toán mặc định**. Kế toán có thể xem xét các thuộc tính hợp đồng dự án hoạt động, chẳng hạn như ngày giao hàng được yêu cầu và số tiền hợp đồng bằng cách chọn ID hợp đồng dự án trong ứng dụng tài chính và hoạt động để mở hồ sơ hợp đồng dự án liên quan trong Dataverse.

Thực thể dự án được đồng bộ hóa với các ứng dụng tài chính và vận hành bằng cách sử dụng **Dự án V2 (msdyn\_ dự án)** bản đồ bảng. Kế toán viên của dự án có thể:

  - Xem lại các dự án trong ứng dụng tài chính và hoạt động bằng cách truy cập **Quản lý dự án và kế toán** > **Tất cả các dự án**. 
  - Cập nhật các thuộc tính kế toán cho dự án trong ứng dụng tài chính và hoạt động bằng cách truy cập **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Cài đặt** > **Hiển thị kế toán mặc định**.  
  - Xem lại các thuộc tính của dự án hoạt động, chẳng hạn như ngày bắt đầu và ngày kết thúc ước tính, bằng cách chọn ID dự án trong ứng dụng tài chính và hoạt động để mở hồ sơ dự án liên quan trong Dataverse.

Một dự án được liên kết với hợp đồng dự án thông qua thực thể **Mô tả hợp đồng dự án**.

Các dòng hợp đồng dự án trong Dataverse tạo quy tắc thanh toán hợp đồng dự án trong các ứng dụng tài chính và hoạt động bằng cách sử dụng **Các dòng hợp đồng dự án (chi tiết bán hàng)** bản đồ bảng. Phương thức thanh toán xác định loại quy tắc thanh toán hợp đồng dự án trong các ứng dụng tài chính và hoạt động:

  - Mô tả hợp đồng dự án có phương thức thanh toán theo thời gian và vật tư tạo ra quy tắc thanh toán về thời gian và loại vật tư.
  - Mô tả hợp đồng có phương thức thanh toán giá cố định tạo ra một quy tắc thanh toán quan trọng.

Kế toán dự án có thể xem xét các dòng hợp đồng dự án trong các ứng dụng tài chính và hoạt động bằng cách vào **Quản lý dự án và kế toán** > **Hợp đồng dự án** > **Cài đặt** > **Hiển thị kế toán mặc định** và xem xét các chi tiết về **Dòng hợp đồng** chuyển hướng. Kế toán cũng có thể đặt các thứ nguyên tài chính mặc định cho các dòng hợp đồng theo phương pháp thanh toán theo giá cố định trên tab này.

## <a name="billing-milestones"></a>Mốc thanh toán

Mô tả hợp đồng dự án sử dụng phương pháp thanh toán giá cố định được lập hóa đơn thông qua các mốc thanh toán. Các mốc thanh toán được đồng bộ hóa để dự kiến các giao dịch trên tài khoản trong các ứng dụng tài chính và hoạt động bằng cách sử dụng **Các mốc quan trọng của dòng hợp đồng tích hợp Hoạt động dự án (msdyn\_ hợp đồng** bản đồ bảng.

  ![Tích hợp mốc thanh toán.](./media/2Milestones.jpg)

Kế toán viên có thể đánh giá các giao dịch trên tài khoản và điều chỉnh các thuộc tính kế toán cho các giao dịch đó bằng cách chuyển đến **Quản lý dự án và kế toán** > **Hợp đồng dự án** > **Duy trì** > **Giao dịch trên tài khoản** hoặc **Quản lý dự án và kế toán** > **Tất cả các dự án** > **Duy trì** > **Giao dịch trên tài khoản**.

Trong lần đầu tiên tạo mốc thanh toán cho mô tả hợp đồng dự án nhất định, hệ thống sẽ tự động tạo một dự án ước tính doanh thu theo giá cố định cho dự án được liên kết với mô tả hợp đồng này. Các dự án ước tính doanh thu theo giá cố định có thể được xem xét bằng cách chuyển đến **Quản lý dự án và kế toán** > **Dự án ước tính doanh thu theo giá cố định**.

### <a name="project-tasks"></a>Nhiệm vụ dự án

Các nhiệm vụ dự án được đồng bộ hóa với các ứng dụng tài chính và vận hành thông qua **Nhiệm vụ dự án (msdyn\_ nhiệm vụ dự án)** bản đồ bảng chỉ cho mục đích tham khảo. Các hoạt động tạo, cập nhật và xóa không được hỗ trợ thông qua các ứng dụng tài chính và hoạt động.

  ![Tích hợp nhiệm vụ dự án.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Nguồn lực dự án

Các **Vai trò tài nguyên dự án** thực thể được đồng bộ hóa với các ứng dụng tài chính và hoạt động bằng cách sử dụng **Các vai trò tài nguyên dự án cho tất cả các công ty (các thể loại nguồn có thể đặt trước)** bản đồ bảng chỉ cho mục đích tham khảo. Bởi vì tài nguyên đóng vai trò trong Dataverse không dành riêng cho công ty, hệ thống sẽ tự động tạo các bản ghi vai trò tài nguyên tương ứng của từng công ty cụ thể trong các ứng dụng tài chính và hoạt động cho tất cả các pháp nhân được bao gồm trong phạm vi tích hợp ghi kép.

![Tích hợp vai trò nguồn lực.](./media/5Resources.jpg)

Nguồn lực dự án trong Hoạt động dự án được duy trì trong Dataverse và không được đồng bộ hóa với các ứng dụng tài chính và hoạt động.

### <a name="transaction-categories"></a>Danh mục giao dịch

Các danh mục giao dịch được duy trì trong Dataverse và được đồng bộ hóa với các ứng dụng tài chính và hoạt động bằng cách sử dụng **Các hạng mục giao dịch dự án (msdyn\_ các thể loại giao dịch)** bản đồ bảng. Sau khi bản ghi danh mục giao dịch được đồng bộ hóa, hệ thống sẽ tự động tạo bốn bản ghi danh mục được chia sẻ. Mỗi bản ghi tương ứng với một loại giao dịch trong ứng dụng tài chính và hoạt động và liên kết chúng với bản ghi danh mục giao dịch.

![Tích hợp danh mục giao dịch.](./media/4TransactionCategories.jpg)

Việc sử dụng các danh mục giao dịch cho các giá trị ước tính và thực tế yêu cầu kế toán viên của dự án hoặc quản trị viên hệ thống phải tạo các danh mục dự án tương ứng trong mọi pháp nhân. Để biết thêm thông tin, hãy xem [Đặt cấu hình danh mục dự án](../project-accounting/configure-project-categories.md).
