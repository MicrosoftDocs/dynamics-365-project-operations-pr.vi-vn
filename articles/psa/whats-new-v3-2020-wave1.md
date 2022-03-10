---
title: Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3.x đợt 1 2020
description: Chủ đề này cung cấp thông tin về tính năng mới và đã thay đổi trong Project Service Automation phiên bản 3 đợt 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a88b777c54ce54935d5483f616f3a24724ee192d40fbfd5d514f990e958dd5ea
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002132"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3 đợt 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Chủ đề nêu bật những thông tin cần cân nhắc chính khi nâng cấp khi chuyển sang bản phát hành mới nhất của Project Service Automation (PSA) phiên bản 3.x đợt 1 2020.

## <a name="time-entry"></a>Mục nhập thời gian
Trải nghiệm mục nhập thời gian đã được gia hạn để cung cấp khả năng kéo dài mục nhập thời gian vào nhiều tình huống khách hàng hơn. Điều này bao gồm khả năng thêm các loại mục nhập, hiện điều khiển hành vi cụ thể dựa vào tên lược đồ trường **Cài đặt mục nhập thời gian**, hiển thị dưới dạng **Nguồn thời gian**. Một giải pháp mới, được gọi là Thời gian, Chi phí, Trạng thái và Phê duyệt (TESA) đã được thêm vào để hỗ trợ chức năng này.

### <a name="upgrade-consideration"></a>Xem xét việc nâng cấp
Để hỗ trợ chức năng này, các vai trò trong PSA đã được cập nhật để bao gồm các đặc quyền mới. Những đặc quyền này cấp quyền truy cập đọc vào thực thể mới, **Cài đặt mục nhập thời gian**.

Người dùng yêu cầu khả năng ghi lại thời gian phải được cấp vai trò người dùng **Người dùng mục nhập thời gian** ngoài các vai trò hiện có. Vai trò này bao gồm chức năng mới và đảm bảo rằng mục nhập thời gian sẽ tiếp tục hoạt động.

Ngoài ra, nếu bạn có bất kỳ mô-đun ứng dụng tùy chỉnh nào bao gồm tất cả các biểu mẫu cho thực thể mục nhập thời gian, bạn sẽ được yêu cầu xóa **Biểu mẫu tạo nhanh mục nhập thời gian TESA** từ mô-đun đó.

### <a name="currently-extended-time-entry-changes"></a>Các thay đổi của mục nhập thời gian hiện được gia hạn
Để giảm thiểu tác động đến người dùng hiện tại của mục nhập thời gian, thay đổi vai trò này là yêu cầu cốt lõi duy nhất cần thiết để tiếp tục sử dụng mục nhập thời gian. Nếu bạn đã tạo dạng xem tùy chỉnh hoặc trải nghiệm mục nhập thời gian riêng biệt, bạn phải đặt trường **Cài đặt mục nhập thời gian** thành giá trị PSA chính xác.


[!INCLUDE[footer-include](../includes/footer-banner.md)]