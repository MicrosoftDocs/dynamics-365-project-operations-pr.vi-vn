---
title: Tạo thực thể và trường tùy chỉnh làm thông số định giá
description: Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898287"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Tạo thực thể và trường tùy chỉnh làm thông số định giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh.

> [!IMPORTANT]
> Bạn nên thực hiện tất cả thay đổi kích thước giá tùy chỉnh trong một giải pháp riêng. Cách làm quan trọng này sẽ giúp bạn có thể thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang phiên bản khác. Sau khi bạn thực hiện tất cả các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng **Giải pháp được quản lý** và nhập nó vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Tạo giải pháp tùy chỉnh cho kích thước giá
1. Chuyển đến **Chế độ cài đặt** > **Giải pháp**, rồi chọn **Mới** để tạo một giải pháp mới. 
2. Đặt tên giải pháp, **\<your organization name> kích thước giá**, nhập thông tin yêu cầu còn lại, sau đó chọn **Lưu**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Tạo các trường tùy chỉnh và bộ tùy chọn trong giải pháp kích thước giá

Kích thước giá có thể là một bộ tùy chọn hoặc một thực thể. Cả hai phải được tạo trong giải pháp giá cả của bạn. Các bước trong quy trình này giải thích cách tạo kích thước dựa trên thực thể và kích thước dựa trên bộ tùy chọn.

### <a name="entity-based-dimensions"></a>Kích thước dựa trên thực thể

1. Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**.
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể**.
3. Chọn **Mới** để tạo một thực thể mới gọi là **Chức vụ tiêu chuẩn**. 
4. Nhập các thông tin cần thiết còn lại, sau đó chọn **Lưu**.


### <a name="option-set-based-dimensions"></a>Kích thước dựa trên bộ tùy chọn 
Bạn có thể tạo hai kích thước dựa trên bộ tùy chọn. Sử dụng **Vị trí làm việc của nguồn lực** để theo dõi giá của công việc ở vị trí **Nhà** và công việc **Tại chỗ**, cũng như sử dụng **Số giờ làm việc của nguồn lực** với các giá trị **Giờ làm việc** và **Ngoài giờ** để áp dụng đánh dấu khi công việc hoàn tất.


1. Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**. 
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Bộ tùy chọn**. 
3. Chọn **Mới** để tạo bộ tùy chọn mới, nhập thông tin yêu cầu còn lại, và sau đó chọn **Lưu**.

## <a name="create-data-for-entity-based-dimensions"></a>Tạo dữ liệu cho kích thước dựa trên thực thể

Bạn có thể tạo dữ liệu cho kích thước dựa trên thực thể theo cách thủ công hoặc bằng cách sử dụng lệnh gọi dịch vụ hoặc nhập Microsoft Excel. Sử dụng các bước trong quy trình này để tạo hai chức vụ tiêu chuẩn là **Kỹ sư hệ thống** và **Kỹ sư hệ thống cấp cao** từ kích thước dựa trên thực thể **Chức vụ tiêu chuẩn**. Nếu dữ liệu bạn muốn tạo nhỏ, như trong ví dụ sau đây, bạn có thể sử dụng biểu mẫu chuẩn.

1. Chọn **Tìm nâng cao**, chọn thực thể **Chức vụ tiêu chuẩn**, rồi chọn **Kết quả**. Tất cả các hàng trong thực thể **Chức vụ tiêu chuẩn** sẽ hiển thị.
2. Chọn **Mới**, và trong trường **Tên**, hãy nhập "Kỹ sư hệ thống" rồi chọn **Lưu**.
3. Đóng biểu mẫu. 
4. Lặp lại bước 1-3 để tạo một chức vụ tiêu chuẩn khác cho "Kỹ sư hệ thống cao cấp".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Thêm tất cả các thực thể yêu cầu và các thành phần liên quan đến Giải pháp kích thước giá
Bạn sẽ cần thêm các thực thể sau đây vào giải pháp giá của bạn. Sử dụng các bước trong quy trình này để thực hiện một số thay đổi sơ đồ quan trọng trong giải pháp giá để các thực thể trở thành kích thước giá mới.

1. Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**. 
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


> [!NOTE]
> Đảm bảo bao gồm tất cả các biểu mẫu và dạng xem cho từng thực thể được chọn.

4. Khi được nhắc đưa vào bất kỳ thực thể phụ thuộc nào cho các thực thể đã chọn ở trên, hãy chọn **Không**.

