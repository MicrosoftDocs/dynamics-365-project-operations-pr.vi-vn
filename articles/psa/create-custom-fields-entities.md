---
title: Tạo các trường và thực thể tùy chỉnh
description: Bài viết này giải thích cách tạo các tập hợp tùy chọn và thực thể trong giải pháp của riêng bạn trong Power Apps nền tảng.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3b6f675d604f3b6a6f2465c413ceff3d16815e12
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926940"
---
# <a name="create-custom-fields-and-entities"></a>Tạo các trường và thực thể tùy chỉnh 

[!include [banner](../includes/psa-now-project-operations.md)]

Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh trên nền tảng Power Apps.  
Các thủ tục trong bài viết này nên được hoàn thành bằng cách sử dụng giao diện web của Tự động hóa dịch vụ dự án (PSA).

> [!IMPORTANT]
> Bạn nên thực hiện tất cả thay đổi kích thước giá tùy chỉnh trong một giải pháp riêng. Cách làm quan trọng này sẽ giúp bạn có thể thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang phiên bản khác. Sau khi bạn thực hiện tất cả các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng **Giải pháp được quản lý** và nhập nó vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Tạo các trường tùy chỉnh và bộ tùy chọn trong giải pháp kích thước giá

Kích thước giá có thể là một bộ tùy chọn hoặc một thực thể. Cả hai phải được tạo trong giải pháp giá cả của bạn. Các bước trong quy trình này giải thích cách tạo kích thước dựa trên thực thể và kích thước dựa trên bộ tùy chọn.

### <a name="entity-based-dimensions"></a>Kích thước dựa trên thực thể

1. Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> thông số định giá**.
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể**.
3. Nhấp vào **Mới** để tạo một thực thể mới gọi là **Chức vụ tiêu chuẩn**. Nhập các thông tin cần thiết còn lại, sau đó nhấp vào **Lưu**.

> ![Định nghĩa thực thể chức vụ tiêu chuẩn.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Kích thước dựa trên bộ tùy chọn 
Bạn có thể tạo hai kích thước dựa trên bộ tùy chọn. Sử dụng **Vị trí làm việc của nguồn lực** để theo dõi giá của công việc ở vị trí **Nhà** và công việc **Tại chỗ**, cũng như sử dụng **Số giờ làm việc của nguồn lực** với các giá trị **Giờ làm việc** và **Ngoài giờ** để áp dụng đánh dấu khi công việc hoàn tất.


1. Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> thông số định giá**. 
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Bộ tùy chọn**. 
3. Nhấp vào **Mới** để tạo bộ tùy chọn mới, nhập thông tin yêu cầu còn lại, và sau đó nhấp vào **Lưu**.

> ![Kích thước giá dựa trên bộ tùy chọn gọi là Vị trí làm việc của nguồn lực.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Kích thước giá dựa trên bộ tùy chọn gọi là Số giờ làm việc của nguồn lực.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Tạo dữ liệu cho kích thước dựa trên thực thể

Bạn có thể tạo dữ liệu cho kích thước dựa trên thực thể theo cách thủ công hoặc bằng cách sử dụng lệnh gọi dịch vụ hoặc nhập Microsoft Excel. Sử dụng các bước trong quy trình này để tạo hai chức vụ tiêu chuẩn là **Kỹ sư hệ thống** và **Kỹ sư hệ thống cấp cao** từ kích thước dựa trên thực thể **Chức vụ tiêu chuẩn**. Nếu dữ liệu bạn muốn tạo nhỏ, như trong ví dụ sau đây, bạn có thể sử dụng biểu mẫu chuẩn.

1. Trong PSA, nhấp vào **Tìm kiếm nâng cao**. Chọn thực thể **Chức vụ tiêu chuẩn**, sau đó nhấp vào **Kết quả**. Tất cả các hàng trong thực thể **Chức vụ tiêu chuẩn** sẽ hiển thị.
2. Bấm vào **Mới**. Trong trường **Tên**, nhập "Kỹ sư hệ thống", sau đó nhấp vào **Lưu**.
3. Đóng biểu mẫu. 
4. Lặp lại bước 1-3 để tạo một chức vụ tiêu chuẩn khác cho "Kỹ sư hệ thống cao cấp".

> ![Dữ liệu mẫu cho thực thể Chức vụ tiêu chuẩn.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
