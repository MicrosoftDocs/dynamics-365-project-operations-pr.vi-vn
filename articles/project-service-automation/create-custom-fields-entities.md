---
title: Tạo các trường và thực thể tùy chỉnh
description: Chủ đề này giải thích cách tạo bộ tùy chọn và thực thể trong giải pháp của riêng bạn trong nền tảng Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757121"
---
# <a name="create-custom-fields-and-entities"></a>Tạo các trường và thực thể tùy chỉnh 

Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh trên nền tảng Power Apps.  
Các quy trình trong chủ đề này sẽ được hoàn thành bằng cách sử dụng giao diện web của Project Service Automation (PSA).

> [!IMPORTANT]
> Bạn nên thực hiện tất cả thay đổi kích thước giá tùy chỉnh trong một giải pháp riêng. Cách làm quan trọng này sẽ giúp bạn có thể thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang phiên bản khác. Sau khi bạn thực hiện tất cả các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng **Giải pháp được quản lý** và nhập nó vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Tạo giải pháp tùy chỉnh cho kích thước giá
1. Trong PSA, nhấp vào **Thiết đặt** > **Giải pháp**, sau đó nhấp vào **Mới** để tạo một giải pháp mới. 
2. Đặt tên giải pháp, **\<tên tổ chức của bạn> kích thước giá**, nhập thông tin yêu cầu còn lại, sau đó nhấp vào **Lưu**.

> ![Tạo giải pháp tùy chỉnh cho kích thước giá](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Tạo các trường tùy chỉnh và bộ tùy chọn trong giải pháp kích thước giá

Kích thước giá có thể là một bộ tùy chọn hoặc một thực thể. Cả hai phải được tạo trong giải pháp giá cả của bạn. Các bước trong quy trình này giải thích cách tạo kích thước dựa trên thực thể và kích thước dựa trên bộ tùy chọn.

### <a name="entity-based-dimensions"></a>Kích thước dựa trên thực thể

1. Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, sau đó nhấp đúp vào **\<tên tổ chức > kích thước giá**.
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể**.
3. Nhấp vào **Mới** để tạo một thực thể mới gọi là **Chức vụ tiêu chuẩn**. Nhập các thông tin cần thiết còn lại, sau đó nhấp vào **Lưu**.

> ![Định nghĩa thực thể chức vụ tiêu chuẩn](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Kích thước dựa trên bộ tùy chọn 
Bạn có thể tạo hai kích thước dựa trên bộ tùy chọn. Sử dụng **Vị trí làm việc của nguồn lực** để theo dõi giá của công việc ở vị trí **Nhà** và công việc **Tại chỗ**, cũng như sử dụng **Số giờ làm việc của nguồn lực** với các giá trị **Giờ làm việc** và **Ngoài giờ** để áp dụng đánh dấu khi công việc hoàn tất.


1. Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, sau đó nhấp đúp vào **\<tên tổ chức > kích thước giá**. 
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Bộ tùy chọn**. 
3. Nhấp vào **Mới** để tạo bộ tùy chọn mới, nhập thông tin yêu cầu còn lại, và sau đó nhấp vào **Lưu**.

> ![Kích thước giá dựa trên bộ tùy chọn gọi là Vị trí làm việc của nguồn lực ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Kích thước giá dựa trên bộ tùy chọn gọi là Số giờ làm việc của nguồn lực ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Tạo dữ liệu cho kích thước dựa trên thực thể

Bạn có thể tạo dữ liệu cho kích thước dựa trên thực thể theo cách thủ công hoặc bằng cách sử dụng lệnh gọi dịch vụ hoặc nhập Microsoft Excel. Sử dụng các bước trong quy trình này để tạo hai chức vụ tiêu chuẩn là **Kỹ sư hệ thống** và **Kỹ sư hệ thống cấp cao** từ kích thước dựa trên thực thể **Chức vụ tiêu chuẩn**. Nếu dữ liệu bạn muốn tạo nhỏ, như trong ví dụ sau đây, bạn có thể sử dụng biểu mẫu chuẩn.

1. Trong PSA, nhấp vào **Tìm kiếm nâng cao**. Chọn thực thể **Chức vụ tiêu chuẩn**, sau đó nhấp vào **Kết quả**. Tất cả các hàng trong thực thể **Chức vụ tiêu chuẩn** sẽ hiển thị.
2. Bấm vào **Mới**. Trong trường **Tên**, nhập "Kỹ sư hệ thống", sau đó nhấp vào **Lưu**.
3. Đóng biểu mẫu. 
4. Lặp lại bước 1-3 để tạo một chức vụ tiêu chuẩn khác cho "Kỹ sư hệ thống cao cấp".

> ![Dữ liệu mẫu cho thực thể chức vụ tiêu chuẩn ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Thêm tất cả các thực thể PSA yêu cầu và các thành phần liên quan đến giải pháp kích thước giá
Bạn sẽ cần thêm các thực thể Project Service sau đây vào giải pháp giá của bạn. Sử dụng các bước trong quy trình này để thực hiện một số thay đổi sơ đồ quan trọng trong giải pháp giá để các thực thể trở thành kích thước giá mới.

1. Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, sau đó nhấp đúp vào **\<tên tổ chức > kích thước giá**. 
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thêm hiện có** > **Thực thể**.
3. Trong hộp thoại **Thành phần giải pháp**, chọn các thực thể sau:

- Thực tế
- Nguồn lực có thể đặt trước
- Mô tả Ước tính
- Chi tiết Mô tả Hóa đơn
- Dòng Nhật ký Kế toán
- Chi tiết Mô tả Hợp đồng Dự án
- Thành viên Nhóm Dự án
- Chi tiết Mô tả Báo giá
- Tăng giá theo Vai trò
- Giá Vai trò 
- Mục nhập Thời gian 

> ![Thêm các thực thể hiện có vào giải pháp kích thước giá](media/Existing-entities-to-PD-solution.png)

> ![Chọn thành phần giải pháp.](media/Dimension-Components.png)

> [!NOTE]
> Đảm bảo bao gồm tất cả các biểu mẫu và dạng xem cho từng thực thể được chọn.

4. Khi được nhắc đưa vào bất kỳ thực thể phụ thuộc nào cho các thực thể đã chọn ở trên, nhấp vào **Không**.

> ![Không bao gồm tất cả thành phần liên quan](media/Do-not-include-required.png)


