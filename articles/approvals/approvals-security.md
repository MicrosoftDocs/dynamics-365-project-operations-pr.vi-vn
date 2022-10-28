---
title: Bảo mật và phê duyệt
description: Bài viết này cung cấp thông tin về thiết lập bảo mật để làm việc với các phê duyệt trong Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709424"
---
# <a name="security-and-approvals"></a>Bảo mật và phê duyệt

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Microsoft Dynamics 365 Project Operations sử dụng hai vai trò bảo mật để cho phép phê duyệt các mục nhập thời gian, chi phí và vật chất:

- Người phê duyệt Dự án
- Quản trị viên người phê duyệt dự án

## <a name="project-approver"></a>Người phê duyệt Dự án

Bạn phải có **Người phê duyệt dự án** vai trò bảo mật để phê duyệt các mục nhập thời gian, chi phí và vật liệu của dự án. Bạn cũng phải có quyền truy cập vào các thực thể liên quan có liên quan, chẳng hạn như **Dự án**. Quyền truy cập đó có thể được chỉ định bởi người có **Quản lý dự án** vai diễn. Ngoài ra, bạn phải là thành viên trong nhóm của dự án và được đánh dấu là người phê duyệt.

Để phê duyệt các mục không thuộc dự án, bạn phải là người quản lý của người gửi.

## <a name="project-approver-admin"></a>Quản trị viên người phê duyệt dự án

> [!NOTE]
> Các [Bộ phê duyệt](approval-sets.md) tính năng này phải được bật trước khi bạn có thể sử dụng chức năng Quản trị viên trình duyệt dự án.

Các **Quản trị viên người phê duyệt dự án** vai trò bảo mật cho phép người dùng bỏ qua các chính sách và cho phép phê duyệt các mục nhập trên tất cả các dự án. Việc chỉ định vai trò này sẽ bỏ qua logic xác thực yêu cầu tư cách thành viên nhóm và được đánh dấu là người phê duyệt. Bạn phải có quyền truy cập vào các bảng liên quan có liên quan, chẳng hạn như **Dự án**, thông qua các vai trò bảo mật được chỉ định cho bạn.

Ngữ cảnh người dùng SYSTEM bỏ qua xác thực theo cách giống như Quản trị viên trình duyệt dự án vai trò bảo mật.
