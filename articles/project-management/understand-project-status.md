---
title: Hiểu trạng thái của dự án
description: Chủ đề này cung cấp thông tin về trạng thái đã gán dự án trong Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965702"
---
# <a name="understand-project-status"></a><span data-ttu-id="db455-103">Hiểu trạng thái của dự án</span><span class="sxs-lookup"><span data-stu-id="db455-103">Understand project status</span></span>

<span data-ttu-id="db455-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="db455-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="db455-105">Phần **Trạng thái** trên trang **Thực thể dự án** cung cấp thông tin tóm tắt về tình trạng của dự án dựa trên chi phí và nhân công.</span><span class="sxs-lookup"><span data-stu-id="db455-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="db455-106">Trường tóm tắt trạng thái</span><span class="sxs-lookup"><span data-stu-id="db455-106">Status summary fields</span></span>

- <span data-ttu-id="db455-107">Trường **Tổng quan trạng thái dự án** là trường có thể chỉnh sửa hiển thị trạng thái tổng quan của dự án.</span><span class="sxs-lookup"><span data-stu-id="db455-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="db455-108">Trường này dùng mã màu, chẳng hạn như xanh lục, vàng và đỏ để chỉ ra rủi ro gia tăng.</span><span class="sxs-lookup"><span data-stu-id="db455-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="db455-109">Trường **Nhận xét** cho phép người quản lý dự án nhập nhận xét cụ thể về trạng thái.</span><span class="sxs-lookup"><span data-stu-id="db455-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="db455-110">Trường **Ngày cập nhật trạng thái** là trường không thể chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="db455-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="db455-111">Giá trị trong trường này là dấu thời gian cho biết thời điểm trạng thái được cập nhật lần gần đây nhất.</span><span class="sxs-lookup"><span data-stu-id="db455-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="db455-112">Các trường **Hiệu suất lịch trình** và **Hiệu suất chi phí** được đặt từ lưới theo dõi.</span><span class="sxs-lookup"><span data-stu-id="db455-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="db455-113">Khi chênh lệch lịch trình và chi phí cho các nút gốc trong dạng xem **Theo dõi nhân công** dương, bạn có thể đặt các trường này thành **Ahead**.</span><span class="sxs-lookup"><span data-stu-id="db455-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="db455-114">Khi chênh lệch lịch trình và chi phí cho nút gốc âm, các trường này được đặt thành **Sau**.</span><span class="sxs-lookup"><span data-stu-id="db455-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
