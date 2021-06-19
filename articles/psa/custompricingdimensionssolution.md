---
title: Tạo giải pháp tùy chỉnh cho thông số định giá
description: Chủ đề này giải thích cách tạo giải pháp tùy chỉnh khi tạo thông số định giá tùy chỉnh.
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
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012342"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Tạo giải pháp tùy chỉnh cho thông số định giá

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Tất cả các thay đổi về thông số định giá tùy chỉnh phải nằm trong một giải pháp riêng biệt. Cách làm quan trọng này sẽ giúp bạn có thể thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang phiên bản khác. Sau khi bạn thực hiện các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng **Giải pháp được quản lý** và nhập nó vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.

1. Chọn **Cài đặt** > **Giải pháp** rồi chọn **Mới**. 
2. Đặt tên giải pháp, **\<your organization name> kích thước giá**, nhập thông tin yêu cầu còn lại, sau đó chọn **Lưu**.

> ![Tạo giải pháp tùy chỉnh cho kích thước giá](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Thêm tất cả các thực thể cần thiết và các thành phần liên quan vào giải pháp Thông số định giá
Bạn sẽ cần thêm các thực thể Project Service sau đây vào giải pháp giá của bạn. Hoàn thành các bước trong quy trình này để thực hiện một số thay đổi sơ đồ quan trọng trong giải pháp giá để các thực thể trở thành kích thước giá mới.

1. Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**. 
2. Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thêm hiện có** > **Thực thể**.
3. Trong hộp thoại **Thành phần giải pháp**, chọn các thực thể sau:

- Thực tế
- Nguồn lực có thể đăng ký
- Mô tả Ước tính
- Nhiệm vụ dự án
- Chi tiết Mô tả Hóa đơn
- Dòng nhật ký kế toán
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

4. Khi được nhắc đưa vào tất cả các thực thể phụ thuộc cho các thực thể đã chọn, hãy chọn **Không**.

> ![Không bao gồm tất cả thành phần liên quan](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]