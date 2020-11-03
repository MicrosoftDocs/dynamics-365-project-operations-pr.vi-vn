---
title: Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3.x đợt 1 2020
description: Chủ đề này cung cấp thông tin về tính năng mới và đã thay đổi trong Project Service Automation phiên bản 3 đợt 1 2020.
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087054"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="f5cfe-103">Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3 đợt 1 2020</span><span class="sxs-lookup"><span data-stu-id="f5cfe-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="f5cfe-104">Chủ đề nêu bật những thông tin cần cân nhắc chính khi nâng cấp khi chuyển sang bản phát hành mới nhất của Project Service Automation (PSA) phiên bản 3.x đợt 1 2020.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="f5cfe-105">Mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="f5cfe-105">Time entry</span></span>
<span data-ttu-id="f5cfe-106">Trải nghiệm mục nhập thời gian đã được gia hạn để cung cấp khả năng kéo dài mục nhập thời gian vào nhiều tình huống khách hàng hơn.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="f5cfe-107">Điều này bao gồm khả năng thêm các loại mục nhập, hiện điều khiển hành vi cụ thể dựa vào tên lược đồ trường **Cài đặt mục nhập thời gian** , hiển thị dưới dạng **Nguồn thời gian**.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings** , displayed as **Time Source**.</span></span> <span data-ttu-id="f5cfe-108">Một giải pháp mới, được gọi là Thời gian, Chi phí, Trạng thái và Phê duyệt (TESA) đã được thêm vào để hỗ trợ chức năng này.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="f5cfe-109">Xem xét việc nâng cấp</span><span class="sxs-lookup"><span data-stu-id="f5cfe-109">Upgrade consideration</span></span>
<span data-ttu-id="f5cfe-110">Để hỗ trợ chức năng này, các vai trò trong PSA đã được cập nhật để bao gồm các đặc quyền mới.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="f5cfe-111">Những đặc quyền này cấp quyền truy cập đọc vào thực thể mới, **Cài đặt mục nhập thời gian**.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="f5cfe-112">Người dùng yêu cầu khả năng ghi lại thời gian phải được cấp vai trò người dùng **Người dùng mục nhập thời gian** ngoài các vai trò hiện có.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="f5cfe-113">Vai trò này bao gồm chức năng mới và đảm bảo rằng mục nhập thời gian sẽ tiếp tục hoạt động.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="f5cfe-114">Ngoài ra, nếu bạn có bất kỳ mô-đun ứng dụng tùy chỉnh nào bao gồm tất cả các biểu mẫu cho thực thể mục nhập thời gian, bạn sẽ được yêu cầu xóa **Biểu mẫu tạo nhanh mục nhập thời gian TESA** từ mô-đun đó.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="f5cfe-115">Các thay đổi của mục nhập thời gian hiện được gia hạn</span><span class="sxs-lookup"><span data-stu-id="f5cfe-115">Currently extended time entry changes</span></span>
<span data-ttu-id="f5cfe-116">Để giảm thiểu tác động đến người dùng hiện tại của mục nhập thời gian, thay đổi vai trò này là yêu cầu cốt lõi duy nhất cần thiết để tiếp tục sử dụng mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="f5cfe-117">Nếu bạn đã tạo dạng xem tùy chỉnh hoặc trải nghiệm mục nhập thời gian riêng biệt, bạn phải đặt trường **Cài đặt mục nhập thời gian** thành giá trị PSA chính xác.</span><span class="sxs-lookup"><span data-stu-id="f5cfe-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
