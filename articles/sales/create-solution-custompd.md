---
title: Tạo giải pháp cho thông số định giá tùy chỉnh
description: Chủ đề này trình bày thông tin về cách tạo giải pháp cho các thông số giá cả tùy chỉnh.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514037"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Tạo giải pháp cho thông số định giá tùy chỉnh

 _**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_ 

>[!IMPORTANT]
>Tất cả các thay đổi về thông số định giá tùy chỉnh phải nằm trong một giải pháp riêng biệt. Cách làm quan trọng này sẽ cho phép bạn thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang các phiên bản khác. Sau khi bạn thực hiện tất cả các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng giải pháp **Được quản lý** và nhập vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Tạo giải pháp cho thông số định giá tùy chỉnh

1.  Chọn **Cài đặt** > **Giải pháp** rồi chọn **Mới**.
2.  Đặt tên giải pháp này là *<your organization name> thông số giá*.
3. Nhập các thông tin cần thiết còn lại, sau đó chọn **Lưu**.

  ![Cách tạo giải pháp thông số giá tùy chỉnh](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Thêm tất cả các thực thể cần thiết và các thành phần liên quan vào giải pháp Thông số định giá

Thêm các thực thể Project Service sau vào giải pháp giá của bạn để thực hiện những thay đổi quan trọng đối với sơ đồ trong giải pháp giá. Sau khi bạn hoàn tất quy trình này, các thực thể sẽ ghi nhận các thông số giá mới.

1.  Chọn **Cài đặt** > **Giải pháp** rồi bấm đúp vào **<*tên tổ chức của bạn*> thông số giá**.
2.  Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thêm hiện có** > **Thực thể**.
3.  Trong hộp thoại **Thành phần giải pháp**, chọn các thực thể sau:
 
   - **Thực tế**
   - **Nguồn lực có thể đăng ký**
   - **Mô tả Ước tính**
   - **Nhiệm vụ dự án**
   - **Chi tiết Mô tả Hóa đơn**
   - **Dòng nhật ký kế toán**
   - **Chi tiết Mô tả Hợp đồng Dự án**
   - **Thành viên Nhóm Dự án**
   - **Chi tiết Mô tả Báo giá**
   - **Tăng giá theo Vai trò**
   - **Giá Vai trò**
   - **Mục nhập Thời gian**
 
   ![Thêm giải pháp thông số giá tùy chỉnh cho các thực thể hiện có](./media/Existing-entities-to-PD-solution.png)
 
 4. Đối với từng thực thể, hãy xem lại các thành phần được thêm cũng như danh sách chính thức của các tài sản thực thể. 

   >[!NOTE]
   > Đưa vào tất cả biểu mẫu và dạng xem cho từng thực thể đã chọn.

  ![Đã thêm thực thể](./media/solution-component-selection.png)


5.  Khi được nhắc đưa vào bất kỳ thực thể phụ thuộc nào cho các thực thể đã chọn, hãy bấm vào **Không, không đưa vào các thành phần bắt buộc.**

    ![Đưa vào các thực thể phụ thuộc](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]