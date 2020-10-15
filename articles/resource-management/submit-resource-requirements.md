---
title: Gửi đề nghị nguồn lực
description: Bạn có thể gửi yêu cầu nguồn lực được tạo ra dưới dạng yêu cầu nguồn lực. Sau đó, yêu cầu này được gửi tới người quản lý nguồn lực để thực hiện.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961760"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="b048f-104">Gửi đề nghị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="b048f-104">Submit a resource request</span></span>

<span data-ttu-id="b048f-105">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="b048f-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b048f-106">Bạn có thể gửi yêu cầu nguồn lực được tạo ra dưới dạng yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="b048f-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="b048f-107">Sau đó, yêu cầu này được gửi tới người quản lý nguồn lực để thực hiện.</span><span class="sxs-lookup"><span data-stu-id="b048f-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="b048f-108">Trong Dynamics 365 Project Operations, trên trang **Dự án**, hãy chọn tab **Nhóm** để xem danh sách các nguồn lực có thể đặt.</span><span class="sxs-lookup"><span data-stu-id="b048f-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="b048f-109">Chọn nguồn lực chung có yêu cầu nguồn lực từ danh sách rồi nhấp vào **Gửi yêu cầu**.</span><span class="sxs-lookup"><span data-stu-id="b048f-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="b048f-110">Trạng thái yêu cầu của thành viên nhóm chung sẽ thay đổi thành **Đã gửi**.</span><span class="sxs-lookup"><span data-stu-id="b048f-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="b048f-111">Sau khi yêu cầu này được thực hiện, nguồn lực chung được thay thế bằng một nguồn lực được đặt tên nếu người quản lý nguồn lực thực hiện yêu cầu bằng cách đăng ký nguồn lực được đặt tên.</span><span class="sxs-lookup"><span data-stu-id="b048f-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="b048f-112">Ngoài ra, nếu người quản lý nguồn lực đề xuất một nguồn lực được đặt tên, thì nguồn lực chung sẽ vẫn còn trong nhóm và trạng thái yêu cầu sẽ thay đổi thành **Cần đánh giá**.</span><span class="sxs-lookup"><span data-stu-id="b048f-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
