---
title: Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3.x đợt 1 2020
description: Chủ đề này cung cấp thông tin về tính năng mới và đã thay đổi trong Project Service Automation phiên bản 3 đợt 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757051"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3 đợt 1 2020
Chủ đề nêu bật những thông tin cần cân nhắc chính khi nâng cấp khi chuyển sang bản phát hành mới nhất của Project Service Automation (PSA) phiên bản 3.x đợt 1 2020.

## <a name="time-entry"></a>Mục nhập thời gian
Trải nghiệm mục nhập thời gian đã được gia hạn để cung cấp khả năng kéo dài mục nhập thời gian vào nhiều tình huống khách hàng hơn. Điều này bao gồm khả năng thêm các loại mục nhập, hiện điều khiển hành vi cụ thể dựa vào tên lược đồ trường **Cài đặt mục nhập thời gian**, hiển thị dưới dạng **Nguồn thời gian**.

### <a name="upgrade-consideration"></a>Xem xét việc nâng cấp
Để hỗ trợ chức năng này, các vai trò trong PSA đã được cập nhật để bao gồm các đặc quyền mới. Những đặc quyền này cấp quyền truy cập đọc vào thực thể mới, **Cài đặt mục nhập thời gian**.

Người dùng yêu cầu khả năng ghi lại thời gian phải được cấp vai trò người dùng **Người dùng mục nhập thời gian** ngoài các vai trò hiện có. Vai trò này bao gồm chức năng mới và đảm bảo rằng mục nhập thời gian sẽ tiếp tục hoạt động.

### <a name="currently-extended-time-entry-changes"></a>Các thay đổi của mục nhập thời gian hiện được gia hạn
Để giảm thiểu tác động đến người dùng hiện tại của mục nhập thời gian, thay đổi vai trò này là yêu cầu cốt lõi duy nhất cần thiết để tiếp tục sử dụng mục nhập thời gian. Nếu bạn đã tạo dạng xem tùy chỉnh hoặc trải nghiệm mục nhập thời gian riêng biệt, bạn phải đặt trường **Cài đặt mục nhập thời gian** thành giá trị PSA chính xác.
