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
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="df61a-103">Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3 đợt 1 2020</span><span class="sxs-lookup"><span data-stu-id="df61a-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="df61a-104">Chủ đề nêu bật những thông tin cần cân nhắc chính khi nâng cấp khi chuyển sang bản phát hành mới nhất của Project Service Automation (PSA) phiên bản 3.x đợt 1 2020.</span><span class="sxs-lookup"><span data-stu-id="df61a-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="df61a-105">Mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="df61a-105">Time entry</span></span>
<span data-ttu-id="df61a-106">Trải nghiệm mục nhập thời gian đã được gia hạn để cung cấp khả năng kéo dài mục nhập thời gian vào nhiều tình huống khách hàng hơn.</span><span class="sxs-lookup"><span data-stu-id="df61a-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="df61a-107">Điều này bao gồm khả năng thêm các loại mục nhập, hiện điều khiển hành vi cụ thể dựa vào tên lược đồ trường **Cài đặt mục nhập thời gian**, hiển thị dưới dạng **Nguồn thời gian**.</span><span class="sxs-lookup"><span data-stu-id="df61a-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="df61a-108">Xem xét việc nâng cấp</span><span class="sxs-lookup"><span data-stu-id="df61a-108">Upgrade consideration</span></span>
<span data-ttu-id="df61a-109">Để hỗ trợ chức năng này, các vai trò trong PSA đã được cập nhật để bao gồm các đặc quyền mới.</span><span class="sxs-lookup"><span data-stu-id="df61a-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="df61a-110">Những đặc quyền này cấp quyền truy cập đọc vào thực thể mới, **Cài đặt mục nhập thời gian**.</span><span class="sxs-lookup"><span data-stu-id="df61a-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="df61a-111">Người dùng yêu cầu khả năng ghi lại thời gian phải được cấp vai trò người dùng **Người dùng mục nhập thời gian** ngoài các vai trò hiện có.</span><span class="sxs-lookup"><span data-stu-id="df61a-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="df61a-112">Vai trò này bao gồm chức năng mới và đảm bảo rằng mục nhập thời gian sẽ tiếp tục hoạt động.</span><span class="sxs-lookup"><span data-stu-id="df61a-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="df61a-113">Các thay đổi của mục nhập thời gian hiện được gia hạn</span><span class="sxs-lookup"><span data-stu-id="df61a-113">Currently extended time entry changes</span></span>
<span data-ttu-id="df61a-114">Để giảm thiểu tác động đến người dùng hiện tại của mục nhập thời gian, thay đổi vai trò này là yêu cầu cốt lõi duy nhất cần thiết để tiếp tục sử dụng mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="df61a-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="df61a-115">Nếu bạn đã tạo dạng xem tùy chỉnh hoặc trải nghiệm mục nhập thời gian riêng biệt, bạn phải đặt trường **Cài đặt mục nhập thời gian** thành giá trị PSA chính xác.</span><span class="sxs-lookup"><span data-stu-id="df61a-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
