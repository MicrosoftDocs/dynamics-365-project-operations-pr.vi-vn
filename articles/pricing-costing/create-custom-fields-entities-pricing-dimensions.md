---
title: Tạo thực thể và trường tùy chỉnh làm thông số định giá
description: Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642839"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Tạo thực thể và trường tùy chỉnh làm thông số định giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hãy làm theo các bước sau nếu bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh để dùng làm thông số định giá. Để biết thêm thông tin, hãy xem [Tổng quan về thông số định giá](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Bạn nên thực hiện tất cả thay đổi kích thước giá tùy chỉnh trong một giải pháp riêng. Đây là phương pháp quan trọng mang đến sự linh hoạt nếu bạn cần cập nhật hoặc xóa các thay đổi trong tương lai. Điều này cũng sẽ hỗ trợ việc sử dụng lại công việc của bạn, cũng như giúp bạn dễ dàng áp dụng những thay đổi này vào một phiên bản khác. Sau khi bạn đã thực hiện mọi thay đổi cần thiết, hãy xuất giải pháp này là **Giải pháp được quản lý**, sau đó nhập vào phiên bản khác để sử dụng lại cách thiết lập giá cả.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Tạo các trường tùy chỉnh và bộ tùy chọn trong giải pháp kích thước giá

Kích thước giá có thể là một bộ tùy chọn hoặc một thực thể. Cả hai phải được tạo trong giải pháp giá cả của bạn. Các bước trong quy trình này giải thích cách tạo kích thước dựa trên thực thể và kích thước dựa trên bộ tùy chọn.

### <a name="entity-based-dimensions"></a>Kích thước dựa trên thực thể
Để tạo các thông số dựa trên thực thể, hãy làm theo các bước sau:

1. Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**.
2. Trong Trình khám phá giải pháp, trên ngăn điều hướng bên trái, hãy chọn **Thực thể**.
3. Chọn **Mới** để tạo một thực thể mới gọi là **Chức vụ tiêu chuẩn**. 
4. Nhập các thông tin cần thiết còn lại, sau đó chọn **Lưu**.

> ![Định nghĩa thực thể chức vụ tiêu chuẩn](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Kích thước dựa trên bộ tùy chọn 
Bạn có thể tạo hai kích thước dựa trên bộ tùy chọn. 

- Dùng **Vị trí làm việc của nguồn lực** để theo dõi giá của công việc có vị trí làm việc tại **Nhà** hoặc **Tại cơ sở**. 
- Dùng **Giờ làm việc của nguồn lực** với giá trị là **Bình thường** và **Ngoài giờ** để áp dụng phần tăng giá khi công việc hoàn thành.

Hình sau mang đến cái nhìn tổng quan về thông số **Vị trí làm việc của nguồn lực**. 

> ![Kích thước giá dựa trên bộ tùy chọn gọi là Vị trí làm việc của nguồn lực](media/Option-set-PD-called-Resource-Work-Location.png)

Hình sau mang đến cái nhìn tổng quan về thông số **Giờ làm việc của nguồn lực**. 

> ![Kích thước giá dựa trên bộ tùy chọn gọi là Số giờ làm việc của nguồn lực](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**. 
2. Trong Trình khám phá giải pháp, trên ngăn điều hướng bên trái, chọn **Bộ tùy chọn**. 
3. Chọn **Mới** để tạo bộ tùy chọn mới, nhập thông tin yêu cầu còn lại, và sau đó chọn **Lưu**.

## <a name="create-data-for-entity-based-dimensions"></a>Tạo dữ liệu cho kích thước dựa trên thực thể

Bạn có thể tạo dữ liệu cho kích thước dựa trên thực thể theo cách thủ công hoặc bằng cách sử dụng lệnh gọi dịch vụ hoặc nhập Microsoft Excel. Sử dụng các bước trong quy trình này để tạo hai chức vụ tiêu chuẩn là **Kỹ sư hệ thống** và **Kỹ sư hệ thống cấp cao** từ kích thước dựa trên thực thể **Chức vụ tiêu chuẩn**. Nếu dữ liệu bạn muốn tạo nhỏ, như trong ví dụ sau đây, bạn có thể sử dụng biểu mẫu chuẩn.

1. Chọn **Tìm kiếm nâng cao**.
2. Chọn thực thể **Chức vụ tiêu chuẩn**, sau đó chọn **Kết quả**. Tất cả các hàng trong thực thể **Chức vụ tiêu chuẩn** sẽ hiển thị.
3. Chọn **Mới**, và trong trường **Tên**, hãy nhập "Kỹ sư hệ thống" rồi chọn **Lưu**.
4. Đóng trang. 
5. Lặp lại bước 1-3 để tạo một chức vụ tiêu chuẩn khác cho "Kỹ sư hệ thống cao cấp".

> ![Dữ liệu mẫu cho thực thể Chức vụ tiêu chuẩn](media/ST-data.png)
