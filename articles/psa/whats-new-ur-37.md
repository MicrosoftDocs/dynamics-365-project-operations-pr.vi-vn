---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 37, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có sẵn trong Microsoft Dynamics 365 Project Service Automation Bản phát hành cập nhật 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593500"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation, Bản phát hành cập nhật 37, V3. Phiên bản này có số bản dựng là V3.10.58.120 và thường có sẵn thông qua bản tự cập nhật vào tháng 11 năm 2021.

## <a name="update-release-37"></a>Phát hành bản cập nhật 37

### <a name="bug-fixes"></a>Sửa lỗi

Các vấn đề sau đã được khắc phục.

**Thời gian và Chi phí**
- Người dùng không thể xóa mục nhập thời gian bằng cách xóa ô.
- Dạng xem **Phê duyệt không thành công của tôi** chỉ chứa các phê duyệt dự án với trạng thái **Đã gửi**.

**Quản lý dự án**
- Người dùng nhận được lỗi ngoại lệ tham chiếu rỗng khi mở một dự án trong phần bổ trợ máy tính để bàn của Microsoft nếu tên vị trí của thành viên nhóm Dự án bị bỏ trống.
- Không có nút **Lưu** trên trang **Nhiệm vụ Dự án** nên người dùng không thể lưu các thay đổi đối với bản ghi nhiệm vụ.
- Người dùng không thể xóa dự án có nhiệm vụ được liên kết với báo giá có trạng thái **Đã chốt**.

**Bán hàng**
- Trường **Đơn vị tiền tệ** trên trang **Dự án** được cập nhật để khớp với đơn vị tiền tệ của mẫu được áp dụng.
- Chi phí được tính không chính xác trên các nhiệm vụ có nhiều đơn vị tiền tệ.
