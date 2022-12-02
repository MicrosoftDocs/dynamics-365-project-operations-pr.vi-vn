---
title: Thiết đặt dự án
description: Bài viết này cung cấp thông tin về thiết đặt quản lý dự án.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3d4b9b920150d31ae2366b4a1ee4168d71d70a17
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915854"
---
# <a name="project-settings"></a>Thiết đặt dự án

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sử dụng các thiết đặt sau để truy cập vào các tính năng hoạch định dự án.

## <a name="work-template"></a>Mẫu công việc

Để tạo lịch trình dự án, bạn tạo mẫu lịch dự án xác định số giờ làm việc mỗi ngày và thời gian đóng cửa. Để tạo mẫu lịch dự án, bạn liên kết công việc với trường **Mẫu lịch** cho dự án. Làm theo các bước sau để tạo mẫu công việc.

1. Trong PSA, trong ngăn điều hướng, hãy bấm vào **Nguồn lực**. 
2. Trên trang danh sách **Nguồn lực**, hãy mở bản ghi người dùng rồi chọn **Hiển thị giờ làm việc**.

  > [!NOTE]
  > Đảm bảo rằng bạn cho phép cửa sổ bật lên trên trang trình duyệt. Điều này cho phép bạn xem giờ làm việc đã đặt cho nguồn lực.
  
3. Trên tab **Xem hàng tháng**, hãy bấm vào **Thiết lập**. Danh sách ba tùy chọn xuất hiện: 

  - Lịch hàng tuần mới
  - Lịch hoạt động cho một ngày
  - Thời gian Rảnh

> ![Thiết lập tùy chọn.](media/project-13.png)

4. Chọn **Lịch trình hàng tuần mới** rồi đặt tùy chọn cho lịch trình nguồn lực này. Bạn có thể đặt lịch trình hàng tuần định kỳ, tham số giờ hàng ngày, thời gian đóng cửa và hơn thế nữa.
5. Để đặt phạm vi ngày, hãy chọn **Lưu** rồi bấm vào **Đóng**. 
6. Quay lại trang danh sách **Nguồn lực** rồi chọn nguồn lực mà bạn đặt giờ làm việc. 
7. Chọn **Đặt lịch ở dạng** để đặt mẫu công việc. 
8. Trong hộp thoại **Mẫu công việc**, hãy nhập tên cho mẫu công việc rồi chọn **Áp dụng**. 

Bạn hiện có thể liên kết mẫu công việc với mẫu lịch dự án.

## <a name="resource-roles"></a>Vai trò nguồn lực

Thuật ngữ *vai trò nguồn lực* đề cập đến một bộ kỹ năng, năng lực và chứng chỉ mà một người phải có để thực hiện một bộ nhiệm vụ cụ thể trên một dự án. PSA cho phép chi trả và lập hóa đơn thời gian của nguồn lực dựa trên vai trò mà nguồn lực được liên kết. Mỗi tổ chức phải thiết lập các vai trò này bằng cách dùng điều hướng bên trái trên menu **Project Service**.

Mỗi tổ chức phải thiết lập các vai trò này trên trang **Loại nguồn lực hiện hoạt**. Để mở trang này, trong ngăn điều hướng bên trái, hãy chọn **Vai trò nguồn lực**.

## <a name="price-lists"></a>Bảng giá

Bảng giá cho phép bạn đặt chi phí và giá bán hàng cho vai trò nguồn lực, loại chi phí, sản phẩm và các yếu tố khác trong tổ chức. Trước khi đặt ước tính tài chính cho công việc phải được giao cho dự án, bạn nên tạo bảng giá bán hàng và chi phí hỗ trợ. Trong phần tham số, bạn cũng nên thiết lập một bảng giá bán hàng và chi phí mặc định áp dụng cho tất cả dự án được tạo trong tổ chức. Trên trang **Tham số dự án hiện hoạt**, hãy đảm bảo bạn thiết lập bảng giá bán hàng và chi phí mặc định.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
