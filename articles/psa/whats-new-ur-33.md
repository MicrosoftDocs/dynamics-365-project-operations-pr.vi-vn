---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 33, V3
description: Bài viết này liệt kê các tính năng và bản sửa lỗi có sẵn trong Bản phát hành cập nhật tự động hóa dịch vụ dự án 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915442"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Bài viết này liệt kê các tính năng và bản sửa lỗi mới hoặc được thay đổi cho Tự động hóa dịch vụ dự án V3, Bản phát hành cập nhật 33. Phiên bản này có số bản dựng là V3.10.54.98 và thường có sẵn thông qua bản tự cập nhật vào tháng 7 năm 2021.

## <a name="update-release-33"></a>Phát hành bản cập nhật 33

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

- Hai trường bị khóa, **msdyn_description** và **msdyn_externaldescription** có thể chỉnh sửa sau khi gửi.
- Thông báo lỗi xảy ra nếu một khoản chi phí được tạo ra không liên quan đến dự án.
- Khi mục nhập thời gian được tạo, vai trò nguồn lực mặc định là vai trò không hoạt động.
- Các dòng nhật ký kế toán liên quan đến chi phí bị thu hồi và đã xóa sẽ không bị xóa.
- Trên **Mục nhập thời gian Tạo biểu mẫu nhanh**, cập nhật dạng xem **Danh sách nhiệm vụ dự án** để thay đổi ngày được hiển thị theo mặc định thành ngày bắt đầu của nhiệm vụ.
- Khi bạn tạo một mục nhập thời gian từ tab **Có liên quan** của nguồn lực có thể đặt trước, mục nhập thời gian được tạo không chính xác cho người dùng đã đăng nhập thay vì nguồn lực chính có thể đặt trước.
- Các trường mới được thêm vào hộp thoại **MDD phê duyệt hàng loạt**.

**Lập kế hoạch dự án**

Các vấn đề sau đã được khắc phục:
- Hiệu suất tạo dự án chậm khi các mẫu giờ làm việc của dự án được áp dụng với các lịch phức tạp.
- Khi ngày bắt đầu lớn hơn ngày kết thúc, lỗi sẽ hiển thị trên mẫu dự án sao chép do sự khác biệt về thành phần thời gian của mỗi trường.

**Quản lý nguồn lực**

Các vấn đề sau đã được khắc phục:
- Tham số không chính xác được sử dụng trong truy vấn sử dụng tài nguyên và XML dẫn đến kết quả bộ lọc không chính xác trên lưới **Thời gian làm việc của nguồn lực**.
- Xác nhận **Mở rộng đăng ký** hiển thị ngày kết thúc chính xác cho đăng ký.

**Bán hàng**

Các vấn đề sau đã được khắc phục:
- Thông báo lỗi xảy ra nếu giá danh mục được tạo với các giá trị bị thiếu.
- Thông báo lỗi xảy ra nếu một mốc mô tả hợp đồng được tạo mà không có dòng đơn hàng.
